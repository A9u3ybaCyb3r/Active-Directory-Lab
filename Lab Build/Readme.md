## 📚 Table of Contents

### 🪟 Microsoft Evaluation Center – Windows VM Setup

1. [🌐 Access the Microsoft Evaluation Center](#-step-1-access-the-microsoft-evaluation-center)
2. [🧰 Why Use a Virtual Machine?](#-step-2-why-use-a-virtual-machine)
3. [🗭 Navigate the Download Page](#-step-3-navigate-the-download-page)
4. [📅 Download the ISO File](#-step-4-download-the-iso-file)

---

### 🖥️ Installing Windows 11 in VirtualBox

8. [🧱 New VM Setup](#-step-1-new-vm-setup)
9. [⚙️ Configure Settings](#-step-2-configure-settings)
10. [🤮 Assign Resources](#-step-3-assign-resources)
11. [📀 Set Up Hard Disk](#-step-4-set-up-hard-disk)
12. [🚫 Boot and Begin Install](#-step-5-boot-and-begin-install)
13. [🧙 Complete Installation Wizard](#-step-6-complete-installation-wizard)
14. [👤 Local Account Setup](#-step-7-local-account-setup)
15. [🚫 Privacy Settings](#-step-8-privacy-settings)

---

### 💻 Guest Additions & Full Screen

16. [🧙 Log In](#-step-1-log-in)
17. [📀 Insert Guest Additions CD](#-step-2-insert-guest-additions-cd)
18. [🛠️ Run Installer](#-step-3-run-installer)
19. [🔄 Reboot](#-step-4-reboot)
20. [💻 Full Screen Mode](#-step-5-full-screen-mode)

---

### 📸 Taking & Restoring Snapshots

21. [🧬 Why Snapshots?](#-why-snapshots)
22. [📸 Take Snapshot](#-step-1-take-snapshot)
23. [📂 Test (optional)](#-step-2-test-optional)
24. [🛀 Power Off](#-step-3-power-off)
25. [🔄 Restore Snapshot](#-step-4-restore-snapshot)
26. [▶️ Restart VM](#️-step-5-restart-vm)

---

### 🖥️ Downloading & Installing Windows Server 2022 (Active Directory Lab)

27. [🔎 Download Windows Server 2022](#-download-windows-server-2022)
28. [🛠️ Install on VirtualBox](#️-install-on-virtualbox)
29. [🏛️ Configure as Domain Controller](#️-configure-as-domain-controller)

---

### 🧑‍💼 Active Directory & GPO Tasks

30. [👥 Add Users in ADUC](#-add-users-in-aduc)
31. [🏁 Join Windows 11 to Domain](#-join-windows-11-to-domain)
32. [🧱 OUs vs Groups & Folder Sharing](#-ous-vs-groups--folder-sharing)
33. [🛠️ GPO: Set Desktop Wallpaper](#️-gpo-set-desktop-wallpaper)

---

# 🔤 Microsoft Evaluation Center – Windows VM Setup Guide

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

![image](https://github.com/user-attachments/assets/875172c0-7af5-41fa-9997-95aaec062969)

![image](https://github.com/user-attachments/assets/43b760e1-7c7a-4d09-9361-35d8fb66aac0)

3. You’ll be redirected to the download form

---

## 📅 Step 4: Download the ISO File

1. Fill out the form (use placeholders if needed)
2. Click **Download Now**
3. Choose **English (US)** + **64-bit ISO**

![image](https://github.com/user-attachments/assets/79cdcf35-20cf-4329-9d47-badaef2aedec)

4. File will start downloading — valid for **90 days**

---

# 🖠️ Installing Windows 11 in VirtualBox

## 🧱 Step 1: New VM Setup

1. Open **VirtualBox**
2. Click **Tools** → **New**

![image](https://github.com/user-attachments/assets/20746b52-8d04-4297-a336-26327e0eff8c)

---

## ⚙️ Step 2: Configure Settings

* Name it and select your ISO image
* Auto-detected as **Windows 11 Enterprise**
* Check **Skip Unattended Installation** ✅
* Click **Next**

![image](https://github.com/user-attachments/assets/4e7eadf7-7591-463b-a2b8-e2474d8b0882)

---

## 🤮 Step 3: Assign Resources

* RAM: **4 GB minimum**, **8 GB+ recommended**
* CPU: **2+ cores** (watch the green usage bar)
* Click **Next**

![image](https://github.com/user-attachments/assets/69294904-4b76-402a-a1b7-d7512e5a4885)

---

## 📀 Step 4: Set Up Hard Disk

* Disk size: **80 GB** (dynamic)
* Uncheck **Pre-allocate full size**
* Click **Next** → **Finish**

![image](https://github.com/user-attachments/assets/46ad739f-5f27-4c5a-b893-5d14dc1e0d05)

---

## 🚫 Step 5: Boot and Begin Install

* Select VM → Click **Start** ▶️
* Press **Enter** when prompted to boot from CD

---

## 🧙 Step 6: Complete Installation Wizard

* Accept defaults (Language, Keyboard)

![image](https://github.com/user-attachments/assets/67258473-9145-4d25-bd79-ba2aa5e432ba)

![image](https://github.com/user-attachments/assets/6a7fc457-3fb8-4cee-b33a-dd9d97c09363)

* Click **Install Now**

![image](https://github.com/user-attachments/assets/f02907f3-570c-4862-97c9-d158790f40ef)

* Accept license → Click **Next**

![image](https://github.com/user-attachments/assets/250b3331-0786-41f9-acf6-62ae74f88b31)

* Choose **Custom Install**
* Select the drive → Click **Next**

![image](https://github.com/user-attachments/assets/f63664cc-da6a-4653-8704-87d2d5ceab5b)

* Click **Install**

![image](https://github.com/user-attachments/assets/ea26f59e-e60c-42ca-80cc-1a65932e3ca9)

* Wait for the installation to finish

---

## 👤 Step 7: Local Account Setup

* Choose region/keyboard: US

![image](https://github.com/user-attachments/assets/08135280-8a80-41bc-9262-44a82b2d4c23)

![image](https://github.com/user-attachments/assets/195973d8-daf1-4eb4-85d4-c6add30ccc0d)

* Skip network setup
* Sign-in Options → **Domain Join Instead**

![image](https://github.com/user-attachments/assets/a286f417-f137-4295-9f2d-f5e9d54e6cdf)

![image](https://github.com/user-attachments/assets/af913ea7-c17e-4857-baf2-b422119bb6f6)

* Enter name/password/security Qs

![image](https://github.com/user-attachments/assets/a620cd07-351b-4cf1-8203-83b21dd1213e)

![image](https://github.com/user-attachments/assets/ed0bc543-6c79-4944-802e-f27f6d85bf2d)

---

## 🚫 Step 8: Privacy Settings

* Uncheck all boxes for privacy ✉️
* Click **Accept**

![image](https://github.com/user-attachments/assets/3a544938-1e34-4a85-8f99-b6ed6feb94eb)

---

# 💻 Guest Additions & Full Screen

## 🧙 Step 1: Log In

* Drag up to unlock
* Enter your password

![image](https://github.com/user-attachments/assets/62b61ecb-af0f-4a0a-a38b-8d8a0eb88da1)

## 📀 Step 2: Insert Guest Additions CD

* Devices → Insert Guest Additions CD image

![image](https://github.com/user-attachments/assets/c8f8b806-f0a5-4ffc-aa26-3d1110afb6fe)

* Open File Explorer → locate DVD drive

![image](https://github.com/user-attachments/assets/7dd06d13-be44-46ff-a0d1-768250b3ed98)

## 🛠️ Step 3: Run Installer

* Right-click `VBoxWindowsAdditions-amd64.exe` → Run as Admin
* Follow wizard steps → Install

![image](https://github.com/user-attachments/assets/2a146460-403f-4570-b8ca-ab90a02a8698)

## 🔄 Step 4: Reboot

* Click **Reboot Now** after install

![image](https://github.com/user-attachments/assets/376a334d-c56c-4ac0-bf26-6af6b8c4f7d4)

* Log back into Windows

## 💻 Step 5: Full Screen Mode

* View → Auto-resize Guest Display ✅
* View → Full Screen Mode (Host + F)

![image](https://github.com/user-attachments/assets/33dba844-0bc5-41f9-b962-c6ca3f81e3c3)

---

# 📸 Taking & Restoring Snapshots

## 🧬 Why Snapshots?

* Saves entire VM state
* Helps with repeatability & error recovery

## 📸 Step 1: Take Snapshot

* Machine → Take Snapshot

![image](https://github.com/user-attachments/assets/563d31e1-8c98-4911-b703-8347c3d935f9)

* Name it (e.g., "Fresh Install") → OK

![image](https://github.com/user-attachments/assets/31d15183-a08c-415c-9bf0-49ad7ad34e42)

## 📂 Step 2: Test (optional)

* Create a temp file or folder

![image](https://github.com/user-attachments/assets/3b7520c2-77af-455f-8d00-f98025c8a7d6)

![image](https://github.com/user-attachments/assets/8e5d6984-278c-4b43-bd67-9d2ff28fed4b)

## 🛀 Step 3: Power Off

* Close VM → Power Off

![image](https://github.com/user-attachments/assets/f7c173b7-cce4-4280-9cb8-ab45d82f6efa)

## 🔄 Step 4: Restore Snapshot

* Snapshots pane → Select snapshot → Restore

![image](https://github.com/user-attachments/assets/e2a6c7d8-9d80-481f-a7c7-a4250391ac36)

* Uncheck "Keep current state" → Confirm

![image](https://github.com/user-attachments/assets/a76cb846-8d93-4272-b962-4232ec58a54c)

## ▶️ Step 5: Restart VM

* Click **Start**
* Temp changes gone? Snapshot worked! 🎉

![image](https://github.com/user-attachments/assets/96765d52-9a24-45ae-a013-7e60a7fb3d8a)

---

# 💾 Downloading & Installing Windows Server 2022 for Active Directory Labs

This guide walks you through:

* Downloading **Windows Server 2022** from Microsoft's Evaluation Center.
* Installing it on VirtualBox
* Configuring a **Domain Controller** (`DC01`)
* Adding users, clients, shared folders, and applying GPOs

---

## 🔎 Download Windows Server 2022

1. Visit: [Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter)
2. Select **Windows Server 2022**

![image](https://github.com/user-attachments/assets/e8ffd345-600a-4678-946b-f8c4c0379a34)

3. On **Get Started for Free** click on **Download the ISO**

![image](https://github.com/user-attachments/assets/3f84cee9-7726-4276-8805-78210b713cd6)

4. Fill out the form and download the **64-bit ISO**

![image](https://github.com/user-attachments/assets/79a876e4-7843-4ef1-91ad-abaa84b9b55e)

5. Save it to your lab folder (e.g., `AD-Lab-Files`)

---

## 🛠️ Install on VirtualBox

1. Open **VirtualBox** → **New VM**

![image](https://github.com/user-attachments/assets/7a074b89-7508-48e5-9b5d-5dcbd83a027b)

2. Attach the downloaded ISO
3. Skip Unattended Installation ✅

![image](https://github.com/user-attachments/assets/6da08730-6d33-4a6e-a747-f9f169fb0a48)

4. Allocate:

   * **RAM**: 8 GB
   * **CPU**: 4 cores

![image](https://github.com/user-attachments/assets/198ee385-820c-499d-b61e-e34114791fcc)

   * **Disk**: 50 GB (dynamic)

![image](https://github.com/user-attachments/assets/9248cea8-54ba-4040-a689-4c3bb2942e92)

---

### 🚀 Start the VM & Begin Installation

- Click **Start** to launch the VM
- Follow setup prompts:
    - Language: English (United States)
    - Keyboard: US
    - Click **Install Now**

![image](https://github.com/user-attachments/assets/d35d7017-db99-4f08-8ade-6c2272bb0a7a)

![image](https://github.com/user-attachments/assets/e9054300-3e07-4daf-b9d2-dea17a6d200e)

---

### 🪟 Select Windows Server Edition

Choose:  
🔹 **Standard Evaluation (Desktop Experience)**  
Click **Next** → Accept Terms → Click **Next**

![image](https://github.com/user-attachments/assets/b73b21b9-c3a9-4b4c-bfbd-1b64e7130607)

![image](https://github.com/user-attachments/assets/468eca2c-b163-4ac1-b65e-8f54e29cd17b)

---

### 🖱️ Custom Install

- Select the listed drive (Drive 0)
- Click **Next**  
    The installation will begin (takes several minutes)

![image](https://github.com/user-attachments/assets/9acbb6cf-508a-4393-af40-01b190a3804f)

![image](https://github.com/user-attachments/assets/d963d8dc-c7be-4bdd-81a9-429f4fb5fa9e)

---

### 🔐 Set Administrator Password

Choose a **lab-friendly password** (example):

```
P@ssword!
```

![image](https://github.com/user-attachments/assets/779cc49a-1dcc-4021-a65c-810f2a2fd40e)

You’ll use this to log in later.

---

### 🔑 First Login

- On the login screen, go to:
```
Input > Keyboard > Insert Ctrl+Alt+Del
```

![image](https://github.com/user-attachments/assets/5b74d093-5f28-4cd9-b683-071416e7f34e)

- Enter your admin password

![image](https://github.com/user-attachments/assets/e807ab80-de18-4892-bdc0-b322feaf58b2)

---

### 🧰 Post-Install Enhancements

1. Devices → Insert Guest Additions CD

![image](https://github.com/user-attachments/assets/ca18c2d7-07b6-451a-b61b-968a3cd80e1d)

![image](https://github.com/user-attachments/assets/45f64abd-2b6d-428f-a5e2-a1d317faac99)

2. Run installer inside VM (as Admin)

![image](https://github.com/user-attachments/assets/7d1fb119-0a6a-4459-9422-d8e87ef7cfaa)

3. Reboot → Enable full screen

![image](https://github.com/user-attachments/assets/e5b20afd-ca25-41bb-afd4-d9853a35cc06)

4. Take a snapshot: `Server 2022 Fresh Install`

![image](https://github.com/user-attachments/assets/cae06742-ff42-4f9d-a9ef-210576922b92)

![image](https://github.com/user-attachments/assets/d20d18a4-e6e8-4bef-b109-95ccf5c89267)

---

## 🏛️ Configure as Domain Controller

### Rename the Server:

1. Click **Start** and type `View your PC name`

![image](https://github.com/user-attachments/assets/9544e9a7-98de-4945-9fe3-38e7ea5b6614)

2. Click **Rename this PC**

![image](https://github.com/user-attachments/assets/21e89af8-b584-4896-9469-ebf7f29f75d3)

3. PC Name: `DC01` → Restart Now

![image](https://github.com/user-attachments/assets/a3bbb637-f353-47ad-812f-c3de167b7a40)

![image](https://github.com/user-attachments/assets/f509823c-9366-4d33-89e4-e4139f151efc)

### Install Active Directory Domain Services:

1. After reboot, open **Server Manager**
2. Click **Manage > Add Roles and Features**

![image](https://github.com/user-attachments/assets/eabaf5ec-340d-4c9c-a436-715183fc039e)

3. Proceed with defaults until you reach **Server Roles**
4. Select ✅ **Active Directory Domain Services**
5. Click **Add Features** when prompted

![image](https://github.com/user-attachments/assets/45463c02-9e55-4340-9f47-25578a052acf)

![image](https://github.com/user-attachments/assets/a2e6885d-d8ad-47f3-8dc4-b843d524ef4e)

6. Continue clicking **Next** until you can check:
    - ☑️ Restart the destination server automatically if required

![image](https://github.com/user-attachments/assets/8e5f585f-81fd-4baf-9c81-dd392e92cda4)

🕐 Wait for installation to complete.

### Promote to Domain Controller:

1. Server Manager → Promote → Add new forest: `lab.local`

![image](https://github.com/user-attachments/assets/8bf0ff1c-7742-430d-9ebf-d6bc9fd8b689)

![image](https://github.com/user-attachments/assets/dcd771ef-367e-4ef4-8b65-3445c9c2dfb8)

2. Use the same admin password to set DSRM password if you prefer (e.g., `P@ssword!`)

![image](https://github.com/user-attachments/assets/80e1c9e6-c0e7-4bf4-b202-46fb7d3167cc)

3. Default paths → Prerequisite check → ✅ Install → Reboot

![image](https://github.com/user-attachments/assets/ebc8fba2-1784-4e1a-8bc2-6126cca8c760)

## 🔐 Log into the Domain

After reboot, you'll see:

```
lab\Administrator
```

![image](https://github.com/user-attachments/assets/97fcf826-92cd-40b7-9cd1-e2bbe3522fd6)

Login with your **admin password**.  
🎉 Congratulations — your server is now a **Domain Controller**!

### Install Active Directory Certificate Services (AD CS):

1. Add Roles → Select **AD Certificate Services**

![image](https://github.com/user-attachments/assets/9f8e1489-45bb-448f-8306-03a41b0425ef)

![image](https://github.com/user-attachments/assets/350fc42c-ade3-4f1a-95f7-a2d4943caf87)

2. Add Features → Install

![image](https://github.com/user-attachments/assets/54ae75f3-8f93-40a6-a27c-19144d4ab81a)

3. Proceed with all defaults and select

☑️ Restart the destination server automatically if required → then Install

![image](https://github.com/user-attachments/assets/5951b312-969e-48e4-b181-9e16d418d46b)

4. Configure Active Directory Certificate Services → Certification Authority → Enterprise CA → New key

![image](https://github.com/user-attachments/assets/01322bc2-d97a-4655-a1c3-627c089d4dcc)

![image](https://github.com/user-attachments/assets/8b0c037a-538a-44f8-a1de-879cc57e3e08)

![image](https://github.com/user-attachments/assets/79066cc2-3f10-411c-b3a4-fba2aee4f29f)

![image](https://github.com/user-attachments/assets/51d116ea-f16f-47a8-b8fa-dc8dfd311eb0)

5. Defaults → 5-year validity → Configure

![image](https://github.com/user-attachments/assets/cf0efa41-d945-4c26-9602-6e6b60c5b8d4)

![image](https://github.com/user-attachments/assets/a51871a8-3712-487a-b6bb-47dab53b785a)

---

## 👥 Add Users in ADUC

1. Tools → AD Users & Computers (ADUC)

![image](https://github.com/user-attachments/assets/b9379f67-a927-4350-bc93-2280792b43de)

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

