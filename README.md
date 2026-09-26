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
## Main Components

- **Azure Virtual Machine** – Hosts the Windows Server environment.
- **Active Directory Domain Services** – Manages on-premises identities.
- **Microsoft Entra Connect** – Synchronizes identities.
- **Password Hash Synchronisation** – Supports cloud authentication.
- **Microsoft Entra ID** – Provides the cloud identity layer.
- **Azure Virtual Network** – Provides network connectivity.

---

## Project Workflow

```text
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
Cloud Authentication & MFA Verification
         ↓
Filtering and Troubleshooting
         ↓
Project Validation

Project Tasks
Task 1 — Azure Environment Setup
- Created the required Azure environment.
- Configured the virtual network and subnet.
- Deployed the Windows Server virtual machine.
- Connected to the Windows Server environment.
Task 2 — Active Directory Configuration
- Installed and configured Active Directory Domain Services.
- Created the p093hybrid.local domain.
- Configured Organizational Units for users, groups, and administration.
- Created test users and groups.
- Configured user UPNs using the Microsoft Entra tenant domain.
- Verified Active Directory users and groups.
Task 3 — Microsoft Entra Connect with PHS
- Installed Microsoft Entra Connect.
- Connected the on-premises Active Directory forest to Microsoft Entra ID.
- Configured the Microsoft Entra tenant connection.
- Configured synchronization scope using selected Organizational Units.
- Enabled Password Hash Synchronisation.
- Completed Microsoft Entra Connect configuration successfully.
- Started the initial synchronization process.
Task 4 — Identity Synchronization and Verification
- Synchronized the selected on-premises users to Microsoft Entra ID.
- Verified Test User1, Test User2, and Test User3 in Microsoft Entra ID.
- Confirmed the synchronized users were enabled.
- Verified the users had the expected Microsoft Entra UPN format.
- Tested cloud authentication using a synchronized user.
- Successfully completed authentication using the configured authentication app.
Task 5 — Filtering and Troubleshooting
- Configured synchronization using selected Active Directory Organizational Units.
- Investigated UPN suffix configuration.
- Resolved Microsoft Entra Connect administrative credential requirements.
- Configured the required Enterprise Admin permissions for the on-premises AD account.
- Verified synchronization after Microsoft Entra Connect configuration.
- Confirmed that only the intended Organizational Units were included in synchronization.

### 2. Then find this

```markdown
Troubleshooting Areas 
 
The project focuses on:

Replace from Troubleshooting Areas through the end of the README with:

---

## Troubleshooting Areas

During implementation, several configuration issues were identified and resolved.

### UPN Configuration

The on-premises users were configured with the Microsoft Entra tenant UPN suffix:

`@anembhargav02gmail.onmicrosoft.com`

This allowed the synchronized users to appear in Microsoft Entra ID with the expected cloud sign-in format.

### Microsoft Entra Connect Administrative Credentials

Microsoft Entra Connect required an appropriate on-premises Active Directory administrative account when adding the AD directory.

The required permissions were configured for the AD administrative account before continuing with synchronization.

### Synchronization Scope

Synchronization was restricted to the required Active Directory Organizational Units rather than synchronizing the entire domain.

The selected OUs included:

- `P093-Users`
- `P093-Groups`

### Synchronization Verification

After Microsoft Entra Connect configuration completed, the synchronized users were verified in Microsoft Entra ID.

The following test users were successfully synchronized:

- `Test User1`
- `Test User2`
- `Test User3`

### Authentication Verification

A synchronized test user successfully signed in using the Microsoft Entra cloud identity, and authentication using the configured authentication app was also successfully verified.

---

## Testing Results

| Test | Result |
|---|---|
| Active Directory configuration | Passed |
| Microsoft Entra Connect installation | Passed |
| AD directory connection | Passed |
| Selected OU synchronization | Passed |
| Password Hash Synchronisation | Passed |
| Test User1 synchronization | Passed |
| Test User2 synchronization | Passed |
| Test User3 synchronization | Passed |
| Microsoft Entra cloud sign-in | Passed |
| Authentication app verification | Passed |

---

## Final Outcome

The Azure Hybrid Identity environment was successfully implemented.

The completed solution provides:

- On-premises Active Directory
- Microsoft Entra ID integration
- Microsoft Entra Connect synchronization
- Password Hash Synchronisation
- Controlled synchronization scope
- Synchronization of selected test users
- Cloud authentication using synchronized identities
- Authentication app verification
- Verification and troubleshooting of the hybrid identity configuration

The final implementation demonstrates a working hybrid identity environment connecting on-premises Active Directory with Microsoft Entra ID.
### Testing Includes

- Active Directory verification
- Microsoft Entra ID verification
- Synchronization status
- Attribute verification
- Cloud authentication
- Filtering validation

---

## ## Final Outcome

The completed project demonstrate:

- A functioning Active Directory environment
- Integration with Microsoft Entra ID
- Controlled identity synchronization
- Password Hash Synchronisation
- Successful synchronization of selected users
- Cloud authentication using synchronized identities
- Synchronization filtering
- Troubleshooting of common synchronization issues

---

## Repository Structure

```text
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

## Project Information

- **Project Code:** 24CC3046-P093
- **Project Title:** Azure Hybrid Identity with Password Hash Synchronisation
- **Domain:** Identity and Cloud Computing
- **Status:** Completed
- **Microsoft Entra Connect:** Configured Successfully
- **Password Hash Synchronisation:** Enabled
- **Synchronization:** Successfully Verified
- **Cloud Authentication:** Successfully Verified
- **MFA / Authentication App:** Successfully Verified
