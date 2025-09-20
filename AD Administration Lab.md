
Created a function to create the users as well as set the following attributes

![alt text](Screenshot%202025-09-11%20at%208.03.21%20PM.png)

Moved the users to the correct OU (Corp > Employees > HQ-NYC > IT)
![alt text](Screenshot%202025-09-11%20at%208.05.32%20PM.png)
Unlocking and resetting of password for Adam Masters account
![alt text](Screenshot%202025-09-11%20at%208.11.17%20PM.png)
Creating a new OU within PowerShell
![alt text](Screenshot%202025-09-11%20at%208.30.27%20PM.png)
Moving these 3 newly created users into "Security Analysts"
![alt text](Screenshot%202025-09-11%20at%208.30.54%20PM.png)
![alt text](Screenshot%202025-09-11%20at%208.32.44%20PM.png)
Copying existing GPO "Logon Banner" and naming it "Security Analysts Control" Then linking it to Security Analysts OU
![alt text](Screenshot%202025-09-11%20at%209.08.25%20PM.png)
Here in the Group Policy Management Editor is where we enforce the rules for password
![alt text](Screenshot%202025-09-11%20at%209.03.48%20PM.png) ![alt text](Screenshot%202025-09-11%20at%209.05.34%20PM.png)
* We need to modify the removable media settings and ensure they are set to block any removable media from access. We will expressly allow security analysts to access PowerShell and CMD since their daily duties require it.
   * location of removable media policy settings = `User Configuration > Policies > Administrative Templates > System > Removable Storage Access.`
   * Location of Command Prompt settings = `User Configuration > Policies > Administrative Templates > System.`
* For `Computer settings`, we need to ensure the Logon Banner is applied and that the password policy settings for this group are strengthened.
   * Location of Logon Banner settings = `Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > Security Options.`
   * For reference, this setting should already be enabled since the GPO we copied was for a Logon Banner. We are validating the settings and ensuring it is enabled and applied.
   * Location of Password Policy settings = `Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy.`

