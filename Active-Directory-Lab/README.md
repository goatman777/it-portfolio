# Active Directory Lab (Proxmox Homelab)

## 🧭 Overview

This project documents a Windows Active Directory environment built in a Proxmox-based virtual lab. It simulates a small enterprise structure with multiple branches and departments, focusing on identity management and access control.

---

## 🖥️ Lab Environment

* Proxmox Virtual Environment (Proxmox VE)
* Windows Server (Domain Controller)
* Windows 10 Client (Domain-joined workstation)
* Active Directory Domain Services (AD DS)
* DNS
* NTFS file sharing and permissions

---

## 🏗️ Active Directory Structure

The domain is organized using a branch-based structure.

```text id="adimgstruct"
Domain
├── Branch1
│   ├── IT
│   ├── HR
│   ├── Finance
│   └── Sales
└── Branch2
    ├── IT
    ├── HR
    ├── Finance
    └── Sales
```

### 📸 OU Structure in Active Directory

![OU Structure](./images/ou-structure.png)

---

## 👥 User & Group Management

* Users created per branch and department
* Security groups assigned based on role and location
* Groups used to manage access to resources

### 📸 Users and Groups in ADUC

![Users and Groups](./images/users-groups.png)

---

## 🔐 Access Control (NTFS Permissions)

* Shared folders created per department
* Permissions applied using security groups (not individual users)
* Access restricted based on group membership

### 📸 Folder Permissions Configuration

![NTFS Permissions](./images/permissions.png)

---

## 🧪 Validation & Testing

* Domain join confirmed from Windows 10 client
* User authentication verified
* Access tested across multiple users
* Unauthorized access correctly denied

### 📸 Domain-Joined Client Login

![Domain Login](./images/domain-login.png)

---

## 🧠 Skills Demonstrated

* Active Directory administration (users, groups, OUs)
* Organizational Unit design (branch-based structure)
* Role-based access control (RBAC)
* NTFS permissions and file security
* Domain authentication and client management
* Virtualization using Proxmox

---

## 🎯 Objective

To develop practical IT support and system administration skills through a structured Active Directory environment that simulates real-world enterprise identity and access management.

---

## 📌 Notes

This project will be expanded with Group Policy configuration, troubleshooting scenarios, and helpdesk simulation labs.
