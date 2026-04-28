# IT Homelab Portfolio

## 🧭 Overview

This repository documents a hands-on IT homelab built to develop and demonstrate practical system administration and IT support skills.

The environment simulates a basic enterprise network using virtualization, with a primary focus on Active Directory, identity management, and access control.

All configurations and testing are performed in a controlled lab environment using Proxmox.

---

## 🖥️ Lab Environment

**Hypervisor:**

* Proxmox Virtual Environment (Proxmox VE)

**Virtual Machines:**

* Windows Server (Domain Controller)
* Windows 10 Client (Domain-joined workstation)

**Core Services Configured:**

* Active Directory Domain Services (AD DS)
* DNS (name resolution within the domain)
* File sharing with NTFS-based access control

---

## 📂 Active Directory Implementation

A structured Active Directory environment was deployed to model real-world user and access management.

### Directory Structure

* Organizational Units (OUs) created to represent logical separation (e.g., branches and departments)
* User accounts organized based on role and location

### Group Design

* **Global Groups** used to organize users by role/department
* **Domain Local Groups** used to assign permissions to resources

Group nesting follows the **AGDLP model**:

> Accounts → Global Groups → Domain Local Groups → Permissions

---

## 🔐 Access Control Configuration

* Created departmental shared folders
* Applied NTFS permissions using Domain Local Groups
* Nested Global Groups into Domain Local Groups to enforce role-based access control
* Restricted access based on user role and group membership

---

## 🧪 Validation & Testing

* Successfully joined client machine to the domain
* Verified domain authentication for multiple user accounts
* Tested access control by logging in as different users and validating permissions
* Confirmed proper DNS resolution within the domain environment

---

## 🧠 Technical Skills Demonstrated

* Active Directory administration (users, groups, OUs)
* Role-based access control (RBAC)
* NTFS permissions and shared resource management
* Domain authentication and client-server interaction
* Basic networking (DNS, connectivity validation)
* Virtualization and lab deployment using Proxmox

---

## 🚧 In Progress

The lab environment is being expanded to include:

* Ticketing system simulation (helpdesk workflow)
* Windows troubleshooting scenarios
* Group Policy (GPO) configuration and enforcement

---

## 🎯 Objective

To build job-ready IT support and system administration skills by implementing and testing real-world scenarios in a controlled lab environment.

---

## 📌 Notes

This portfolio reflects practical, hands-on work and will continue to evolve with additional infrastructure, troubleshooting cases, and system configurations.
