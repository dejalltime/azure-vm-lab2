# Lab 2 – Working with Instances: An Azure VM Walkthrough

**Azure equivalent of “Working with Instances: An Amazon EC2 Walkthrough.”**

**Level:** Beginner  
**Duration:** ~1 hour

---

## Overview

In this lab, you’ll create and secure an **Azure Virtual Machine (VM)**, bootstrap it with a simple web server, and verify access via **SSH** and a **web browser**. You’ll also learn to clean up resources to avoid extra costs.

---

## Learning Objectives

- Understand core concepts of Azure Virtual Machines (VMs)
- Create and use SSH key pairs for authentication
- Configure Network Security Groups (NSGs) for SSH (22) and HTTP (80)
- Deploy and connect to an Azure VM in a default Virtual Network
- Bootstrap a VM to install a web server
- Test connectivity via SSH and browser
- Clean up all resources safely

---

## Technologies

- Azure Virtual Machines
- Virtual Network (VNet)
- Network Security Groups (NSG)
- Public IP, NIC
- Azure Portal (primary) / Azure CLI (optional)

---

## Architecture Diagram

_Add your diagram as `azure-vm-lab2.png` in the repo and embed it here:_

![Azure Lab 2 Architecture](./azure-vm-lab2.png)

---

## Cloud Lab Tasks

1. **Introduction – Getting Started**

   - Review lab goals and architecture

2. **Network & Security**

   - Create a Network Security Group (NSG) with inbound rules for SSH and HTTP
   - Generate an SSH key pair

3. **Virtual Machine**

   - Launch an Azure Virtual Machine
   - Bootstrap the VM with a simple web server
   - Test the VM via SSH and browser

4. **Conclusion – Clean Up**
   - Delete the VM and related resources

---

## Clean Up (Avoid Charges)

**Portal**

- Go to **Resource groups** → delete the lab resource group.

**CLI**

```bash
az group delete -n rg-vm-lab --yes --no-wait
```

---

## Wrap Up

- You created and configured an Azure VM.
- You hosted a simple web page and verified it.
- You safely cleaned up resources.

Congratulations — you’ve completed **Lab 2: Working with Instances: An Azure VM Walkthrough.**
