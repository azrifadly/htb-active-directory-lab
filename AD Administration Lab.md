# Active Directory Configuration Tasks

## User Management

### Creating User Accounts
Created a function to create users with the following attributes:

![alt text](Screenshot%202025-09-11%20at%208.03.21%20PM.png)

### Moving Users to Organizational Units
Moved the users to the correct OU: **Corp > Employees > HQ-NYC > IT**

![alt text](Screenshot%202025-09-11%20at%208.05.32%20PM.png)

### Account Administration
Unlocked and reset password for Adam Masters account:

![alt text](Screenshot%202025-09-11%20at%208.11.17%20PM.png)

## Organizational Unit Management

### Creating New OU
Created a new OU using PowerShell:

![alt text](Screenshot%202025-09-11%20at%208.30.27%20PM.png)

### User Assignment
Moved 3 newly created users into the **Security Analysts** OU:

![alt text](Screenshot%202025-09-11%20at%208.30.54%20PM.png)

![alt text](Screenshot%202025-09-11%20at%208.32.44%20PM.png)

## Group Policy Configuration

### GPO Creation and Linking
Copied existing GPO "Logon Banner" and renamed it to **"Security Analysts Control"**, then linked it to the Security Analysts OU:

![alt text](Screenshot%202025-09-11%20at%209.08.25%20PM.png)

### Password Policy Configuration
Configured password rules in the Group Policy Management Editor:

![alt text](Screenshot%202025-09-11%20at%209.03.48%20PM.png) ![alt text](Screenshot%202025-09-11%20at%209.05.34%20PM.png)

## Policy Configuration Requirements

### User Configuration Settings

**Removable Media Restrictions:**
- Block all removable media access
- Allow PowerShell and CMD access for Security Analysts (required for daily duties)
- **Location:** `User Configuration > Policies > Administrative Templates > System > Removable Storage Access`

**Command Prompt Settings:**
- **Location:** `User Configuration > Policies > Administrative Templates > System`

### Computer Configuration Settings

**Logon Banner:**
- Ensure banner is applied and enabled
- **Location:** `Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > Security Options`
- **Note:** Should already be enabled since we copied from existing Logon Banner GPO

**Password Policy:**
- Strengthen password requirements for Security Analysts group
- **Location:** `Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy`
