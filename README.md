# 24CC3046-P093: Azure Hybrid Identity with Password Hash Synchronisation

## Project Overview

This project demonstrates a hybrid identity environment by connecting an on-premises Active Directory Domain Services (AD DS) environment with Microsoft Entra ID.

Microsoft Entra Connect is used to synchronize selected identities, with Password Hash Synchronisation (PHS) configured for cloud authentication using existing organizational credentials.

The project also addresses common synchronization challenges such as duplicate attributes, unwanted account synchronization, filtering issues, and synchronization failures.

---

## Problem Statement

Organizations using both on-premises infrastructure and cloud services may face identity-management challenges such as:

- Duplicate user accounts
- Additional password management
- Synchronization inconsistencies
- Unwanted account synchronization
- Authentication and access-management issues

This project implements a controlled hybrid identity architecture using Azure, Active Directory, Microsoft Entra ID, and Microsoft Entra Connect.

---

## Objectives

1. Set up an on-premises Active Directory environment.
2. Configure users, groups, and Organizational Units.
3. Prepare Microsoft Entra ID for hybrid identity integration.
4. Install and configure Microsoft Entra Connect.
5. Enable Password Hash Synchronisation.
6. Synchronize selected identities to Microsoft Entra ID.
7. Verify synchronization and cloud authentication.
8. Configure synchronization filtering.
9. Identify and troubleshoot synchronization problems.

---

## Architecture

The project follows a hybrid identity architecture in which identities are created and managed in on-premises Active Directory and synchronized to Microsoft Entra ID.

### Architecture Diagram

![Azure Hybrid Identity Architecture](project%20Architecture%20diagram.png)

### Architecture Flow

```text
On-Premises Active Directory
            |
            v
   Microsoft Entra Connect
       /     |      \
      /      |       \
Directory   PHS    Filtering
  Sync
            |
            v
     Microsoft Entra ID
            |
            v
     Cloud Applications
Main Components
Azure Virtual Machine – Hosts the Windows Server environment.
Active Directory Domain Services – Manages on-premises identities.
Microsoft Entra Connect – Synchronizes identities.
Password Hash Synchronisation – Supports cloud authentication.
Microsoft Entra ID – Provides the cloud identity layer.
Azure Virtual Network – Provides network connectivity.
Project Workflow
Azure Infrastructure Setup
          ↓
Windows Server Configuration
          ↓
Active Directory Setup
          ↓
Microsoft Entra ID Preparation
          ↓
Microsoft Entra Connect Configuration
          ↓
Password Hash Synchronisation
          ↓
Identity Synchronization
          ↓
Authentication Verification
          ↓
Filtering and Troubleshooting
Project Tasks
Task 1 — Azure Environment Setup
Create resource group
Create virtual network and subnet
Deploy Windows Server VM
Connect to the virtual machine
Task 2 — Active Directory Configuration
Install AD DS
Create test domain
Create Organizational Units
Create test users and groups
Verify Active Directory
Task 3 — Microsoft Entra Connect with PHS
Install Microsoft Entra Connect
Connect Active Directory
Configure synchronization
Enable Password Hash Synchronisation
Configure synchronization scope
Task 4 — Identity Synchronization and Verification
Run synchronization
Check synchronized users
Verify user attributes
Test cloud authentication
Confirm synchronized identity access
Task 5 — Filtering and Troubleshooting
Configure synchronization filtering
Test duplicate attributes
Examine synchronization errors
Check unwanted account synchronization
Monitor and troubleshoot synchronization
Troubleshooting Areas

The project focuses on:

Duplicate identity attributes
Incorrect synchronization filtering
Synchronization errors
Unwanted account synchronization

Testing includes:

Active Directory verification
Microsoft Entra ID verification
Synchronization status
Attribute verification
Cloud authentication
Filtering validation
Expected Outcome

The completed project should demonstrate:

A functioning Active Directory environment
Integration with Microsoft Entra ID
Controlled identity synchronization
Password Hash Synchronisation
Successful synchronization of selected users
Cloud authentication using synchronized identities
Synchronization filtering
Troubleshooting of common synchronization issues
Repository Structure
24CC3046-P093-Azure-Hybrid-Identity/
│
├── README.md
├── project Architecture diagram.png
├── Project_Abstract.docx
├── Project_Modules.docx
├── Required_Services.docx
├── Five_Project_Tasks.docx
├── Architecture_Explanation.docx
│
├── tasks/
├── screenshots/
└── results/
Project Information
Project Code: 24CC3046-P093
Project Title: Azure Hybrid Identity with Password Hash Synchronisation
Domain: Identity and Cloud Computing
Status: In Progress

The repository will be updated with implementation steps, configurations, screenshots, testing results, and documentation as the project progresses
