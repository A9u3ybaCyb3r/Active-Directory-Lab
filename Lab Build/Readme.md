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

2. Expand your domain:

![image](https://github.com/user-attachments/assets/83641300-e647-45ee-9b76-351d07c988f3)

- Move Built-In Groups to a New OU

3. Right-click your domain name (e.g., `lab.local`)
4. Select `New > Organizational Unit`

![image](https://github.com/user-attachments/assets/403f937c-207c-4e0c-9618-8bcd6d488c2a)

5. Name it `Groups`

![image](https://github.com/user-attachments/assets/d47db64c-e3b4-4c0b-9c6e-6463b2bb5693)

6. In the **Users** folder:
    - Select all groups (Shift + Click)
    - Drag them into the new `Groups` OU
    - Click **Yes** when prompted

![image](https://github.com/user-attachments/assets/d69d345d-3387-4caf-b49b-f15f8f3284f2)

![image](https://github.com/user-attachments/assets/cfb33891-8ddd-4cbb-9269-e747258acb81)

Now the **Users** folder will contain only user accounts for easier management ✅

![image](https://github.com/user-attachments/assets/27052db8-cef3-4904-8480-0713fd66ac2b)

---

### ➕ Create New Domain Users

1. Right-click inside the **Users** container
2. Select `New > User`

![image](https://github.com/user-attachments/assets/ef28ca41-c8c4-4f39-a0f1-51764a99111f)

3. Example:
    - **First Name**: Richard
    - **Last Name**: Hendricks
    - **User Logon Name**: `rhendricks` or `r.hendricks`

![image](https://github.com/user-attachments/assets/fa874822-1d7c-4de6-8f25-94156f5f170a)

4. Click **Next**

### 🔐 Set Password

Use a lab-friendly password:

```
P@ssword1!
```

![image](https://github.com/user-attachments/assets/59933664-6f3b-4817-86c6-6ab9533746e5)

5. Uncheck:
    - ☑️ User must change password at next login
6. Check:
    - ☑️ Password never expires
7. Click **Next > Finish**

---

## 🌀 Quickly Add More Users (via Copy)

To create more users efficiently:

1. Right-click your new user (e.g., `rhendricks`)
2. Click **Copy**

![image](https://github.com/user-attachments/assets/147a7a69-fde5-4732-8309-31ba7059cdcb)

### Create These Example Users (or your own):

|First Name|Last Name|Username|
|---|---|---|
|Nelson|Bighetti|`nbighetti`|
|Ehrlich|Bachman|`ebachman`|
|Jared|Dunn|`jdunn`|

For each user:

- Use the same password `P@ssword1!`
- Set **Password never expires**

Repeat the process to create all four domain users ✅

![image](https://github.com/user-attachments/assets/b6a150e3-f7d7-49de-9ec1-689307436ac1)

---

## 🏁 Join Windows 11 to Domain

### Set Up VirtualBox NAT Network:

* File > Network Manager → Create NAT Network → `ADNetwork`

![image](https://github.com/user-attachments/assets/dd03f5bb-e734-47a8-a84a-faebbf3f58e6)

![image](https://github.com/user-attachments/assets/20576fcf-104b-4f0e-86ae-9931da4a1ce9)

![image](https://github.com/user-attachments/assets/a626e84e-c390-4ae9-9585-17e9f789f8e1)

* Attach both VMs to `AD Network`

![image](https://github.com/user-attachments/assets/37f40482-56d0-4bed-8a20-5ea4ec73553e)

![image](https://github.com/user-attachments/assets/6ec71d32-79c3-407b-8262-ecaf70ebb574)

### 🌐 Assign Static IPs

#### 🖥️ On the **Domain Controller**:

1. Open **Command Prompt**, run:
```
ipconfig
```
    Example IP: `10.0.2.15`

![image](https://github.com/user-attachments/assets/748dbb29-d3f8-49ce-8178-325b3d523b98)

2. Right-click Internet
3. Go to:
```
Open Network & Internet Settings > Change Adapter Options
```
![image](https://github.com/user-attachments/assets/4c90fc1d-16e5-4ae1-b194-57afcd127937)

![image](https://github.com/user-attachments/assets/62b7efa5-893f-4418-a214-c6fbd3037403)

4. Right-click Ethernet > Properties

![image](https://github.com/user-attachments/assets/c31fa2b6-405d-48d6-b7ea-dad7e86623d3)

5. Double-click: **Internet Protocol Version 4 (TCP/IPv4)**

![image](https://github.com/user-attachments/assets/36b26ab4-07e0-419c-b5e6-ca3f7ab4fe8c)

6. Use these static IP settings:

![image](https://github.com/user-attachments/assets/b5ef7a64-8e6d-4916-a52f-d766eebb7825)

| Field           | Value         |
| --------------- | ------------- |
| IP Address      | 10.0.2.15     |
| Subnet Mask     | 255.255.255.0 |
| Default Gateway | 10.0.2.1      |
| Preferred DNS   | 127.0.0.1     |

Click **OK** → **Close**

---
### 💻 On the **Windows 11 Workstation**:

1. Run:
```
ipconfig
```
Example IP: `10.0.2.4`

![image](https://github.com/user-attachments/assets/bfa84d0e-c739-44ac-91ed-3209960e600b)

2. Go to `Network Connections > Ethernet > Properties > TCP/IPv4`

![image](https://github.com/user-attachments/assets/a7b9bc09-d41e-4853-a51e-07bc2061a47c)

![image](https://github.com/user-attachments/assets/c31d7d54-c39e-4731-805b-8b8c9ff92543)

![image](https://github.com/user-attachments/assets/0f4505ab-dd88-48b5-8f41-e2098f28e41c)

3. Use these settings:

![image](https://github.com/user-attachments/assets/3f6cd3ba-0a69-4344-8969-79a54fc99b56)

| Field           | Value         |
| --------------- | ------------- |
| IP Address      | 10.0.2.16     |
| Subnet Mask     | 255.255.255.0 |
| Default Gateway | 10.0.2.1      |
| Preferred DNS   | 10.0.2.15     |

Click **OK** → **Close**


### Rename Workstation:

* Name: `WS01` → Reboot

![image](https://github.com/user-attachments/assets/9527500a-7807-4955-b9bd-385890fd1287)

![image](https://github.com/user-attachments/assets/93d56a86-b59e-4d3d-ae5a-87e1c711570c)

![image](https://github.com/user-attachments/assets/f7eea589-d048-4480-85d2-51a2ffa81df5)

![image](https://github.com/user-attachments/assets/b544813b-0c64-40b2-a970-e440323ff808)

### Join Domain:

* On `WS01` go to Settings → Access work/school → Join local AD domain → `lab.local`

![image](https://github.com/user-attachments/assets/9bc70c57-747f-4f0f-8dd2-81eef72cb5bd)

![image](https://github.com/user-attachments/assets/c748084b-56e6-4abf-82c5-72923249a78f)

![image](https://github.com/user-attachments/assets/ecac5223-869d-486e-bb93-72174a613a2c)

![image](https://github.com/user-attachments/assets/c5ecc72c-3e8e-4439-90a8-f875ef86d608)

* Credentials: `administrator` / `P@ssword!`

![image](https://github.com/user-attachments/assets/35dc5cd2-86a6-4906-9b9d-301d66fcef6f)

* Select **Standard User**

![image](https://github.com/user-attachments/assets/37cccb78-4087-44a1-8e84-a1716a1ac396)

* Restart → Log in as `lab\rhendricks` with passoword of `P@ssword1!`

![image](https://github.com/user-attachments/assets/6ac496f3-bab8-44b7-ac86-274ea28bc2b4)

![image](https://github.com/user-attachments/assets/ee02c700-4c67-4d6a-8fb9-ed0c0cac8eae)

### Verify Join:

* On DC: ADUC → `lab.local > Computers` → ✅ `WS01` listed

![image](https://github.com/user-attachments/assets/a7642459-c65f-4d65-b86c-ae9c7adfb12c)

![image](https://github.com/user-attachments/assets/1d548daa-44a7-4759-910d-c1dba6517e81)

---
![image](https://github.com/user-attachments/assets/14df016c-f142-4233-9548-7b62222fd0f7)

### 🖥️ 1. Open Active Directory Users & Computers

On your **Domain Controller**:

```
Server Manager > Tools > Active Directory Users and Computers
```

Expand your domain:

```
lab.local
```

---

### 🗃️ 2. Create Organizational Units

Right-click on your domain >

```
New > Organizational Unit
```
![image](https://github.com/user-attachments/assets/14df016c-f142-4233-9548-7b62222fd0f7)

Create the following OUs:

- `Engineering`
- `Management`
- `IT`

![image](https://github.com/user-attachments/assets/016bb760-e479-44b7-94df-eef9797d56c0)

📂 Optional:  
Inside `IT`, create a **nested OU**:

- `Administrators`

---

### 👨‍💻 3. Move Users to the OUs

Drag and drop users into their respective departments:

|User|OU|
|---|---|
|Richard Hendricks|Engineering|
|Nelson Bighetti|Engineering|
|Erlich Bachman|Management|
|Jared Dunn|Management|
|Administrator|IT > Administrators|

![image](https://github.com/user-attachments/assets/1c370508-00be-446a-b76e-95fd915524cb)

![image](https://github.com/user-attachments/assets/47317f48-2f92-4f50-a903-ea82c2825855)

![image](https://github.com/user-attachments/assets/e74f4e9e-588e-4c18-90e8-7c35372bbf07)

Confirm the move when prompted ✅

---

### 🧱 4. Create a Security Group

Inside the `Engineering` OU:

1. Right-click > `New > Group`

![image](https://github.com/user-attachments/assets/06505108-f7d9-4421-8448-001b72e8b004)

2. Name: `Engineering Share`
3. Group Type: ✅ **Security**
4. Click OK

![image](https://github.com/user-attachments/assets/3b7fab61-4561-42f6-a63b-02ebe9c5921c)

---

### ➕ 5. Add Members to the Group

Double-click `Engineering Share` > go to **Members tab** > click **Add**

![image](https://github.com/user-attachments/assets/ccbfed9e-97bb-4a15-a91e-6b58930940b8)

- Add: `Richard`, `Nelson`, ✅ and also `Jared`  
    (Yes, he’s in Management, but needs access!)

![image](https://github.com/user-attachments/assets/500206dd-bc20-4fa2-b7a3-c5be9ad7f454)

Use **Check Names** to auto-complete entries.

![image](https://github.com/user-attachments/assets/9e3b3a9a-2253-4654-a182-27a4e941bde0)

![image](https://github.com/user-attachments/assets/149d1d24-c8b2-4ea1-9a34-616d8320c605)

✅ Click Apply > OK

---

### 📂 6. Create a Shared Folder on the Domain Controller

1. Go to:
```
Server Manager > File and Storage Services > Shares
```

![image](https://github.com/user-attachments/assets/f1405db2-6f0a-4941-8e76-cca686265396)

![image](https://github.com/user-attachments/assets/c77499bc-097f-4ec1-adaa-4fe264111edb)

2. Click **Tasks > New Share**

![image](https://github.com/user-attachments/assets/18a1ea8f-2911-4cfe-9de5-7bba1a1c2dcf)

3. Choose: `SMB Share - Quick`

![image](https://github.com/user-attachments/assets/6a6d8101-d565-45c8-a06e-c52075d78422)

### Share Settings:

| Setting        | Value               |
| -------------- | ------------------- |
| Share Location | `C:\`               |
| Share Name     | `Engineering Share` |
| Permissions    | Customized          |

![image](https://github.com/user-attachments/assets/de791b52-bc88-4735-a1f5-683c071f85d8)

![image](https://github.com/user-attachments/assets/6cd12ddb-a05a-4685-9b85-c6364526d9a2)

![image](https://github.com/user-attachments/assets/a4be59b3-402d-4aa3-94f5-e3406888eb5c)

![image](https://github.com/user-attachments/assets/dd42ba87-7528-46d3-bc77-24bb99614d70)

---

### 🛡️ 7. Configure Share Permissions

1. Click **Customize permissions**
2. Disable inheritance > Convert permissions

![image](https://github.com/user-attachments/assets/c7e93462-287e-448e-a999-a8736d155494)

3. Remove:
    - `Users`

![image](https://github.com/user-attachments/assets/5025ddc2-57d8-4256-82c5-cc768307a79e)

We remove them because that's going to give permission to everyone.

4. Keep:
    - `SYSTEM`
    - `Administrators`
    - `CREATOR OWNER`

5. Click on Add and Select a principal and then Add:
    - `Engineering Share` group  → **Allow**: `Read` & `Write`

![image](https://github.com/user-attachments/assets/d0683c7c-c702-48d3-8e37-9427f8bf6a2e)

![image](https://github.com/user-attachments/assets/336bfff0-f9b1-486c-83a4-5561086a9faf)

![image](https://github.com/user-attachments/assets/886e1426-dfee-429d-9766-d4415aff34e4)

![image](https://github.com/user-attachments/assets/91b88b60-7b78-4f30-9138-ae2e403c68de)

✅ Click OK → Next → Create

![image](https://github.com/user-attachments/assets/4298a128-9ab3-4b8f-b16a-fc0298089ce9)

---

## 💻 8. Test from the Windows 11 Workstation

---

### 👤 Login as `Jared Dunn`

1. Sign in as: `lab\jdunn`  
    Password: `P@ssword1!`

![image](https://github.com/user-attachments/assets/e1bf8c3c-726b-44ac-ac9b-8d70ca48b998)

2. Open **File Explorer** 
3. In the address bar:
```
\\dc01\Engineering Share
```

![image](https://github.com/user-attachments/assets/f2b20691-d60f-4ea9-81a4-df748fd8a7eb)

✅ Jared should have full access — test by creating a file or folder.

![image](https://github.com/user-attachments/assets/1733e56d-250b-466a-ac3a-d890910160e5)

![image](https://github.com/user-attachments/assets/4143e64c-0b6e-4d8c-b953-30e3eef6bdc6)

---

### 💾 (Optional) Map Network Drive

1. In **This PC**, right-click → **Map network drive**

![image](https://github.com/user-attachments/assets/c2157aa3-1aba-49aa-a073-e8fda6eca4d7)

2. Choose a letter (e.g., `Z:`)
3. Path:
```
\\dc01\Engineering Share
```
![image](https://github.com/user-attachments/assets/bb585d44-4900-4b55-af76-f6f51bfff62f)

Click **Finish** → The shared drive is now mounted as Z:\

![image](https://github.com/user-attachments/assets/f0013988-305a-405e-9c1c-682dc6239208)

### Test Access:

* Log in as Jared → `\\dc01\Engineering Share` → ✅ Can write
* Log in as Erlich → ❌ Access Denied

![image](https://github.com/user-attachments/assets/e87d97ca-e4a6-4b24-a2c1-d726b9ef7152)

![image](https://github.com/user-attachments/assets/5de5a8f4-9266-4309-80e6-8fb9fb2b2ce1)

![image](https://github.com/user-attachments/assets/81607f10-cad8-414a-9db4-ff80a47d8dd5)

📌 This demonstrates that **OU membership ≠ access rights**, while **group membership = permissions**.

---

## 🛠️ GPO: Set Desktop Wallpaper

### 🎨 Step 1: Create a Wallpaper File

1. Open **Paint** 🎨 on the **Domain Controller**

![image](https://github.com/user-attachments/assets/3e85b4d6-da6f-4482-a332-d644821b630a)

2. Resize canvas:
    - `1920 x 1080 px`
![image](https://github.com/user-attachments/assets/3a19d9f3-4de2-4325-88b8-7ede6976f17d)

![image](https://github.com/user-attachments/assets/52db8ebd-273c-4a79-8666-b1b55f293e63)

3. Add text: `Engineering Dept.`

![image](https://github.com/user-attachments/assets/43e0a000-b79b-4669-a3ad-69b19ae58120)

![image](https://github.com/user-attachments/assets/e119089e-d103-46b0-aba3-400f429f065b)

![image](https://github.com/user-attachments/assets/c4eef2b3-99ff-4091-8390-85bbda6128af)

4. Save as:
    - 📄 `Engineering_Wallpaper.jpg`
    - 📁 Location: **Desktop**

![image](https://github.com/user-attachments/assets/c17b9fa6-5571-4990-a2f3-014af834e22e)

![image](https://github.com/user-attachments/assets/178e80e2-e0cf-4635-9939-1d486d1aa9e8)

---

### 📂 Step 2: Move the Wallpaper to a Shared Folder

We need to store the image where **domain users can read it**.

1. Open:
```
Server Manager > File and Storage Services > Shares
```

![image](https://github.com/user-attachments/assets/fbf34d6b-ac42-4087-9987-deda9b69f5d1)

2. Right-click **NetLogon** → `Open Share`

![image](https://github.com/user-attachments/assets/93258f89-d466-481d-8231-334167ee93a2)

3. Copy the `Engineering_Wallpaper.jpg` into this folder

![image](https://github.com/user-attachments/assets/de6e05e5-4d5c-4df8-9956-05d190633a9c)

![image](https://github.com/user-attachments/assets/afaf47a8-ffb1-415b-ad24-dc0a9204ca36)

4. Hold **Shift** + Right-click the image → `Copy as path`

![image](https://github.com/user-attachments/assets/daee04a8-eee0-4d80-9337-394d2d2da56d)

✅ You now have the full UNC path (e.g. `\\dc01\netlogon\Engineering_Wallpaper.jpg`)

---

### 🧰 Step 3: Open Group Policy Management

1. Go to:
```
Server Manager > Tools > Group Policy Management
```

![image](https://github.com/user-attachments/assets/363f83e0-f12e-471f-927e-04d5fd585415)

2. Expand:
```
Forest > Domains > lab.local > Engineering
```

![image](https://github.com/user-attachments/assets/c533244c-b887-4b54-a8cf-981d7b418d8b)

3. Right-click `Engineering` OU →  
    Select:
```
Create a GPO in this domain, and Link it here…
```

![image](https://github.com/user-attachments/assets/04906c1f-ad7f-425c-aa32-2c1b568fd0fa)

4. Name the GPO:
```
Set Engineering Background
```
![[Pasted image 20250523140005.png]]

---

### 🎛️ Step 4: Configure the GPO

1. Right-click on the GPO → `Edit`
![[Pasted image 20250523140653.png]]
2. Navigate to:
```
User Configuration > Policies > Administrative Templates > Desktop > Desktop > Desktop Wallpaper
```
![[Pasted image 20250523140807.png]]
3. Double-click `Desktop Wallpaper` → Set to `Enabled`
![[Pasted image 20250523140838.png]]
4. Paste the path from NetLogon (🛑 Remove quotes)
```
\\dc01\netlogon\Engineering_Wallpaper.jpg
```
![[Pasted image 20250523140901.png]]
5. Apply → OK → Close GPO Editor

---

### 💻 Step 5: Test the GPO

#### 🔑 Log in as: `lab\rhendricks`

- Richard Hendricks is in the **Engineering OU**
- Enter password: `P@ssword1!`
![[Pasted image 20250523140945.png]]

✅ The wallpaper should update to the Engineering-themed background!
![[Pasted image 20250523140958.png]]

---

#### 🧪 Test with Non-Engineering User

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

