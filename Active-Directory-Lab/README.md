# Active Directory Lab — Proxmox Homelab

A Windows Active Directory environment built in a Proxmox virtual lab, simulating a small enterprise network across two branches with full departmental separation. Covers identity management, role-based access control, NTFS permissions, and end-to-end domain authentication — built entirely from scratch.

---

## Environment

| Component | Details |
|---|---|
| Hypervisor | Proxmox VE |
| Domain Controller | Windows Server (AD DS, DNS) |
| Client Workstation | Windows 10 (domain-joined) |
| Services | Active Directory Domain Services, DNS, NTFS file sharing |

---

## Domain Structure

The domain uses a branch-based OU hierarchy with departmental separation inside each site. This mirrors how enterprise environments segment identity management across locations.

```
corp.local
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

![OU Structure](./images/ou-structure.png)
*Active Directory Users and Computers — Branch1 and Branch2 expanded with department OUs visible*

---

## User & Group Management

User accounts are placed directly into their department OUs. Security groups are used for all role assignments — no permissions are applied to individual user accounts.

| Group | Role |
|---|---|
| Helpdesk | Tier 1 support access |
| Senior Helpdesk | Elevated support access |
| Network Engineer | Infrastructure access |
| Administrator | Full domain control |

![Users and Groups](./images/users-groups.png)
*Branch1 → IT → Groups — security groups visible inside the department OU*

Group membership was verified to confirm groups are actively used and not just created.

![Group Membership](./images/group-membership.png)
*Helpdesk group — Members tab showing assigned user accounts*

---

## Access Control (NTFS Permissions)

Shared folders were created for each department. All access is assigned through security groups, enforcing clean separation between departments and branches. No individual user accounts appear in any ACL.

| Permission | Assigned To |
|---|---|
| Read | Helpdesk |
| Modify | Senior Helpdesk, Network Engineer |
| Full Control | Administrator |

![NTFS Permissions](./images/permissions.png)
*Folder Properties → Security tab — groups listed with explicit permission levels, no individual users*

---

## Domain Authentication

A Windows 10 client was joined to the domain and used to validate the full authentication flow across multiple user accounts and roles.

![Domain Login](./images/domain-login.png)
*Domain-joined Windows 10 workstation — `domain\user` format confirms successful domain login*

---

## Validation

- [x] Windows 10 client joined to the domain
- [x] User authentication verified across multiple accounts and roles
- [x] Shared resource access confirmed per role
- [x] Unauthorized access attempts correctly denied
- [x] DNS resolution confirmed within the domain

---

## Skills Demonstrated

- Active Directory administration — users, groups, OUs
- Organizational Unit design with branch-based hierarchy
- Role-based access control (RBAC) via security groups
- NTFS permissions and file-level security
- Domain authentication and client management
- Virtualization with Proxmox VE
