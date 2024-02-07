---
title: Windows Update / Patching
layout: default
parent: Windows Policies
grand_parent: OS Hardening
---

# Windows Update / Patching Policies

---

### Step-by-Step Guide:

1. **Open Local Group Policy Editor**:
    1. Press `Windows Key + R` to open the Run dialog.
    2. Type `gpedit.msc` and press Enter.

2. **Navigate to the Policy Setting**: `Computer Configuration -> Policies -> Administrative Templates -> Windows Components -> Microsoft Edge`

3. **Locate and Configure the Policy**:

    Look for below policies:

    - `Allow Adobe Flash` to `Disabled`
    - `Allow Developer Tools` to `Disabled`
    - `Configure Do Not Track` to `Enabled`
    - `Configure Password Manager` to `Disabled`
    - `Configure Pop-up Blocker` to `Enabled`
    - `Configure Windows Defender SmartScreen` to `Enabled`
    - `Prevent access to the about:flags page in Microsoft Edge` to `Enabled`
    - `Prevent bypassing Windows Defender SmartScreen prompts for files` to `Enabled`
    - `Prevent users and apps from accessing dangerous websites` to `Enabled` and `Block`


4. **Apply the Policy**: Once configured, close the Local Group Policy Editor.

The policy will be applied to the local computer upon closing the Local Group Policy Editor. If you are managing multiple computers within a domain, you can use Group Policy Management Console (GPMC) to apply this policy across multiple computers.
