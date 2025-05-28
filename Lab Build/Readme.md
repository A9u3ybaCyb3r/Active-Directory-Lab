# 🔤 Microsoft Evaluation Center – Windows VM Setup Guide

## 📚 Table of Contents

### 🔤 Microsoft Evaluation Center – Windows VM Setup Guide

* [🌐 Step 1: Access the Microsoft Evaluation Center](#-step-1-access-the-microsoft-evaluation-center)
* [🧰 Step 2: Why Use a Virtual Machine?](#-step-2-why-use-a-virtual-machine)
* [🗭 Step 3: Navigate the Download Page](#-step-3-navigate-the-download-page)
* [📅 Step 4: Download the ISO File](#-step-4-download-the-iso-file)
* [🔧 Step 5: Create VM Using ISO](#-step-5-create-vm-using-iso)
* [💡 Tips](#-tips)
* [🧪 Summary Table](#-summary-table)

### 🖠️ Installing Windows 11 in VirtualBox

* [🧱 Step 1: New VM Setup](#-step-1-new-vm-setup)
* [⚙️ Step 2: Configure Settings](#-step-2-configure-settings)
* [🤮 Step 3: Assign Resources](#-step-3-assign-resources)
* [📀 Step 4: Set Up Hard Disk](#-step-4-set-up-hard-disk)
* [🚫 Step 5: Boot and Begin Install](#-step-5-boot-and-begin-install)
* [🧙 Step 6: Complete Installation Wizard](#-step-6-complete-installation-wizard)
* [👤 Step 7: Local Account Setup](#-step-7-local-account-setup)
* [🚫 Step 8: Privacy Settings](#-step-8-privacy-settings)

### 💻 Guest Additions & Full Screen

* [🧙 Step 1: Log In](#-step-1-log-in)
* [📀 Step 2: Insert Guest Additions CD](#-step-2-insert-guest-additions-cd)
* [🛠️ Step 3: Run Installer](#-step-3-run-installer)
* [🔄 Step 4: Reboot](#-step-4-reboot)
* [💻 Step 5: Full Screen Mode](#-step-5-full-screen-mode)

### 📸 Taking & Restoring Snapshots

* [🧬 Why Snapshots?](#-why-snapshots)
* [📸 Step 1: Take Snapshot](#-step-1-take-snapshot)
* [📂 Step 2: Test (optional)](#-step-2-test-optional)
* [🛀 Step 3: Power Off](#-step-3-power-off)
* [🔄 Step 4: Restore Snapshot](#-step-4-restore-snapshot)
* [▶️ Step 5: Restart VM](#️-step-5-restart-vm)

### ✅ Final

* [🚀 You’re Ready!](#-youre-ready)

---

## 🌐 Step 1: Access the Microsoft Evaluation Center

🔗 Visit: [Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter)

Perfect for setting up lab environments with free trial versions of Windows 11 Enterprise. 🧪💻

---

## 🧰 Step 2: Why Use a Virtual Machine?

* 🔄 **Snapshots** make testing reversible
* 💣 Safe from damaging host system
* 🧪 Great for hands-on OS install practice
* 🛡️ Isolated and secure

> ⚠️ Always use a VM — never your main system for testing labs.

---

## 🗭 Step 3: Navigate the Download Page

1. Scroll to **Windows** section
2. Click **Windows 11 Enterprise**
3. You’ll be redirected to the download form

---

## 📅 Step 4: Download the ISO File

1. Fill out the form (use placeholders if needed)
2. Click **Download Now**
3. Choose **English (US)** + **64-bit ISO**
4. File will start downloading — valid for **90 days**

---

## 🔧 Step 5: Create VM Using ISO

* Launch **VirtualBox** / other hypervisor
* Create new VM ✅
* Load ISO as startup disk
* Install Windows 11 normally
* Take a **snapshot** after setup

---

## 💡 Tips

* 📆 Reminder: rearm/reset before 90 days
* 🧠 Practice snapshot workflow
* 🌍 Use same VM throughout the course

---

## 🧪 Summary Table

| Step | Task                         |
| ---- | ---------------------------- |
| 🌐   | Go to Evaluation Center      |
| 🔍   | Select Windows 11 Enterprise |
| 📝   | Complete short form          |
| 📂   | Download ISO (64-bit)        |
| 🔧   | Set up VM                    |
| 🧼   | Take clean snapshot          |

---

# 🖠️ Installing Windows 11 in VirtualBox

## 🧱 Step 1: New VM Setup

1. Open **VirtualBox**
2. Click **Tools** → **New**
3. Name it and select your ISO image
4. Click **Open**

---

## ⚙️ Step 2: Configure Settings

* Auto-detected as **Windows 11 Enterprise**
* Check **Skip Unattended Installation** ✅
* Click **Next**

---

## 🤮 Step 3: Assign Resources

* RAM: **4 GB minimum**, **8 GB+ recommended**
* CPU: **2+ cores** (watch the green usage bar)
* Click **Next**

---

## 📀 Step 4: Set Up Hard Disk

* Disk size: **80 GB** (dynamic)
* Uncheck **Pre-allocate full size**
* Click **Next** → **Finish**

---

## 🚫 Step 5: Boot and Begin Install

* Select VM → Click **Start** ▶️
* Press **Enter** when prompted to boot from CD

---

## 🧙 Step 6: Complete Installation Wizard

* Accept defaults (Language, Keyboard)
* Click **Install Now**
* Accept license → Click **Next**
* Choose **Custom Install**
* Select the drive → Click **Next**

---

## 👤 Step 7: Local Account Setup

* Choose region/keyboard: US
* Skip network setup
* Sign-in Options → **Domain Join Instead**
* Enter name/password/security Qs

---

## 🚫 Step 8: Privacy Settings

* Uncheck all boxes for privacy ✉️
* Click **Accept**

---

# 💻 Guest Additions & Full Screen

## 🧙 Step 1: Log In

* Drag up to unlock
* Enter your password

## 📀 Step 2: Insert Guest Additions CD

* Devices → Insert Guest Additions CD image
* Open File Explorer → locate DVD drive

## 🛠️ Step 3: Run Installer

* Right-click `VBoxWindowsAdditions-amd64.exe` → Run as Admin
* Follow wizard steps → Install

## 🔄 Step 4: Reboot

* Click **Reboot Now** after install
* Log back into Windows

## 💻 Step 5: Full Screen Mode

* View → Auto-resize Guest Display ✅
* View → Full Screen Mode (Host + F)

---

# 📸 Taking & Restoring Snapshots

## 🧬 Why Snapshots?

* Saves entire VM state
* Helps with repeatability & error recovery

## 📸 Step 1: Take Snapshot

* Machine → Take Snapshot
* Name it (e.g., "Fresh Install") → OK

## 📂 Step 2: Test (optional)

* Create a temp file or folder

## 🛀 Step 3: Power Off

* Close VM → Power Off

## 🔄 Step 4: Restore Snapshot

* Snapshots pane → Select snapshot → Restore
* Uncheck "Keep current state" → Confirm

## ▶️ Step 5: Restart VM

* Click **Start**
* Temp changes gone? Snapshot worked! 🎉

---

## 🚀 You’re Ready!

Take a snapshot after every config milestone. Need help exporting or cloning VMs next? Just ask! 🧳

---

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

