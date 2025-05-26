# 🔐 Active Directory Lab: Password Reset & Account Lockout Handling

## 📚 Table of Contents

* [🎯 Objective](#-objective)
* [🖥️ Lab Environment](#️-lab-environment)
* [🔧 Step 1: Configure Account Lockout Policy](#-step-1-configure-account-lockout-policy)
* [❌ Step 2: Trigger Account Lockout](#-step-2-trigger-account-lockout)
* [🔐 Step 3: Unlock and Reset User Password (GUI)](#-step-3-unlock-and-reset-user-password-gui)
* [🧪 Step 4: User Changes Password (Windows 11)](#-step-4-user-changes-password-windows-11)
* [💻 Step 5: PowerShell Method for Reset & Expire](#-step-5-powershell-method-for-reset--expire)
* [🧰 Tools Used](#-tools-used)
* [✅ Summary](#-summary)
* [📁 Notes for Portfolio](#-notes-for-portfolio)

---

## 🎯 Objective

Learn how to:

* Configure **account lockout policies** via GPO
* Lock a user account through repeated login failures
* **Reset and unlock user accounts** using both GUI and PowerShell
* Enforce password change on next login

---

## 🖥️ Lab Environment

| Component         | Configuration                          |
| ----------------- | -------------------------------------- |
| Domain Controller | `DC01.lab.local` – Windows Server 2022 |
| Workstation       | Windows 11 – Domain-joined             |
| Domain            | `lab.local`                            |
| Test User         | `R.Hendricks` (Engineering OU)         |

---

## 🔧 Step 1: Configure Account Lockout Policy

### 📍 GPO Setup

1. Server Manager → Tools → Group Policy Management
2. Right-click `lab.local` → Create GPO → Name: `Account Lockout Policy`
3. Edit GPO:

   * Path:
     `Computer Configuration → Policies → Windows Settings → Security Settings → Account Policies → Account Lockout Policy`
   * Set:

     * `Account lockout threshold` → `3`
     * Lockout Duration → 30 minutes
     * Reset Counter → 30 minutes
4. Right-click the GPO → Enforce

✅ After 3 failed logins, the account is locked.

---

## ❌ Step 2: Trigger Account Lockout

1. On the Windows 11 workstation, login as `R.Hendricks`
2. Enter the wrong password 3 times

**Result:**

> “The referenced account is currently locked out and may not be logged on to.”

---

## 🔐 Step 3: Unlock and Reset User Password (GUI)

1. Open Active Directory Users and Computers (ADUC)
2. Search for `R.Hendricks`
3. Right-click → Reset Password → Enter new password: `ResetMe1!`
4. Check:

   * ✅ Unlock the account
   * ✅ User must change password at next login

*Note: If the password change option is grayed out, uncheck "Password never expires" in Account tab.*

---

## 🧪 Step 4: User Changes Password (Windows 11)

1. Login as `R.Hendricks` on workstation
2. Enter `ResetMe1!` → Prompted to change password
3. Set new password: `P@ssw0rd!`

✅ User logs in successfully.

---

## 💻 Step 5: PowerShell Method for Reset & Expire

### 🔁 Reset Password:

```powershell
Set-ADAccountPassword -Identity rhendricks -Reset -NewPassword (ConvertTo-SecureString "ResetMe1!" -AsPlainText -Force)
```

### 📌 Force Password Change on Next Login:

```powershell
Set-ADUser -Identity rhendricks -ChangePasswordAtLogon $true
```

### 🔍 Verify Password Change Timestamp:

```powershell
Get-ADUser rhendricks -Properties * | select name, pass*
```

---

## 🧰 Tools Used

| Tool                | Purpose                           |
| ------------------- | --------------------------------- |
| Group Policy Editor | Set lockout thresholds            |
| ADUC (GUI)          | Reset password and unlock account |
| PowerShell Cmdlets  | Automate user reset               |

Key Cmdlets:

* `Set-ADAccountPassword`
* `Set-ADUser -ChangePasswordAtLogon`
* `Get-ADUser -Properties *`

---

## ✅ Summary

| Task                        | GUI | PowerShell |
| --------------------------- | --- | ---------- |
| Set lockout threshold       | ✅   | ❌          |
| Unlock & reset password     | ✅   | ✅          |
| Enforce password change     | ✅   | ✅          |
| View password last set time | ❌   | ✅          |

---

## 📁 Notes for Portfolio

**Lab Name**: `AD Password Reset and Lockout Policy`

**Skills Demonstrated**:

* GPO policy configuration
* Password reset workflows
* PowerShell AD automation
* Real-world IT support practice

---
