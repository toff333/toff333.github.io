---
title: Password and Account Lockout
layout: default
parent: Windows Policies
grand_parent: OS Hardening
---

# Password and Account Lockout Policies

---

### Step-by-Step Guide:

1. **Open Local Group Policy Editor**:
    1. Press `Windows Key + R` to open the Run dialog.
    2. Type `gpedit.msc` and press Enter.

2. **Navigate to the Policy Settings**: In the Local Group Policy Editor, go to: `Computer Configuration -> Windows Settings -> Security Settings -> Account Policies`.

3. **Locate and Configure the Policies**:

   - **Disable convenience PIN sign-in**:
     1. Navigate to `Local Policies -> Security Options`.
     2. Find "Interactive logon: Require Windows Hello for Business or smart card" policy.
     3. Set it to "Enabled".

   - **Limit remembered passwords to 5**:
     1. Find "Interactive logon: Number of previous logons to cache (in case domain controller is not available)" policy.
     2. Set it to "5".

   - **Force user to change password every 90 days**:
     1. Find "Password Policy" under "Account Policies".
     2. Set "Maximum Password Age" to "90 days".

   - **A user can only change their password after 24 hours**:
     1. Find "Password Policy" under "Account Policies".
     2. Set "Minimum Password Age" to "1 day".

   - **Set minimum password length to 10 characters**:
     1. Find "Password Policy" under "Account Policies".
     2. Set "Minimum Password Length" to "10".

   - **Passwords must meet complexity requirements**:
     1. Find "Password must meet complexity requirements" under "Password Policy".
     2. Set it to "Enabled".

   - **Disable reversible encryption for passwords**:
     1. Find "Accounts: Limit local account use of blank passwords to console logon only" under "Account Policies".
     2. Set it to "Disabled".

   - **Set a maximum of 5 failed logon attempts**:
     1. Find "Account Lockout Policy" under "Account Policies".
     2. Set "Account lockout threshold" to "5".

   - **Reset account lockout after 15 minutes**: Set "Reset account lockout counter after" to "15 minutes".

4. **Apply the Policies**: Once configured, close the Local Group Policy Editor.

These settings will apply to the local computer's security policy. If you're managing multiple computers, consider using Group Policy in a domain environment for centralized management. Ensure you have appropriate administrative privileges to make these changes.