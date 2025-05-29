# 🛠️ Issue: DC DNS Forwarder Misconfiguration – No Internet Access in VirtualBox Lab

---

## ❌ Problem Summary

In a home lab using **VirtualBox** with a **NAT Network** (`10.0.2.0/24`), the following issues were happening:

- ✅ **Domain Controller** (DC) shows as connected but **can't access the internet**
- ❌ **Workstation** (joined to domain) shows **no internet**
- Error: `DNS_PROBE_FINISHED_BAD_CONFIG`

---

## ⚠️ Root Cause

- **Both VMs use static IPs**, so VirtualBox’s built-in DHCP no longer provides DNS.
- The **Domain Controller** had its DNS set to `127.0.0.1` (localhost) without any **forwarders** configured.
- The **Workstation** relies on the **DC for DNS**, but the DC couldn’t resolve anything externally.
- A broken forwarder (`10.0.2.3`) was set on the DC, which doesn't lead anywhere.

---

## ✅ How to Fix It – Step-by-Step

---

### 🔧 Step 1: Fix Forwarders on the Domain Controller (DC01)

1. Open **Server Manager** on the DC
2. Go to **Tools > DNS**
3. Right-click your server name (e.g., `DC01`) > **Properties**
4. Select the **Forwarders** tab
5. Click **Edit**
6. Remove any broken entry (like `10.0.2.3`)
7. Add public DNS servers:
    ```
    8.8.8.8    (Google)
    1.1.1.1    (Cloudflare)
    8.8.4.4    (Google backup)
    ```
8. Click **OK** > **Apply**

---

### 🧪 Step 2: Test on the Domain Controller

In Command Prompt or PowerShell:

```powershell
nslookup google.com
```

✅ If you get an IP address back, your forwarders are working!

---

### 🔧 Step 3: Verify Workstation Configuration

Ensure your **domain-joined workstation** is set up like this:

|Setting|Value|
|---|---|
|IP Address|`10.0.2.16`|
|Subnet Mask|`255.255.255.0`|
|Default Gateway|`10.0.2.1`|
|Preferred DNS|`10.0.2.15` (the DC)|
|Alternate DNS|_(Optional)_|

---

### 🧪 Step 4: Test on the Workstation

Open PowerShell or CMD:

```powershell
nslookup google.com
ping google.com
```

✅ If you get a valid IP and ping works — you're done!

---

## 💡 Alternative Network Options (If You Want More Flexibility)

- **Option 1:** Use **Google DNS** directly on both machines (`8.8.8.8`), but not ideal for domain labs.
- **Option 2:** Use **two network adapters** (one for internal domain, one for internet via NAT).
- **Option 3:** Use **Bridged Adapter** to put both VMs on your real LAN (best if DHCP is available).

---

## 🔁 Summary Table

|Machine|DNS Setting|Internet Access|Internal Domain Access|
|---|---|---|---|
|Domain Controller|`127.0.0.1` (with forwarders) ✅|✅ Yes|✅ Yes|
|Workstation|`10.0.2.15` (points to DC) ✅|✅ Yes (after fix)|✅ Yes|

---

## ✅ Final Result

- 🖥️ Both VMs have internet access
- 🌐 External websites like `google.com` resolve successfully
- 🧠 Internal DNS (`lab.local`) remains functional
- 🧩 Workstation uses DC as DNS — best practice for Active Directory

