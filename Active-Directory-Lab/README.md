# Active Directory Homelab Portfolio

## 🧭 Overview

This project documents a Windows Active Directory environment built and managed in a Proxmox-based virtual lab. The purpose of this lab is to demonstrate practical IT support and system administration skills, including identity management, access control, and domain-based authentication.

The environment simulates a small enterprise structured across multiple branches and departments.

---

## 🖥️ Lab Environment

**Hypervisor:**

* Proxmox Virtual Environment (Proxmox VE)

**Virtual Machines:**

* Windows Server (Active Directory Domain Controller)
* Windows 10 Client (Domain-joined workstation)

**Core Services:**

* Active Directory Domain Services (AD DS)
* DNS (domain name resolution)
* NTFS file sharing and permissions

---

## 🏗️ Active Directory Structure

The domain is organized using a branch-based structure with departmental separation.

```text id="adstructurefinal"
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

This structure was designed to reflect a multi-branch organization and support scalable user and permission management.

---

## 👥 User & Group Management

* User accounts were created within each branch and department
* Security groups were created to represent departments and roles
* Users were assigned to groups based on their department and branch
* Groups were used to simplify access control and resource assignment

---

## 🔐 Access Control Implementation

* Departmental shared folders were created for resource access
* NTFS permissions were assigned using security groups (not individual users)
* Access was restricted based on group membership
* Separation of access between Branch1 and Branch2 was enforced through permissions

---

## 🧪 Validation & Testing

The environment was tested to confirm correct functionality:

* Windows 10 client successfully joined to the domain
* User authentication verified across multiple accounts
* Access to shared resources validated based on group membership
* Unauthorized access attempts were correctly denied
* DNS resolution confirmed within the domain environment

---

## 🧠 Skills Demonstrated

* Active Directory administration (users, groups, OUs)
* Organizational Unit design and structure
* Role-based access control (RBAC)
* NTFS permissions and shared resource security
* Domain authentication and client management
* Basic Windows Server and networking concepts
* Virtualization using Proxmox VE

---

## 🎯 Objective

To develop practical, job-relevant IT support and system administration skills by building and managing a virtual Active Directory environment that simulates a real-world enterprise structure.

---

## 📌 Notes

This project is part of an ongoing homelab used to build foundational IT infrastructure and troubleshooting skills. Additional projects such as Group Policy configuration, ticketing system simulation, and troubleshooting scenarios will be added as the lab expands.
