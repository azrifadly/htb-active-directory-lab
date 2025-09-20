
Created a function to create the users as well as set the following attributes

![image alt[Screenshot 2025-09-11 at 8.03.21 PM.png]]

Moved the users to the correct OU (Corp > Employees > HQ-NYC > IT)

![[Screenshot 2025-09-11 at 8.05.32 PM.png]]

Unlocking and resetting of password for Adam Masters account

![[Screenshot 2025-09-11 at 8.11.17 PM.png]]

Creating a new OU within PowerShell

![[Screenshot 2025-09-11 at 8.30.27 PM.png]]

Moving these 3 newly created users into "Security Analysts"

![[Screenshot 2025-09-11 at 8.30.54 PM.png]]

![[Screenshot 2025-09-11 at 8.32.44 PM.png]]

Copying existing GPO "Logon Banner" and naming it "Security Analysts Control"
Then linking it to Security Analysts OU

![[Screenshot 2025-09-11 at 9.08.25 PM.png]]

Here in the Group Policy Management Editor is where we enforce the rules for password


![[Screenshot 2025-09-11 at 9.03.48 PM.png]]
![[Screenshot 2025-09-11 at 9.05.34 PM.png]]
- We need to modify the removable media settings and ensure they are set to block any removable media from access. We will expressly allow security analysts to access PowerShell and CMD since their daily duties require it.
    
    - location of removable media policy settings = `User Configuration > Policies > Administrative Templates > System > Removable Storage Access.`
    - Location of Command Prompt settings = `User Configuration > Policies > Administrative Templates > System.`

- For `Computer settings`, we need to ensure the Logon Banner is applied and that the password policy settings for this group are strengthened.
    
    - Location of Logon Banner settings = `Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > Security Options.`
    - For reference, this setting should already be enabled since the GPO we copied was for a Logon Banner. We are validating the settings and ensuring it is enabled and applied.
    - Location of Password Policy settings = `Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy.`


