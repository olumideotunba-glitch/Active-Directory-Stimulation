
# Active Directory Simulation – CyberTech Solutions

This project is the deployment of a Windows Server Domain Controller (Active Directory) for a company called **CyberTech Solutions**. It includes domain setup, client configuration, OU design, group policies, and access control in an enterprise environment.

---

## Company Structure

**CyberTech Solutions** is a small IT services firm with the following structure:

- 1 x Windows Server (AD Domain Controller)
- 1 x Windows 8 Client PC (Sales Department)
- 1 x Windows 8 Client PC (Marketing Software)

---

## Project Objectives

- Configure an AD Domain Controller on Windows Server
- Join client PCs to the domain
- Create Organizational Units (OUs)
- Implement basic Group Policies for access control
- Simulate a centralized IT environment

---

## Network Design

```
Internet
   ↓
Router (Gateway: 10.0.5.1)
   ↓
Switch
 ┌──────┬─────────────┬──────────────┐
 │      │             │              │
Server  PC1 (Win 8i)   PC2 (Win 8ii)
```

| Device        | IP Address      | Role                        |
|---------------|----------------|-----------------------------|
| Windows Server| 10.0.5.5  | AD Domain Controller (DC)   |
| Windows 8 PC  | DHCP    | Busola (Sales)           |
| Windows 8ii PC | DHCP    | Olumide Marketing               |

---

## Domain Configuration

- **Domain Name**: `Bpumpytech`
- **Server Name**: `bpumpytech.ai`
- **Static IP**: `10.0.2.4`
- **AD Roles Installed**: AD DS, DNS (DHCP)

---

## Organizational Units (OUs)

Created using **Active Directory Users and Computers**:

```
CyberTech.local
├── OU: Marketing Department
│   └── Users: olumide.marketing
    └── Users: 

├── OU: Sales
│   └── Users: busola.sales
```

---

## Group Policy (GPO)

Created and linked using **Group Policy Management Console (gpmc.msc)**:

- **GPO Name**: `DisableShutDown`
- **Linked to**: OU: Sales Department
- **Policy Configured**:
  - `Computer Configuration` > `Administrative Templates` > `System` > `DisableShutDown`
  - Set **"DisableShutDown: Deny all access"** to **Enabled**

Result: Disable shut down from user in the **Accounts OU**.

---

## Screenshots

- [AD Domain Structure](https://github.com/olumideotunba-glitch/Active-Directory-Stimulation/blob/main/Screenshot/Creating_Organization_%20units_%26users5i.png)
  {https://github.com/olumideotunba-glitch/Active-Directory-Stimulation/blob/819d7f8192f59904c23f547a26a6c738ed38f220/Linking%20GPO%20into%20Domain.png}GPO Editor Screenshot
- PC joined to domain
- Result of Disablling Shut Down

---

## Key Takeaways

- Gained practical experience with Windows Server roles and domain setup
- Implemented centralized access control using Group Policy
- Learned how to structure users and departments with OUs
- Applied IAM concepts in a real-world simulated environment

---

## Author

**Olumide Enilolobo**  
Cybersecurity Analyst  
