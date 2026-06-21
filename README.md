# Azure Storage & Backup Lab

## Project Overview

This project demonstrates the implementation of Azure Storage and Backup services using Microsoft Azure. The objective was to design a secure cloud storage solution and implement backup protection for Azure Virtual Machines to ensure business continuity and disaster recovery readiness.

## Business Scenario

ABC Retail Solutions recently migrated its infrastructure to Microsoft Azure. The company stores important business documents, sales reports, application logs, and customer-related information

The organization faced the following challenges:

* No centralized cloud storage.
* Risk of accidental file deletion.
* No backup strategy for virtual machines.
* Potential business disruption during server failures.

As an Azure Administrator, the goal was to implement Azure Storage services and configure Azure Backup to protect critical workloads.

---

## Project Objectives

* Create and manage Azure Storage Account.
* Implement Blob Storage for unstructured data.
* Implement Azure File Share for shared file storage.
* Configure Recovery Services Vault.
* Protect Azure Virtual Machines using Azure Backup.
* Create recovery points for disaster recovery.

---

## Architecture

Resource Group

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

Resource Group:

RG-Storage-Backup-Lab

Purpose:

* Centralized resource management.
* Cost tracking.
* Access control.
* Simplified administration.
  
<img width="1918" height="891" alt="image" src="https://github.com/user-attachments/assets/d9d9a29e-feb9-4210-ae78-d432138e2b9d" />

---

### Step 2: Storage Account Creation

Created an Azure Storage Account.

Storage Account:

balastorage001

Configuration:

* Performance: Standard
* Redundancy: LRS (Locally Redundant Storage)

Purpose:

Provides the foundation for Azure storage services such as Blob Storage and Azure File Shares.

<img width="1918" height="883" alt="image" src="https://github.com/user-attachments/assets/f44c277b-94e7-414d-aed5-64b66cae12f1" />


### Step 3: Blob Storage Configuration

Created a Blob Container.

Container Name:

projectdata

Uploaded Files:

* invoice-report.txt
* application-log.txt

Purpose:

Blob Storage is used to store unstructured data such as documents, reports, images, logs, and backup files.

<img width="1918" height="887" alt="image" src="https://github.com/user-attachments/assets/85739972-b7e8-4695-86f0-d73c9c09ecf6" />

---

### Step 4: Azure File Share Configuration

Created an Azure File Share.

File Share Name:

sharedfiles

Uploaded File:

* invoice-report.txt

Purpose:

Azure File Share provides centralized shared storage accessible by multiple systems and users.

<img width="1917" height="887" alt="image" src="https://github.com/user-attachments/assets/71079a74-7c77-443e-933d-a7ef6f566d35" />

---

### Step 5: Recovery Services Vault Creation

Created a Recovery Services Vault.

Vault Name:

CompanyBackupVault

Purpose:

Acts as the centralized management service for Azure Backup and recovery operations.

<img width="1918" height="891" alt="image" src="https://github.com/user-attachments/assets/6d9e4539-7fd4-4615-8c71-534039faffca" />

---

### Step 6: Virtual Machine Backup Configuration

Created and protected the following VM:

BackupTestVM-1

Backup Configuration:

* Azure Virtual Machine Backup
* Backup Policy Applied
* Protection Enabled

Purpose:

Protects workloads against accidental deletion, corruption, and infrastructure failures.
<img width="1918" height="892" alt="image" src="https://github.com/user-attachments/assets/dfa0b995-28c2-46f8-8cd5-334563e94da5" />

---

### Step 7: Initial Backup Execution

Performed the first backup operation.

Backup Status:

* Configure Backup: Completed
* Backup: Completed

Purpose:

Created the first recovery point for disaster recovery and restoration purposes.
<img width="1918" height="880" alt="image" src="https://github.com/user-attachments/assets/c04e591d-cf6e-4aa9-b437-8561f9659a91" />

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

* Azure Storage Account management.
* Blob Storage implementation.
* Azure File Share management.
* Recovery Services Vault configuration.
* Azure Backup operations.
* Virtual Machine protection and recovery concepts.
* Disaster Recovery fundamentals in Microsoft Azure.

---

## Outcome

Successfully implemented a complete Azure Storage and Backup solution capable of storing business data, sharing files across systems, protecting Azure Virtual Machines, and supporting disaster recovery requirements through Azure Backup and Recovery Services Vault.
