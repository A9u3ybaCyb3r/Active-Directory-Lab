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

![image](https://github.com/user-attachments/assets/ffb26dca-9180-4d2a-9b65-389ba0362643)

2. Expand:
   `Forest > Domains > lab.local > Engineering`

![image](https://github.com/user-attachments/assets/b8a67f59-469e-4cb6-901a-813bf57dced8)

---

### 📦 Step 2: Create and Link a New GPO

1. Right-click `Engineering` OU →
   Select: `Create a GPO in this domain, and Link it here…`

![image](https://github.com/user-attachments/assets/657c6552-b393-48ff-a848-18f17b9ef0f7)

2. Name the GPO:
   `Lock Desktop`

![image](https://github.com/user-attachments/assets/90bb7611-34a6-4d8c-89ea-b7ed4146c2d2)

✅ This ensures only users in the Engineering OU are affected.

---

### ⚙️ Step 3: Edit the GPO

1. Right-click `Lock Desktop` → `Edit`

![image](https://github.com/user-attachments/assets/7fc1a0d3-d4d4-4768-a17a-425520176a15)

2. Navigate to:

   ```
   User Configuration > Policies > Administrative Templates > Control Panel > Personalization
   ```

![image](https://github.com/user-attachments/assets/411954c1-b2e4-4906-b2ab-f0029f9dd561)

3. Double-click:

   ```
   Prevent changing desktop background
   ```

![image](https://github.com/user-attachments/assets/c4e15e4f-d0ea-440b-83e1-c21ad81011d3)

4. Set to: `Enabled`

![image](https://github.com/user-attachments/assets/9e508d4c-a5e0-4b2c-bd58-d1b40b440331)

5. Click **Apply** → **OK**

---

### 🔁 Step 4: Test the Policy

#### 👤 Login as: `lab\rhendricks`

1. On the **Windows 11 workstation**
2. Log in with:

   * Username: `rhendricks`
   * Password: `P@ssword1!`

![image](https://github.com/user-attachments/assets/7324b043-f50f-4dae-805b-2c783297f6d4)

You should see the **Engineering desktop wallpaper** set earlier.

---

### 🎨 Step 5: Attempt to Change Background

1. Right-click on the **desktop**
2. Choose **Personalize**

![image](https://github.com/user-attachments/assets/619a4c3a-c1c7-40c4-a8b8-730172f7db7c)

3. Click **Background**

![image](https://github.com/user-attachments/assets/1e2c14a9-0ab0-4b0d-b142-ae3b306d6bbe)

❌ You’ll see:

> *“Some settings are managed by your organization”*
> 🔒 The background settings are grayed out and **cannot be changed**

![image](https://github.com/user-attachments/assets/6055e97d-db64-4a7f-9a7e-44eba362bcbf)

---

## ✅ Result

| User              | OU          | Wallpaper Locked? |
| ----------------- | ----------- | ----------------- |
| Richard Hendricks | Engineering | ✅ Yes             |
| Erlich Bachman    | Management  | ❌ No              |

🎯 This proves the GPO was successfully applied **only to Engineering**, meeting the manager’s request.
