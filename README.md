# Microsoft-Endpoint-Management-Labs-KG
# Microsoft Endpoint Management Labs

Hands-on enterprise endpoint management lab portfolio focused on **Microsoft Intune, Microsoft Entra ID, Microsoft Configuration Manager (SCCM), Windows Autopilot, Azure, Microsoft 365, and Windows 11 management**.

This repository documents my practical work building, configuring, integrating, testing, and troubleshooting Microsoft endpoint-management technologies in a hybrid lab environment.

---

## Project Overview

The purpose of this repository is to demonstrate practical experience with both **traditional on-premises endpoint management** and **modern cloud-based device management**.

The environment combines:

* Microsoft Intune
* Microsoft Entra ID
* Microsoft Configuration Manager / SCCM
* Microsoft Azure
* Microsoft 365
* Windows Autopilot
* Windows 11
* Active Directory Domain Services
* Hyper-V
* PowerShell
* Hybrid device management
* Tenant Attach
* Co-management

The main lab environment is based on the official **Microsoft Intune and Configuration Manager Evaluation Lab Kit**, supplemented with additional **MD-102 Endpoint Administrator labs and independent proof-of-concept scenarios**.

---

## Lab Architecture

```text
                         MICROSOFT CLOUD
                ┌─────────────────────────────┐
                │                             │
                │     Microsoft Entra ID      │
                │             │               │
                │       Microsoft Intune      │
                │             │               │
                │          Azure              │
                │             │               │
                │      Microsoft 365          │
                │                             │
                └──────────────┬──────────────┘
                               │
                    Hybrid Management
                               │
             Tenant Attach / Co-management
                               │
                ┌──────────────┴──────────────┐
                │                             │
                │       ON-PREMISES LAB       │
                │                             │
                │  HYD-DC1                    │
                │  Active Directory / DNS     │
                │  DHCP / Certificate Services│
                │             │               │
                │  HYD-CM1                    │
                │  Configuration Manager      │
                │  SQL Server / WSUS / WDS    │
                │             │               │
                │  HYD-GW1                    │
                │  Internet Gateway           │
                │             │               │
                │  Windows 11 Clients         │
                │  HYD-CLIENT1–6              │
                │                             │
                └─────────────────────────────┘
```

---

## Technology Stack

| Technology                          | Lab Use                                                                 |
| ----------------------------------- | ----------------------------------------------------------------------- |
| **Microsoft Intune**                | MDM, policy management, application deployment and device configuration |
| **Microsoft Entra ID**              | Identity, device registration, roles and hybrid identity                |
| **Microsoft Configuration Manager** | Traditional endpoint management, software deployment and co-management  |
| **Windows Autopilot**               | Modern Windows provisioning and enrollment                              |
| **Microsoft Azure**                 | Cloud infrastructure and Configuration Manager cloud integration        |
| **Microsoft 365**                   | Cloud services and Microsoft 365 Apps deployment                        |
| **Active Directory**                | On-premises identity and domain services                                |
| **Microsoft Entra Connect**         | Hybrid identity synchronization                                         |
| **Hyper-V**                         | Hosting the Microsoft evaluation environment                            |
| **Windows 11**                      | Managed endpoint platform                                               |
| **PowerShell**                      | Administration, validation and troubleshooting                          |
| **SQL Server**                      | Configuration Manager site database                                     |
| **WSUS / WDS**                      | Updates and Windows deployment services                                 |

---

# Lab Tracks

## 1. Intune & Configuration Manager Evaluation Lab

The primary environment demonstrates the integration of an on-premises Configuration Manager deployment with Microsoft cloud management.

Topics include:

* Azure and Microsoft Entra tenant preparation
* Hyper-V lab deployment
* Configuration Manager validation
* Microsoft Intune configuration
* Microsoft Entra Connect
* Hybrid Microsoft Entra Join
* Tenant Attach
* Co-management
* Cloud Management Gateway
* Windows Autopilot
* Windows Update management
* Configuration profiles
* Compliance and security policies
* Microsoft 365 Apps deployment
* Enterprise application deployment

---

## 2. MD-102 Endpoint Administrator Labs

Additional labs focus on Microsoft Endpoint Administrator skills aligned with MD-102.

Planned and completed scenarios include:

* User and group administration
* Group-based licensing
* Device enrollment restrictions
* Device enrollment managers
* Microsoft Entra joined devices
* Hybrid Microsoft Entra joined devices
* Windows Autopilot
* Configuration profiles
* Settings Catalog
* OMA-URI policies
* Windows Update rings
* Application deployment
* Endpoint security
* BitLocker
* Microsoft Defender
* Device compliance
* Conditional Access integration

---

# Repository Structure

```text
Microsoft-Endpoint-Management-Labs-KG/
│
├── README.md
│
├── Intune-ConfigurationManager-LabKit/
│   ├── 01-Azure-Entra-Foundation.md
│   ├── 02-HyperV-Lab-Deployment.md
│   ├── 03-Configuration-Manager-Validation.md
│   ├── 04-Intune-Cloud-Setup.md
│   ├── 05-Entra-Connect-Hybrid-Join.md
│   ├── 06-Tenant-Attach-CoManagement.md
│   ├── 07-Windows-Autopilot.md
│   ├── 08-Policies-and-Compliance.md
│   ├── 09-Application-Deployment.md
│   └── Troubleshooting.md
│
├── MD-102-Labs/
│
├── PowerShell/
│   ├── Validation/
│   ├── Autopilot/
│   └── Troubleshooting/
│
└── Screenshots/
    ├── Azure/
    ├── Entra/
    ├── Hyper-V/
    ├── Configuration-Manager/
    └── Intune/
```

---

# Current Lab Progress

| Phase                                    | Status         |
| ---------------------------------------- | -------------- |
| Azure Free Trial provisioning            | ✅ Completed    |
| Azure cost controls / budget             | ✅ Completed    |
| Microsoft Entra tenant preparation       | ✅ Completed    |
| Dedicated lab administrator              | ✅ Completed    |
| Azure RBAC configuration                 | ✅ Completed    |
| Hyper-V environment deployment           | ✅ Completed    |
| Domain Controller validation             | ✅ Completed    |
| Configuration Manager server validation  | ✅ Completed    |
| SQL Server validation                    | ✅ Completed    |
| Configuration Manager Console validation | ✅ Completed    |
| Microsoft 365 / Intune cloud setup       | 🔄 In Progress |
| Microsoft Entra Connect                  | ⏳ Pending      |
| Hybrid device registration               | ⏳ Pending      |
| Tenant Attach                            | ⏳ Pending      |
| Co-management                            | ⏳ Pending      |
| Windows Autopilot                        | ⏳ Pending      |
| Intune policy deployment                 | ⏳ Pending      |
| Application deployment                   | ⏳ Pending      |

---

# Troubleshooting Is Part of the Lab

This repository intentionally documents failures as well as successful configurations.

Real-world issues encountered during the build include:

* Microsoft Entra tenant-context authentication errors
* `AADSTS50020` sign-in failures
* MFA registration loops
* Azure RBAC versus Microsoft Entra role differences
* Azure subscription visibility issues
* Hyper-V VM import and storage-path problems
* External storage / USB connectivity instability
* Lab provisioning failures
* PowerShell `PercentComplete` values exceeding `100`
* Configuration Manager VM registration issues
* Cold-start dependency timing between domain services and Configuration Manager

For each significant issue, the documentation records:

```text
Symptom
    ↓
Investigation
    ↓
Root Cause
    ↓
Resolution
    ↓
Validation
    ↓
Lesson Learned
```

The goal is to demonstrate not only how a technology is configured, but also how it is **diagnosed and recovered when something does not work as expected**.

---

# Key Learning Objectives

By completing this project I aim to strengthen hands-on capability in:

* Modern endpoint management
* Microsoft Intune administration
* Microsoft Entra device identity
* Hybrid identity
* Windows Autopilot
* Configuration Manager administration
* Co-management architecture
* Tenant Attach
* Application lifecycle management
* Windows Update management
* Endpoint security
* Enterprise troubleshooting
* PowerShell automation
* Cloud and on-premises integration

---

# Security and Privacy

This repository is intended for technical demonstration and learning.

Sensitive information is intentionally excluded or redacted.

The following are **never committed**:

* Passwords
* Client secrets
* Certificate private keys
* Tenant IDs
* Subscription IDs
* Payment information
* Personal email addresses
* Authentication tokens
* Production credentials
* Unredacted sensitive screenshots

Example values are represented using placeholders such as:

```text
<LAB-DOMAIN>
<TENANT-ID>
<SUBSCRIPTION-ID>
<ADMIN-UPN>
```

---

## Documentation Approach

Each lab document follows a consistent engineering format:

1. **Objective**
2. **Concept / Architecture**
3. **Prerequisites**
4. **Configuration**
5. **Validation**
6. **Issues Encountered**
7. **Root Cause**
8. **Resolution**
9. **Lessons Learned**

This makes the repository both a learning reference and a record of practical implementation experience.

---

## Disclaimer

This repository is an independent learning and portfolio project.

Microsoft product names and trademarks belong to Microsoft.

The Microsoft evaluation lab material is used as a reference environment; this repository documents my own configuration process, testing, troubleshooting, observations, and lab results.

---

> **Current focus:** Building the hybrid management bridge between Microsoft Configuration Manager and Microsoft Intune using Microsoft Entra ID, Tenant Attach and Co-management.
