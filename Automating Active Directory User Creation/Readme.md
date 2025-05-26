# ⚙️ PowerShell Script Guide: Automating Active Directory User Creation 👤✨

Welcome to this hands-on PowerShell scripting lesson! In this guide, we’ll walk you through the process of **automating the creation of an Active Directory (AD) user** using a custom PowerShell script. You'll write, run, and troubleshoot the script entirely in **Visual Studio Code**, using best practices in syntax, parameter handling, password generation, and secure user onboarding.

---

## 📚 Table of Contents

* [🧑‍💻 Step 1: Setting Up Your Workspace](#-step-1-setting-up-your-workspace)
* [📄 Step 2: Create the Script File](#-step-2-create-the-script-file)
* [✍️ Step 3: Script Overview & Structure](#-step-3-script-overview--structure)
* [🎛️ Step 4: Accepting User Parameters](#-step-4-accepting-user-parameters)
* [🔐 Step 5: Generate a Secure Random Password](#-step-5-generate-a-secure-random-password)
* [🧩 Step 6: Create the Active Directory User](#-step-6-create-the-active-directory-user)
* [🚦 Step 7: Running the Script in VS Code Terminal](#-step-7-running-the-script-in-vs-code-terminal)
* [🧪 Step 8: Troubleshooting and Verification](#-step-8-troubleshooting-and-verification)
* [🎯 Bonus: Expand the Script with Group Membership](#-bonus-expand-the-script-with-group-membership)
* [⚙️ How It Works](#-how-it-works)
* [📌 Final Output Example](#-final-output-example)
* [📜 Full Script](#-full-script)
* [✅ Skills Demonstrated](#-skills-demonstrated)
* [📚 Next Steps](#-next-steps)

---

## 🧑‍💻 Step 1: Setting Up Your Workspace

1. Install Visual Studio Code from the Microsoft Store
2. Launch it and install the PowerShell extension for syntax highlighting

## 📄 Step 2: Create the Script File

Create a new `.ps1` file named `Create-ADUser.ps1` and save it on your Desktop.

## ✍️ Step 3: Script Overview & Structure

Start with a `param()` block to handle inputs, generate a secure password, and create a new user with `New-ADUser`.

## 🎛️ Step 4: Accepting User Parameters

Use PowerShell's `param()` block to collect:

* First Name
* Last Name
* Username
* Organizational Unit
* Domain

## 🔐 Step 5: Generate a Secure Random Password

Use ASCII character ranges and `Get-Random` to create a 12-character password, convert it to a `SecureString`.

## 🧩 Step 6: Create the Active Directory User

Use `New-ADUser` with the supplied parameters and generated password to create the new AD user.

## 🚦 Step 7: Running the Script in VS Code Terminal

From the VS Code terminal:

```powershell
cd Desktop
.\Create-ADUser.ps1 -FirstName "Alex" -LastName "Bellini" -UserName "abellini" -OU "engineering" -Domain "lab.local"
```

## 🧪 Step 8: Troubleshooting and Verification

Use `Get-ADUser` to confirm the user was created. Check errors related to string conversion or syntax.

## 🎯 Bonus: Expand the Script with Group Membership

Use `Add-ADGroupMember` and add an optional `GroupName` parameter.

## ⚙️ How It Works

* `param()` block collects input
* Password is generated securely and converted
* User is created with `New-ADUser`

## 📌 Final Output Example

```powershell
Password Generated as: Xyz789KlmPQ2
```

## 📜 Full Script

A complete working version is included, with a fallback variation.

## ✅ Skills Demonstrated

| Skill                          | ✅ |
| ------------------------------ | - |
| PowerShell scripting           | ✅ |
| AD user management             | ✅ |
| Secure password handling       | ✅ |
| Use of `param()` and `cmdlets` | ✅ |
| Troubleshooting + testing      | ✅ |

## 📚 Next Steps

Build scripts that integrate:

* Exchange
* Teams
* Group Policy

You're now equipped to automate AD onboarding like a pro! 🚀
