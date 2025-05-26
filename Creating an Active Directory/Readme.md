# 💾 Downloading & Installing Windows Server 2022 for Active Directory Labs

This guide walks you through:

* Downloading **Windows Server 2022** from Microsoft's Evaluation Center
* Installing it on VirtualBox
* Configuring a **Domain Controller** (`DC01`)
* Adding users, clients, shared folders, and applying GPOs

---

## 📚 Table of Contents

* [🔎 Download Windows Server 2022](#-download-windows-server-2022)
* [🛠️ Install on VirtualBox](#️-install-on-virtualbox)
* [🏛️ Configure as Domain Controller](#️-configure-as-domain-controller)
* [👥 Add Users in ADUC](#-add-users-in-aduc)
* [🏁 Join Windows 11 to Domain](#-join-windows-11-to-domain)
* [🧱 OUs vs Groups & Folder Sharing](#-ous-vs-groups--folder-sharing)
* [🛠️ GPO: Set Desktop Wallpaper](#️-gpo-set-desktop-wallpaper)

---

## 🔎 Download Windows Server 2022

1. Visit: [Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter)
2. Select **Windows Server 2022**
3. Click **Get Started for Free**
4. Fill out the form and download the **64-bit ISO**
5. Save it to your lab folder (e.g., `AD-Lab-Files`)

---

## 🛠️ Install on VirtualBox

1. Open **VirtualBox** → **New VM**
2. Attach the downloaded ISO
3. Skip Unattended Installation ✅
4. Allocate:

   * **RAM**: 8 GB
   * **CPU**: 4 cores
   * **Disk**: 50 GB (dynamic)
5. Start VM → Boot into ISO
6. Choose **Standard Eval (Desktop Experience)**
7. Custom install → Select disk → Next
8. Set admin password: `P@ssword!`
9. First login: **Insert Ctrl+Alt+Del** → enter password

---

### 🧰 Post-Install Enhancements

1. Devices → Insert Guest Additions CD
2. Run installer inside VM (as Admin)
3. Reboot → Enable full screen
4. Take a snapshot: `Server 2022 Fresh Install`

---

## 🏛️ Configure as Domain Controller

### Rename the Server:

* PC Name: `DC01` → Restart

### Install AD DS:

1. Server Manager → Add Roles → Select **AD DS**
2. Add Features → Continue → Install

### Promote to Domain Controller:

1. Server Manager → Promote → Add new forest: `lab.local`
2. Set DSRM password
3. Default paths → Prerequisite check → ✅ Install → Reboot

### Install AD CS:

1. Add Roles → Select **AD Certificate Services**
2. Add Features → Install
3. Configure → Certification Authority → Enterprise CA → New key
4. Defaults → 5-year validity → Finish

---

## 👥 Add Users in ADUC

1. Tools → AD Users & Computers (ADUC)
2. Create OUs:

   * Engineering
   * Management
   * IT → Administrators (nested)
3. Move users to OUs:

   * `rhendricks`, `nbighetti` → Engineering
   * `ebachman`, `jdunn` → Management
   * `Administrator` → IT > Administrators

### Add Users:

* Right-click → New → User
* Example:

  * Name: `Richard Hendricks`
  * Username: `rhendricks`
  * Password: `P@ssword1!`
  * Set: Password never expires ✅

📋 Repeat for:

| Name            | Username  |
| --------------- | --------- |
| Nelson Bighetti | nbighetti |
| Erlich Bachman  | ebachman  |
| Jared Dunn      | jdunn     |

---

## 🏁 Join Windows 11 to Domain

### Set Up VirtualBox NAT Network:

* File > Network Manager → Create NAT Network → `AD Network`
* Attach both VMs to `AD Network`

### Assign Static IPs:

| Device | IP        | DNS       |
| ------ | --------- | --------- |
| DC01   | 10.0.2.15 | 127.0.0.1 |
| WS01   | 10.0.2.16 | 10.0.2.15 |

### Rename Workstation:

* Name: `WS01` → Reboot

### Join Domain:

* Settings → Access work/school → Join local AD domain → `lab.local`
* Credentials: `administrator` / `P@ssword!`
* Restart → Log in as `lab\rhendricks`

### Verify Join:

* On DC: ADUC → `lab.local > Computers` → ✅ `WS01` listed

---

## 🧱 OUs vs Groups & Folder Sharing

### Create Security Group:

* OU: Engineering
* Group: `Engineering Share`
* Add: Richard, Nelson, Jared

### Create Shared Folder:

* File & Storage Services → New Share
* Path: `C:\Engineering Share`
* Customize permissions:

  * Remove `Users`
  * Add `Engineering Share` group → Read/Write

### Test Access:

* Log in as Jared → `\\dc01\Engineering Share` → ✅ Can write
* Log in as Erlich → ❌ Access Denied

---

## 🛠️ GPO: Set Desktop Wallpaper

### Create GPO:

1. Paint: Create `Engineering_Wallpaper.jpg`
2. Save in: `\\dc01\netlogon\`
3. Group Policy Management → OU: Engineering → New GPO: `Set Engineering Background`

### Configure:

* Edit GPO → User Config → Admin Templates → Desktop → Desktop Wallpaper
* Enable → Set path: `\\dc01\netlogon\Engineering_Wallpaper.jpg`

### Test:

* Log in as `rhendricks` → ✅ Wallpaper appears
* Log in as `ebachman` → ❌ No change

---

## ✅ Final Summary

| Component                     | Status |
| ----------------------------- | ------ |
| Windows Server 2022 Installed | ✅      |
| Domain Controller Configured  | ✅      |
| Users & OUs Created           | ✅      |
| Workstation Joined Domain     | ✅      |
| Group Access Tested           | ✅      |
| GPO Applied to OU             | ✅      |

You're now fully set up to begin testing AD features, deploying security tools, and practicing real-world SOC analyst tasks! 💪
