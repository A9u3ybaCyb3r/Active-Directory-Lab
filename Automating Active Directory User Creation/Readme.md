# ⚙️ PowerShell Script: Active Directory User Creator 👤

This tool is a **PowerShell script** that automatically creates new users in **Active Directory (AD)**.

Instead of adding users manually through the AD interface, this script lets you **create a user with just one command**. It takes inputs like first name, last name, username, OU (organizational unit), and domain, then:

* Generates a secure, random password 🔐
* Creates the AD user with all the right settings ✅
* Sets the user to change their password on first login 🔁

---

### 🎯 What It Solves

Creating users by hand is slow and prone to mistakes—especially when you have to set up many accounts at once. This script:

* **Saves time**
* **Prevents typos and misconfigurations**
* **Standardizes new user setup**

---

### 🚀 How To Use It

1. Open **Visual Studio Code**
2. Save the script as `Create-ADUser.ps1`
3. Run it from the terminal with your user info:

```powershell
.\Create-ADUser.ps1 `
  -FirstName "Alex" `
  -LastName "Bellini" `
  -UserName "abellini" `
  -OU "Engineering" `
  -Domain "lab.local"
```

That’s it—your AD user is created and ready to log in!
