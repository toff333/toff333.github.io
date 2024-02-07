---
title: Application Control
layout: default
parent: Windows Policies
grand_parent: OS Hardening
---

# Application Control Policies

---

### Step-by-Step Guide:

1. **Open Local Group Policy Editor**:
    1. Press `Windows Key + R` to open the Run dialog.
    2. Type `gpedit.msc` and press Enter.

2. **Locate and Configure the Policy**:
   
   Look for below policies under:

   - `Computer Configuration\Policies\Administrative Templates\Windows Components\File Explorer\Configure Windows Defender SmartScreen` to `Enabled` and select `Warn and prevent bypass`
   - `Computer Configuration\Policies\Administrative Templates\Windows Components\Windows Defender SmartScreen\Explorer\Configure Windows Defender SmartScreen` to `Enabled` and select `Warn and prevent bypass`
   - `Computer Configuration\Policies\Administrative Templates\Windows Components\Windows Installer\Allow user control over installs` to `Disabled`
   - `Computer Configuration\Policies\Administrative Templates\Windows Components\Windows Installer\Always install with elevated privileges` to `Disabled`
   - `User Configuration\Policies\Administrative Templates\Windows Components\Windows Installer\Always install with elevated privileges` to `Disabled`

3. **Apply the Policy**: Once configured, close the Local Group Policy Editor.

The policy will be applied to the local computer upon closing the Local Group Policy Editor. If you are managing multiple computers within a domain, you can use Group Policy Management Console (GPMC) to apply this policy across multiple computers.
