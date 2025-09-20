# AD Administration: Guided Lab Part I

## Overview

This lab serves as a hands-on experience in Active Directory administration for Inlanefreight. We will be acting as domain administrators to help the IT department close work orders by performing various administrative tasks including user and group management, group policy configuration, and more.

**Objective:** Successfully complete assigned tasks to potentially earn a promotion to the Tier II IT team from the helpdesk.

## Lab Scenario

### Help Desk Request from Bucky Barnes

**From:** Bucky Barnes (CISSP, IT Team Lead, Inlanefreight LLC)  
**Date:** Thu 1/6/2022 9:25 AM  
**To:** Helpdesk

**Subject:** We Could Use A Bit Of Help...

Our normal admin staff is swamped after our last audit of the enterprise. We need assistance with the following tasks:

### Required Tasks:
- **Add new hires:** Several employees start Monday and need accounts ready
- **Remove inactive users:** Clean up old inactive user and computer objects found during audit
- **Unlock account:** Adam Masters locked himself out again (see trouble ticket)
- **Create Security Group:** New Security Group for analysts with corresponding OU and PCs
- **Domain integration:** Add new-hire computers to domain and validate correct OU placement
- **Group Policy:** Create and apply new Group Policy for Analyst users
- **DNS validation:** Validate DNS records for Host (Sharepoint02.inlanefreight.local)

## Connection Instructions

### Lab Environment
- **Platform:** Domain-joined Windows server
- **Access Method:** RDP via Pwnbox or personal VM over VPN
- **Target Host:** Spawn via Questions section to obtain IP address

### Connection Details
```
IP Address: [Obtain from Questions section]
Username: htb-student_adm
Password: Academy_student_DA!
```

### Connection Command
Use `xfreerdp` to connect to the target:
```bash
xfreerdp /v: /u:htb-student_adm /p:Academy_student_DA!
```

### Getting Started
1. Click in the **Questions** section to spawn the target host and obtain IP address
2. Acquire VPN key for the lab if needed
3. Open terminal in Pwnbox or from your lab VM over VPN
4. Execute the RDP connection command with the target IP
5. Once connected, open MMC console, PowerShell, or ADDS tools to begin

## Lab Environment Access
- MMC Console
- PowerShell
- Active Directory Domain Services (ADDS) tools

---
*This lab provides practical experience in enterprise Active Directory administration and troubleshooting scenarios commonly encountered in IT environments.*
