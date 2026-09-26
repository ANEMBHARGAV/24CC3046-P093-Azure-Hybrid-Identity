# 24CC3046-P093: Azure Hybrid Identity with Password Hash Synchronisation

## Project Overview

This project demonstrates the implementation of a hybrid identity environment by connecting an on-premises Active Directory Domain Services (AD DS) environment with Microsoft Entra ID.

The solution uses Microsoft Entra Connect to synchronize selected identities from the local Active Directory environment to Microsoft Entra ID. Password Hash Synchronisation (PHS) is configured to allow synchronized users to authenticate to supported cloud services using their existing organizational credentials.

The implementation also focuses on common identity synchronization challenges, including duplicate attributes, unwanted account synchronization, filtering configuration issues, and synchronization failures.

---

## Problem Statement

Organizations that use both on-premises infrastructure and cloud services may need to manage identities across different environments.

Maintaining separate identities can lead to:

- Duplicate user accounts
- Additional password management
- Synchronization inconsistencies
- Unwanted accounts being synchronized
- Authentication and access-management issues

This project addresses these challenges by implementing a controlled hybrid identity architecture using Microsoft Azure, Active Directory, Microsoft Entra ID, and Microsoft Entra Connect.

---

## Objectives

The main objectives of this project are:

1. Set up an on-premises Active Directory environment for testing.
2. Configure users, groups, and organizational units in Active Directory.
3. Prepare Microsoft Entra ID for hybrid identity integration.
4. Install and configure Microsoft Entra Connect.
5. Enable Password Hash Synchronisation.
6. Synchronize selected identities from Active Directory to Microsoft Entra ID.
7. Verify synchronized users and cloud authentication.
8. Configure filtering to control which identities are synchronized.
9. Identify and troubleshoot common synchronization problems.

---

## Architecture

The project follows a hybrid identity architecture in which identities are created and managed in an on-premises Active Directory environment and synchronized to Microsoft Entra ID.

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

The architecture consists of the following major components:

On-Premises Identity Environment

A Windows Server virtual machine is used to host Active Directory Domain Services.

The Active Directory environment contains:

Users
Groups
Organizational Units
Domain configuration
Synchronization Layer

Microsoft Entra Connect provides the connection between the on-premises directory and Microsoft Entra ID.

It is used for:

Directory synchronization
Password Hash Synchronisation
Synchronization filtering
Cloud Identity Environment

Microsoft Entra ID provides the cloud-based identity platform where selected synchronized users and groups are available for cloud authentication.

Technologies Used
Technology	Purpose
Microsoft Azure	Provides the cloud infrastructure
Azure Virtual Machine	Hosts the Windows Server environment
Windows Server	Provides the server platform
Active Directory Domain Services	Manages on-premises identities
Microsoft Entra ID	Provides the cloud identity platform
Microsoft Entra Connect	Synchronizes identities between environments
Password Hash Synchronisation	Supports cloud authentication
Azure Virtual Network	Provides network connectivity
Microsoft 365 / Azure Services	Provides cloud application access
Project Components
1. Azure Infrastructure

The Azure environment provides the infrastructure required for the hybrid identity implementation.

The setup includes:

Resource Group
Virtual Network
Subnet
Windows Server Virtual Machine
2. Active Directory Domain Services

Active Directory Domain Services is configured on the Windows Server.

The directory is used to create and organize test identities using:

Organizational Units
Users
Groups
3. Microsoft Entra ID

Microsoft Entra ID provides the cloud identity layer.

Selected identities from the on-premises Active Directory environment are synchronized to the cloud directory.

4. Microsoft Entra Connect

Microsoft Entra Connect is used to establish synchronization between Active Directory and Microsoft Entra ID.

The configuration includes:

Directory synchronization
Password Hash Synchronisation
Synchronization filtering
Project Workflow

The implementation follows these stages:

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

The first task focuses on preparing the Azure infrastructure required for the project.

Activities include:

Creating the resource group
Creating the virtual network
Configuring the subnet
Deploying the Windows Server virtual machine
Connecting to the virtual machine
Task 2 — Active Directory Configuration

The second task focuses on creating the on-premises identity environment.

Activities include:

Installing Active Directory Domain Services
Creating the test domain
Creating Organizational Units
Creating test users
Creating security groups
Verifying the Active Directory configuration
Task 3 — Microsoft Entra Connect with PHS

The third task establishes synchronization between the local Active Directory environment and Microsoft Entra ID.

Activities include:

Installing Microsoft Entra Connect
Connecting the local Active Directory environment
Configuring synchronization
Enabling Password Hash Synchronisation
Selecting the required synchronization scope
Task 4 — Identity Synchronization and Verification

The fourth task verifies that selected identities are successfully synchronized to Microsoft Entra ID.

Activities include:

Running synchronization
Checking synchronized users
Verifying user attributes
Testing cloud authentication
Confirming synchronized identity access
Task 5 — Filtering and Troubleshooting

The fifth task focuses on controlling synchronization and addressing common identity issues.

The task covers:

Synchronization filtering
Duplicate attributes
Synchronization errors
Unwanted account synchronization
Synchronization monitoring
Troubleshooting configuration issues
Password Hash Synchronisation

Password Hash Synchronisation (PHS) allows password-related authentication information to be synchronized from the on-premises Active Directory environment to Microsoft Entra ID in a protected form.

The original on-premises password is not directly transferred to Microsoft Entra ID.

This allows synchronized users to use their existing organizational credentials when accessing supported cloud services.

Synchronization Filtering

Synchronization filtering is used to control which objects from the on-premises Active Directory environment are synchronized to Microsoft Entra ID.

Filtering can be used to control synchronization based on the configured directory scope and organizational structure.

This helps prevent unnecessary or unintended accounts from being synchronized to the cloud directory.

Troubleshooting

The project considers several common hybrid identity problems.

Duplicate Attributes

Duplicate identity attributes can cause synchronization conflicts.

Examples include conflicting:

User Principal Names
Proxy addresses
Other unique identity attributes

These conflicts may prevent an identity from synchronizing successfully.

Incorrect Filtering

An incorrect filtering configuration may cause accounts that are not intended for cloud synchronization to be included.

The synchronization scope is therefore checked and tested to ensure that only the required identities are synchronized.

Synchronization Errors

Synchronization status and error information are examined to identify problems between the on-premises Active Directory environment and Microsoft Entra ID.

Testing and Verification

The implementation will be verified through:

Active Directory user verification
Microsoft Entra ID user verification
Synchronization status checks
Attribute verification
Cloud authentication testing
Filtering validation
Synchronization troubleshooting

Screenshots and test results will be added to the repository as each task is completed.

Expected Outcome

At the completion of the project, the implementation should demonstrate:

A functioning on-premises Active Directory environment
Successful integration with Microsoft Entra ID
Controlled identity synchronization
Password Hash Synchronisation
Successful synchronization of selected users
Cloud authentication using synchronized identities
Appropriate synchronization filtering
Identification and troubleshooting of common synchronization issues
Repository Structure
24CC3046-P093-Azure-Hybrid-Identity/
│
├── README.md
│
├── architecture/
│   └── Architecture_Diagram.png
│
├── documentation/
│
├── tasks/
│   ├── Task-1-Azure-Infrastructure/
│   ├── Task-2-Active-Directory/
│   ├── Task-3-Entra-Connect-PHS/
│   ├── Task-4-Identity-Synchronization/
│   └── Task-5-Filtering-Troubleshooting/
│
├── screenshots/
│   ├── task-1/
│   ├── task-2/
│   ├── task-3/
│   ├── task-4/
│   └── task-5/
│
└── results/
Project Information

Project Code: 24CC3046-P093

Project Title: Azure Hybrid Identity with Password Hash Synchronisation

Domain: Identity and Cloud Computing

Repository:
https://github.com/ANEMBHARGAV/24CC3046-P093-Azure-Hybrid-Identity

Project Status

Status: In Progress

The repository will be updated with implementation steps, configurations, screenshots, testing results, and documentation as the project progresses.
