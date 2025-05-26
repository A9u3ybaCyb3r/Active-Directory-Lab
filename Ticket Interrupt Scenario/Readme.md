# 🎫 Ticket Interrupt: Lock Desktop Background via GPO

## 📚 Table of Contents

* [📋 Ticket Summary](#-ticket-summary)
* [🧠 Solution Overview](#-solution-overview)
* [🧰 Step-by-Step Implementation](#-step-by-step-implementation)

  * [🧭 Step 1: Open Group Policy Management](#-step-1-open-group-policy-management)
  * [📦 Step 2: Create and Link a New GPO](#-step-2-create-and-link-a-new-gpo)
  * [⚙️ Step 3: Edit the GPO](#-step-3-edit-the-gpo)
  * [🔁 Step 4: Test the Policy](#-step-4-test-the-policy)
  * [🎨 Step 5: Attempt to Change Background](#-step-5-attempt-to-change-background)
* [✅ Result](#-result)
* [🔑 Key Takeaways](#-key-takeaways)
* [🧪 Next Steps](#-next-steps)

## 📋 Ticket Summary

> 🧑‍💼 Engineering Manager:
> “Thanks for setting the desktop background image for my team. But some users are changing it. Can you prevent this from happening — **without affecting other departments**?”

✅ **Goal:** Prevent only **Engineering** users from changing their desktop wallpaper.

---

## 🧠 Solution Overview

To solve this:

* 🔒 Create a **new GPO** linked only to the **Engineering OU**
* 🖼️ Use the setting: `Prevent changing desktop background`
* 🔁 Test the policy on a Windows 11 machine with an Engineering user

---

## 🧰 Step-by-Step Implementation

### 🧭 Step 1: Open Group Policy Management

On the **Domain Controller**:

1. Open:
   `Server Manager > Tools > Group Policy Management`
2. Expand:
   `Forest > Domains > lab.local > Engineering`

---

### 📦 Step 2: Create and Link a New GPO

1. Right-click `Engineering` OU →
   Select: `Create a GPO in this domain, and Link it here…`
2. Name the GPO:
   `Lock Desktop`

✅ This ensures only users in the Engineering OU are affected.

---

### ⚙️ Step 3: Edit the GPO

1. Right-click `Lock Desktop` → `Edit`
2. Navigate to:

   ```
   User Configuration > Policies > Administrative Templates > Control Panel > Personalization
   ```
3. Double-click:

   ```
   Prevent changing desktop background
   ```
4. Set to: `Enabled`
5. Click **Apply** → **OK**

---

### 🔁 Step 4: Test the Policy

#### 👤 Login as: `lab\rhendricks`

1. On the **Windows 11 workstation**
2. Log in with:

   * Username: `rhendricks`
   * Password: `P@ssword1!`

You should see the **Engineering desktop wallpaper** set earlier.

---

### 🎨 Step 5: Attempt to Change Background

1. Right-click on the **desktop**
2. Choose **Personalize**
3. Click **Background**

❌ You’ll see:

> *“Some settings are managed by your organization”*
> 🔒 The background settings are grayed out and **cannot be changed**

---

## ✅ Result

| User              | OU          | Wallpaper Locked? |
| ----------------- | ----------- | ----------------- |
| Richard Hendricks | Engineering | ✅ Yes             |
| Erlich Bachman    | Management  | ❌ No              |

🎯 This proves the GPO was successfully applied **only to Engineering**, meeting the manager’s request.

---

## 🔑 Key Takeaways

* ✅ Always **scope your GPOs** properly — don’t apply domain-wide if not required
* 🛠️ Setting:

  ```
  Prevent changing desktop background
  ```

  is found under:

  ```
  User Configuration > Policies > Administrative Templates > Control Panel > Personalization
  ```
* 🛡️ GPOs provide granular control over user environments across an org

---

## 🧪 Next Steps

Want to extend your lab?

* 🔒 Block Control Panel or PowerShell
* 📛 Set user login banners
* 🕒 Configure lock screen timeout
* 🛑 Disable USB storage access

Let me know and I’ll help you build the GPOs for those too! 💼🖥️
