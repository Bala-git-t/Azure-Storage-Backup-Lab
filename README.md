# Azure Storage & Backup Lab

## Project Overview

This project demonstrates the implementation of Azure Storage and Backup services using Microsoft Azure. The objective was to design a secure cloud storage solution and implement backup protection for Azure Virtual Machines to ensure business continuity and disaster recovery readiness.

---

## Business Scenario

ABC Retail Solutions recently migrated its infrastructure to Microsoft Azure. The company stores important business documents, sales reports, application logs, and customer-related information.

The organization faced the following challenges:

* No centralized cloud storage
* Risk of accidental file deletion
* No backup strategy for virtual machines
* Potential business disruption during server failures

As an Azure Administrator, the goal was to implement Azure Storage services and configure Azure Backup to protect critical workloads.

---

## Project Objectives

* Create and manage Azure Storage Account
* Implement Blob Storage for unstructured data
* Implement Azure File Share for shared file storage
* Configure Recovery Services Vault
* Protect Azure Virtual Machines using Azure Backup
* Create recovery points for disaster recovery

---

## Architecture

```text
RG-Storage-Backup-Lab
│
├── Storage Account (balastorage001)
│
├── Blob Container (projectdata)
│   ├── invoice-report.txt
│   └── application-log.txt
│
├── Azure File Share (sharedfiles)
│   └── invoice-report.txt
│
├── Recovery Services Vault
│   └── CompanyBackupVault
│
└── Virtual Machine
    └── BackupTestVM-1
```

---

## Technologies Used

* Microsoft Azure
* Azure Storage Account
* Azure Blob Storage
* Azure File Share
* Recovery Services Vault
* Azure Backup
* Azure Virtual Machine

---

## Implementation Steps

### Step 1: Resource Group Creation

Created a Resource Group to organize and manage all resources related to the Storage and Backup project.

**Resource Group:**

RG-Storage-Backup-Lab

**Purpose:**

* Centralized resource management
* Cost tracking
* Access control
* Simplified administration

### Screenshot


<img width="1915" height="876" alt="image" src="https://github.com/user-attachments/assets/02c8627a-2b49-4b5c-9009-985c2c3e943d" />

---

### Step 2: Storage Account Creation

Created an Azure Storage Account.

**Storage Account:**

balastorage001

**Configuration:**

* Performance: Standard
* Redundancy: LRS (Locally Redundant Storage)

**Purpose:**

Provides the foundation for Azure storage services such as Blob Storage and Azure File Shares.

### Screenshot

<img width="1918" height="875" alt="image" src="https://github.com/user-attachments/assets/1c7503ee-6dea-449d-8d3d-ef20400f3e92" />


---

### Step 3: Blob Storage Configuration

Created a Blob Container.

**Container Name:**

projectdata

**Uploaded Files:**

* invoice-report.txt
* application-log.txt

**Purpose:**

Blob Storage is used to store unstructured data such as documents, reports, images, logs, and backup files.

### Screenshot

<img width="1918" height="900" alt="image" src="https://github.com/user-attachments/assets/ed742bfb-8d66-4d58-810c-e9a2e6cdcdd9" />

---

### Step 4: Azure File Share Configuration

Created an Azure File Share.

**File Share Name:**

sharedfiles

**Uploaded File:**

* invoice-report.txt

**Purpose:**

Azure File Share provides centralized shared storage accessible by multiple systems and users.

### Screenshot

<img width="1918" height="872" alt="image" src="https://github.com/user-attachments/assets/1faee82c-c1ca-4742-b5b7-54395256a2a9" />


---

### Step 5: Recovery Services Vault Creation

Created a Recovery Services Vault.

**Vault Name:**

CompanyBackupVault

**Purpose:**

Acts as the centralized management service for Azure Backup and recovery operations.

### Screenshot

<img width="1915" height="880" alt="image" src="https://github.com/user-attachments/assets/2da2e735-f18f-4b53-9007-ed1bb1a7f576" />


---

### Step 6: Virtual Machine Backup Configuration

Created and protected the following VM:

**BackupTestVM-1**

**Backup Configuration:**

* Azure Virtual Machine Backup
* Backup Policy Applied
* Protection Enabled

**Purpose:**

Protects workloads against accidental deletion, corruption, and infrastructure failures.

### Screenshot

<img width="1918" height="893" alt="image" src="https://github.com/user-attachments/assets/4076b18a-2787-495c-b85b-e808e1ff52f0" />

---

### Step 7: Initial Backup Execution

Performed the first backup operation.

**Backup Status:**

* Configure Backup: Completed
* Backup: Completed

**Purpose:**

Created the first recovery point for disaster recovery and restoration purposes.

### Screenshot

<img width="1918" height="877" alt="image" src="https://github.com/user-attachments/assets/029ac904-c048-452f-b73d-b0fb0e1ea46a" />

---

## Validation

Successfully verified:

✔ Storage Account creation

✔ Blob Container creation

✔ File uploads to Blob Storage

✔ Azure File Share creation

✔ File upload to Azure File Share

✔ Recovery Services Vault creation

✔ Backup policy assignment

✔ VM protection enabled

✔ Initial backup completed successfully

---

## Key Learnings

Through this project, I gained hands-on experience with:

* Azure Storage Account management
* Blob Storage implementation
* Azure File Share management
* Recovery Services Vault configuration
* Azure Backup operations
* Virtual Machine protection and recovery concepts
* Disaster Recovery fundamentals in Microsoft Azure

---

## Outcome

Successfully implemented a complete Azure Storage and Backup solution capable of storing business data, sharing files across systems, protecting Azure Virtual Machines, and supporting disaster recovery requirements through Azure Backup and Recovery Services Vault.
