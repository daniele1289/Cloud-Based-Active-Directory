# Active Directory Configuration Documentation

## Server Configuration

**Server Name:** DC01  
**Operating System:** Windows Server 2022 Standard Evaluation (Desktop Experience)  
**Server Role:** Domain Controller  

---

## Domain Configuration

**Active Directory Domain:** corp.local  

**Domain Controller:** DC01  

**Active Directory Services Installed:**
- Active Directory Domain Services (AD DS)
- DNS Server
- Group Policy Management

---

## Network Configuration

| Device | Role | IP Address |
|--------|------|------------|
| DC01 | Domain Controller | 192.168.10.10 |

**Subnet Mask:** 255.255.255.0  

**DNS Server:** 192.168.10.10  

### DNS Configuration
- Configured DC01 to use itself as the primary DNS server.
- DNS was integrated with Active Directory to support domain authentication and resource discovery.
- Verified the `corp.local` DNS zone was created successfully.

---

# Organizational Unit (OU) Design

The Active Directory environment was organized using Organizational Units to separate users and computers based on department and function.

```
corp.local
│
├── IT
├── HR
├── Finance
├── Sales
├── Workstations
└── Servers
```

### Purpose
- Simplifies administration.
- Allows future Group Policy deployment.
- Separates user accounts from computer objects.
- Improves organization and scalability.

---

# Security Groups

Created departmental security groups to implement Role-Based Access Control (RBAC).

| Organizational Unit | Security Group |
|---------------------|----------------|
| IT | IT_Admins |
| HR | HR_Users |
| Finance | Finance_Users |
| Sales | Sales_Users |

### Purpose
- Assign permissions to groups instead of individual users.
- Simplify user management.
- Prepare environment for access control policies.

---

# User Structure

Created domain users and assigned them to their appropriate departments and security groups.

| Department | Username | Security Group |
|------------|----------|----------------|
| IT | jsmith | IT_Admins |
| IT | sjohnson | IT_Admins |
| HR | edavis | HR_Users |
| HR | mbrown | HR_Users |
| Finance | dwilson | Finance_Users |
| Finance | ltaylor | Finance_Users |
| Sales | cmoore | Sales_Users |
| Sales | omartinez | Sales_Users |

---

# Active Directory Implementation Summary

Completed:
- Installed and configured Windows Server 2022 Domain Controller.
- Created `corp.local` Active Directory domain.
- Configured DNS for domain services.
- Designed Organizational Unit structure.
- Created security groups using RBAC principles.
- Created and organized domain user accounts.

---

# Future Improvements

Planned additions:
- Join Windows 11 CLIENT01 workstation to the domain.
- Configure Group Policies.
- Create shared folders and NTFS permissions.
- Implement PowerShell automation for user/group creation.
- Integrate Splunk for Windows event monitoring.
- Add Sysmon logging and detection rules.
