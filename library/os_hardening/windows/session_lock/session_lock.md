---
title: Session Lock
layout: default
parent: Windows Policies
grand_parent: OS Hardening
---

# Session Lock Policy

This sets a policy to lock the machine after X seconds.

---

### Step-by-Step Guide:

1. **Open Group Policy Management Console (GPMC)**:
   1. Press `Windows Key + R` to open the Run dialog.
   2. Type `gpmc.msc` and press Enter.

2. **Navigate to the Group Policy Object**:
   1. In the left pane of the Group Policy Management Console, expand your domain.
   2. Right-click on the Organizational Unit (OU) or the domain itself where you want to apply the policy.
   3. Select "Create a GPO in this domain, and Link it here..." to create a new Group Policy Object (GPO), or select an existing GPO.

3. **Edit the Group Policy Object**: Right-click on the GPO you've selected and choose "Edit".

4. **Locate the Policy Setting**:
   1. In the Group Policy Management Editor, navigate to the following path:
   `Computer Configuration -> Policies -> Windows Settings -> Security Settings -> Local Policies -> Security Options`
   2. Look for the policy named "Interactive logon: Machine inactivity limit".

5. **Configure the Policy**:
   1. Double-click on the policy to open its properties.
   2. Enable the policy and set the desired inactivity limit (in seconds) according to your requirements.

6. **Apply the Policy**:
   1. Once configured, close the Group Policy Management Editor.
   2. The policy will be applied to the computers in the selected OU during the next Group Policy refresh.

The policy will be applied to the local computer upon closing the Local Group Policy Editor. If you are managing multiple computers within a domain, you can use Group Policy Management Console (GPMC) to apply this policy across multiple computers.