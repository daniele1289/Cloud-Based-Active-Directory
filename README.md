# Cloud-Based-Active-Directory


OVERVIEW
- Build and document a cloud-based Active Directory environment, implement user and group management, and understand domains and forests.



| Machine    | Purpose                                                        |
| ---------- | -------------------------------------------------------------- |
| DC01       | Windows Server 2022 Domain Controller                          |
| CLIENT01   | Windows 11 Domain-Joined Workstation *(after you complete it)* |
| Kali Linux | Security Testing Machine *(future phase)*                      |


# Network Configuration

DC01
IP Address: 192.168.10.10

Domain
corp.local

DNS
192.168.10.10

# Active Directory Configuration
- Installed Active Directory Domain Services
- Promoted server to Domain Controller
- Created corp.local
- Configured DNS
- Verified Active Directory
- Verified Group Policy

  # OUs
IT
HR
Finance
Sales
Workstations
Servers

# Security Groups

IT_Admins
HR_Users
Finance_Users
Sales_Users

# Domain Users

| Username  | Department |
| --------- | ---------- |
| jsmith    | IT         |
| sjohnson  | IT         |
| edavis    | HR         |
| mbrown    | HR         |
| dwilson   | Finance    |
| ltaylor   | Finance    |
| cmoore    | Sales      |
| omartinez | Sales      |


Lessons Learned so far... -->  
- Installed and configured Active Directory Domain Services.
- Learned how DNS supports Active Directory authentication.
- Organized enterprise resources using Organizational Units.
- Implemented Role-Based Access Control using Security Groups.
- Gained experience administering users within an Active Directory domain.
