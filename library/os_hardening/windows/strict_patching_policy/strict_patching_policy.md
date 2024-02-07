---
title: Microsoft Edge
layout: default
parent: Windows Policies
grand_parent: OS Hardening
---

# Microsoft Edge Policies

---

### Step-by-Step Guide:

1. **Open Local Group Policy Editor**:
    1. Press `Windows Key + R` to open the Run dialog.
    2. Type `gpedit.msc` and press Enter.

2. **Locate and Configure the Policy**:

    Look for below policies under `Computer Configuration -> Policies -> Administrative Templates -> Windows Components -> Windows Update`:

   - `Allow Automatic Updates immediate installation` to `Enabled`
   - `Configure Automatic Updates` to `Enabled`
   - `Do not include drivers with Windows Updates` to `Disabled`
   - `No auto-restart with logged on users for scheduled automatic updates installations` to `Enabled`
   - `Remove access to use all Windows Update features` to `Disabled`
   - `Turn on recommended updates via Automatic Updates` to `Enabled`

3. **Apply the Policy**: Once configured, close the Local Group Policy Editor.

The policy will be applied to the local computer upon closing the Local Group Policy Editor. If you are managing multiple computers within a domain, you can use Group Policy Management Console (GPMC) to apply this policy across multiple computers.
