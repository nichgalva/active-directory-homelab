# Active Directory Home Lab

## 📌 Overview
This project simulates a real-world IT help desk environment using Active Directory.  
It includes domain setup, user and group management, shared folder permissions, and common troubleshooting scenarios.

---

## 🧱 Lab Environment

- Hypervisor: VirtualBox  
- Windows Server 2019 (Domain Controller)  
- Windows 10 (Client Machine)  

---

## 🌐 Network Configuration

- Domain Controller IP: 192.168.10.10  
- Client IP: 192.168.10.20  
- DNS configured to point to Domain Controller  
- Internal network used for communication  

![Network Setup](screenshots/03-network-internal.png)

---

## ⚙️ Active Directory Setup

- Installed Active Directory Domain Services (AD DS)  
- Promoted server to Domain Controller  
- Created domain: `homelab.local`  

![AD Installation](screenshots/05-ad-install.png)  
![Domain Setup](screenshots/06-domain-creation.png)

---

## 👥 User & Group Management

- Created Organizational Units:
  - HR, Sales, IT  

- Created users:
  - jsmith (HR)  
  - mlopez (Sales)  
  - itadmin  

- Created security groups:
  - HR-Users  
  - Sales-Users  

- Assigned users to appropriate groups  

![OUs](screenshots/07-organizational-units.png)  
![Users](screenshots/08-users-created.png)  
![Groups](screenshots/09-groups.png)

---

## 🖥️ Domain Join

- Joined Windows 10 client to domain  
- Verified login using domain credentials  

![Domain Join](screenshots/11-domain-join.png)  
![Domain Login](screenshots/12-domain-login.png)

---

## 📁 Shared Folder & Permissions

- Created shared folder: `C:\Departments`  
- Configured subfolders for HR and Sales  
- Assigned permissions using security groups  

![Shared Folder](screenshots/13-shared-folder.png)  
![Permissions](screenshots/14-permissions.png)  
![Access Test](screenshots/15-folder-access.png)

---

## 🛠️ Troubleshooting Scenarios

### 🔹 DNS Misconfiguration (Login Issue)
- Changed client DNS to incorrect server  
- Observed login behavior (cached credentials vs new user)  
- Restored correct DNS to resolve issue  

---

### 🔹 Access Denied (Permissions Issue)
- Removed group permissions  
- Observed continued access due to inherited permissions and default group membership  
- Disabled inheritance and reapplied correct permissions  

---

### 🔹 Account Lockout
- Triggered lockout with multiple failed logins  
- Unlocked account using Active Directory  

---

## 🧠 Key Takeaways

- Gained hands-on experience with Active Directory environments  
- Learned importance of DNS in domain authentication  
- Practiced role-based access control using security groups  
- Troubleshot real-world issues including permission conflicts and account lockouts  

---

## 🔗 Future Improvements

- Implement Group Policy Objects (GPOs)  
- Automate user creation with PowerShell  
- Simulate ticket-based help desk scenarios  
