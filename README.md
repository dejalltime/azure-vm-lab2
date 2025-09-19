# Lab 2 – Working with Instances: An Azure VM Walkthrough

**Azure equivalent of “Working with Instances: An Amazon EC2 Walkthrough.”**

**Level:** Beginner  
**Duration:** ~1 hour

---

## Overview

In this lab, you’ll create and secure an **Azure Virtual Machine (VM)**, configure network access, and deploy a simple web server.  
You’ll test access via **SSH** and the **browser**, and then clean up all resources.

---

## AWS → Azure Mapping

| AWS Service / Concept          | Azure Equivalent                |
| ------------------------------ | ------------------------------- |
| Amazon EC2 (virtual server)    | Azure Virtual Machine (VM)      |
| Amazon EBS (block storage)     | Azure Managed Disk              |
| EC2 Instance Connect (SSH web) | Azure Bastion / Serial Console  |
| EC2 Security Group             | Network Security Group (NSG)    |
| Default VPC + Subnet           | Virtual Network (VNet) + Subnet |
| Availability Zone              | Azure Availability Zone         |
| AWS Region                     | Azure Region                    |

---

## Learning Objectives

By the end of this lab, you will:

- Understand **Azure Virtual Machines** and supporting resources
- Learn how to create and use **SSH keys** for authentication
- Configure **NSGs** for secure SSH (22) and HTTP (80) access
- Deploy an **Azure VM** with a **Managed Disk** in a **VNet/Subnet**
- Test VM connectivity via **Azure Bastion (SSH)** and **browser**
- Clean up resources to avoid extra costs

---

## Technologies

- Azure Virtual Machines
- Managed Disks
- Virtual Network (VNet) & Subnet
- Network Security Group (NSG)
- Public IP, NIC
- Azure Bastion
- NGINX Web Server

---

## Architecture Diagram

**Azure Lab 2 Architecture**

The setup consists of:

- **Client** (browser/SSH client)
- **Azure Bastion** for SSH/HTTP access to the VM
- **Azure VM** running NGINX
- **Managed Disk** attached to the VM
- **NSG** allowing inbound SSH (22) and HTTP (80)
- **VNet & Subnet** providing network isolation
- **Availability Zone** within an **Azure Region**

_Add your diagram as `azure-vm-lab2.png` and embed it here:_

![Azure Lab 2 Architecture](./azure-vm-lab2.png)

---

## Cloud Lab Tasks

### 1. Introduction – Getting Started

- Review lab goals and architecture

### 2. Network & Security

- Create a **Network Security Group (NSG)**
- Generate or upload an **SSH key pair**

### 3. Virtual Machine

- Create an **Azure VM** in the chosen region & availability zone
- Attach a **Managed Disk** (default)
- Install **NGINX** (manual install via SSH or using a startup script)
- Test VM connectivity:
  - **SSH** via Bastion
  - **HTTP** via browser

### 4. Conclusion – Clean Up

- Delete the VM, NSG, VNet, and resource group

---

## Clean Up (Avoid Charges)

**Azure Portal**

- Delete the resource group used for the lab.

**CLI**

```bash
az group delete -n rg-vm-lab --yes --no-wait
```

---

## Wrap Up

- You created and secured an **Azure Virtual Machine**.
- You deployed **NGINX** and tested connectivity via **SSH** and **browser**.
- You mapped AWS concepts to Azure equivalents.
- You safely cleaned up resources.

Congratulations — you’ve completed **Lab 2: Working with Instances: An Azure VM Walkthrough.**
