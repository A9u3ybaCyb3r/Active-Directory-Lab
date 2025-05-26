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
