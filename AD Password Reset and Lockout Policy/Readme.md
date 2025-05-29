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

![image](https://github.com/user-attachments/assets/d8a703b5-3137-4f31-a127-33c69498fba6)

2. Right-click `lab.local` → Create GPO → Name: `Account Lockout Policy`

![image](https://github.com/user-attachments/assets/49d49a50-6d7a-4db8-967d-e94260e7a42f)

![image](https://github.com/user-attachments/assets/0baa3443-a023-47a3-8063-177255dd1e68)

3. Edit GPO:

   * Path:
     `Computer Configuration → Policies → Windows Settings → Security Settings → Account Policies → Account Lockout Policy`

    ![image](https://github.com/user-attachments/assets/01af94d8-c760-40f3-aa3b-03affaaef17d)

    ![image](https://github.com/user-attachments/assets/cd185905-8541-4372-ad38-91ca0e99fb00)

    * Set:

     * `Account lockout threshold` → `3`

     ![image](https://github.com/user-attachments/assets/bd3907cd-867d-4482-a51f-2adb2d74e2f1)

     * Lockout Duration → 30 minutes
     * Reset Counter → 30 minutes

    ![image](https://github.com/user-attachments/assets/a491e9a4-676c-40dc-8dde-ec4655ad4d34)

5. Right-click the GPO → Enforce

![image](https://github.com/user-attachments/assets/42b791b3-a490-4549-bf73-2b5999e773c0)

✅ After 3 failed logins, the account is locked.

---

## ❌ Step 2: Trigger Account Lockout

1. On the Windows 11 workstation, login as `R.Hendricks`
2. Enter the wrong password 3 times

**Result:**

> “The referenced account is currently locked out and may not be logged on to.”

![image](https://github.com/user-attachments/assets/78cb8e37-5392-4f4f-8584-404e7f7a2404)

---

## 🔐 Step 3: Unlock and Reset User Password (GUI)

1. Open Active Directory Users and Computers (ADUC)

![image](https://github.com/user-attachments/assets/756361dd-94e9-4d69-9f15-6b207004994a)

2. Search for `R.Hendricks`

![image](https://github.com/user-attachments/assets/5213a191-9659-4aec-b65d-960a8e727c53)

![image](https://github.com/user-attachments/assets/a0dd15bb-a4e7-42a1-9a69-bd9c81447c62)

3. Right-click → Reset Password → Enter new password: `ResetMe1!`

![image](https://github.com/user-attachments/assets/01c0397f-ce1f-4ed9-bef7-037c3c33f2e3)

4. Check:

   * ✅ Unlock the account
   * ✅ User must change password at next login

![image](https://github.com/user-attachments/assets/b3411757-27d9-483d-a219-c000ff2134ab)

*Note: If the password change option is grayed out, uncheck "Password never expires" in Account tab.*

![image](https://github.com/user-attachments/assets/ceea0c3b-1954-4d25-a19e-4a9ae58c41f2)

![image](https://github.com/user-attachments/assets/c206eaf1-c231-408c-8aec-7e48baa1ceed)

![image](https://github.com/user-attachments/assets/095573fd-70eb-4559-9f2f-05f7e6338283)

![image](https://github.com/user-attachments/assets/d6bdb830-c460-46a9-be4d-28161d2dd875)

---

## 🧪 Step 4: User Changes Password (Windows 11)

1. Login as `R.Hendricks` on workstation
2. Enter `ResetMe1!` → Prompted to change password

![image](https://github.com/user-attachments/assets/f80360f7-e780-4571-9db3-6133dda2c87e)

![image](https://github.com/user-attachments/assets/12f6c2e6-ed00-40e0-8d4c-8f7990641e0c)

3. Set new password: `P@ssw0rd!`

![image](https://github.com/user-attachments/assets/4947ef36-8153-47a6-9222-532dbb83bd57)

✅ User logs in successfully.

---

## 💻 Step 5: PowerShell Method for Reset & Expire

### 🔁 Reset Password:

```powershell
Set-ADAccountPassword -Identity rhendricks -Reset -NewPassword (ConvertTo-SecureString "ResetMe1!" -AsPlainText -Force)
```
Or
```powershell
Set-ADACcountPassword -Identity rhendricks -reset
```

![image](https://github.com/user-attachments/assets/f36aa935-86ee-4fb2-907b-f8ef776ec99c)

### 📌 Force Password Change on Next Login:

```powershell
Set-ADUser -Identity rhendricks -ChangePasswordAtLogon $true
```

![image](https://github.com/user-attachments/assets/0312532d-b52f-42cd-9db7-a856e1cfd2a5)

### 🔍 Verify Password Change Timestamp:

```powershell
Get-ADUser rhendricks -Properties * | select name, pass*
```

![image](https://github.com/user-attachments/assets/9d4543f5-74d9-4d64-beef-9f5ca96c9bac)

![image](https://github.com/user-attachments/assets/0779cd9c-8bfe-4a65-a408-9280f3ea70e2)

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

## **Skills Demonstrated**:

* GPO policy configuration
* Password reset workflows
* PowerShell AD automation
* Real-world IT support practice

