# Azure Virtual Machine & Azure File Share Assignment

**Student:** Mohammad Arab  
**Cloud Platform:** Microsoft Azure  
**Operating System:** Windows Server 2025 Datacenter  
**Region:** North Europe

## 1. Project Overview

The objective of this project was to gain practical experience with Microsoft Azure by deploying a Windows Server virtual machine, connecting to it remotely, and configuring shared cloud storage using Azure Files.

The project also focused on troubleshooting deployment and connectivity issues and managing cloud resources.

## 2. Technologies Used

- Microsoft Azure
- Azure Virtual Machines
- Windows Server 2025 Datacenter
- Azure Resource Groups
- Azure Storage Accounts
- Azure Files
- Remote Desktop Protocol (RDP)
- Windows PowerShell
- GitHub

## 3. Creating the Resource Group

I created a resource group named `MohammadArab_RG` to organize the Azure resources used in this assignment.

The resource group contains the virtual machine and associated resources, including networking and storage services.

## 4. Creating the Virtual Machine

I deployed a Windows Server 2025 Datacenter virtual machine using the Azure Portal.

**Configuration:**

| Setting | Configuration |
|---|---|
| Virtual Machine Name | MohammadArab_VM |
| Operating System | Windows Server 2025 Datacenter |
| Region | North Europe |
| VM Size | Selected during deployment |
| Authentication | Administrator username and password |
| Remote Access | RDP (Port 3389) |

After validating the configuration, I deployed the virtual machine and verified that it was running.

## 5. Connecting to the Virtual Machine

I connected to the virtual machine using Remote Desktop Protocol (RDP).

Steps performed:

1. Opened the virtual machine in the Azure Portal.
2. Selected the RDP connection option.
3. Downloaded the RDP connection file.
4. Opened the file on my local Windows computer.
5. Entered the administrator credentials.
6. Successfully accessed the Windows Server 2025 desktop.

**Result:** Remote access to the Azure virtual machine was successful.

## 6. Creating Azure File Share

I created an Azure Storage Account and configured an Azure File Share named `assignment-share`.

I used the Azure Portal to generate the Windows PowerShell connection script.

The file share was connected to:

- The Azure Windows Server virtual machine.
- My local Windows computer.

The shared storage was mapped as network drive `Z:`.

## 7. Testing File Sharing

To verify the connection, I created a text file named `Azure-Test.txt` in the shared drive.

I accessed the same file from both the local computer and the Azure virtual machine.

**Result:** The file was successfully accessible from both systems, demonstrating that the Azure File Share connection was working.

## 8. Problems Encountered and Solutions

### Problem 1: Azure Region Restriction

**Error:** The selected region was not accepting new customers.

**Solution:** I changed the virtual machine deployment region from West Europe to North Europe.

**Result:** The virtual machine deployment validation succeeded.

### Problem 2: Network Drive Not Visible

**Problem:** The Azure File Share network drive was not visible on my local computer.

**Troubleshooting:**

I tested connectivity to Azure Files using PowerShell:

`Test-NetConnection mohammadfiles2025.file.core.windows.net -Port 445`

The test returned `TcpTestSucceeded : True`.

I also used `net use` to check existing network drive connections.

**Solution:** I reconnected the Azure File Share using the PowerShell connection script from the Azure Portal.

**Result:** The network drive became accessible from my local computer.

## 9. Screenshots

Screenshots documenting the virtual machine deployment, remote desktop connection, Azure File Share configuration, and file-sharing test are included in the project repository.

## 10. Conclusion

This assignment provided practical experience with Microsoft Azure cloud infrastructure.

I learned how to deploy and access a Windows Server virtual machine, configure Azure Files, connect shared cloud storage to multiple computers, and troubleshoot deployment and networking issues.

The project improved my understanding of cloud computing, virtual machines, remote access, and cloud storage management.
