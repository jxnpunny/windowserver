# Standard Operating Procedure (SOP)

## jxnpunny
1414 ravelston ave w 
company name : mitt

**Version:** 1.0  
**Written by:** Jashan  
**Approved by:** Filex 
**Date:** [03/25/2025]  

---

## Purpose
The purpose of this SOP is to outline the standard procedure for preparing and configuring a Windows Server 2025. This includes installation, initial setup, networking configuration, and essential post-installation tasks. Following this SOP ensures consistency, efficiency, and reliability in server preparation.

---

## Application
This SOP applies to IT administrators and engineers responsible for deploying and managing Windows Server 2025 in a virtual or physical environment. It covers the initial setup, basic configuration, and network integration.

---

## Definitions
- **ISO:** Disk image format used for installing operating systems.
- **NIC:** Network Interface Card.
- **RAID:** Redundant Array of Independent Disks, a data storage virtualization technology.
- **DHCP:** Dynamic Host Configuration Protocol, used to assign IP addresses dynamically.
- **DNS:** Domain Name System, responsible for hostname resolution.

---

## Procedure Steps

### Step 1: Prerequisites and Resource Requirements
- **Hardware Requirements:**
  - CPU: 4 cores (minimum)
  - RAM: 16 GB (minimum)
  - Storage: 100 GB (minimum)
- **Software Requirements:**
  - Windows Server 2025 ISO
  - VMware Workstation Player or Hyper-V

### Step 2: Installation of Windows Server 2025
1. **Create a New Virtual Machine (VM):**
   - Launch **VMware Workstation Player** or **Hyper-V**.
   - Click **Create a New Virtual Machine**.
   - Select the option to use an ISO image and browse for the **Windows Server 2025 ISO**.
2. **Configure VM Settings:**
   - **VM Name:** WS2025-01 (or a name of your choice).
   - **RAM:** 16 GB (minimum).
   - **Processor:** 4 cores.
   - **Storage:** 100 GB (minimum).
   - **Network:** Choose **Bridged** or **NAT** mode, depending on your network setup.
3. **Install Windows Server 2025:**
   - Power on the VM.
   - Select **Language**, **Time**, and **Keyboard settings**.
   - Click **Install Now**.
   - Choose **Windows Server 2025 Standard (Desktop Experience)**.
   - Accept the license terms.
   - Select **Custom: Install Windows only**.
   - Choose the primary disk, format it, and proceed with the installation.

### Step 3: Initial Server Configuration
1. **Set the Administrator Password:**
   - After the installation is complete, you will be prompted to set an Administrator password.
   - Choose a strong password (minimum 8 characters, including uppercase, lowercase, numbers, and symbols).
   - Confirm the password and log in.
2. **Configure Basic Server Settings:**
   - **Rename the Computer:**
     - Go to **Settings > System > About**.
     - Click **Rename this PC**.
     - Enter the name `WS2025-01` (or your preferred naming convention).
     - Restart the server.
   - **Time Zone Configuration:**
     - Go to **Settings > Time & Language > Date & Time**.
     - Select the appropriate time zone.
   - **Windows Activation:**
     - Go to **Settings > Update & Security > Activation**.
     - Enter the product key and activate Windows.

### Step 4: Network Configuration
1. **Assign a Static IP Address:**
   - Go to **Settings > Network & Internet > Ethernet**.
   - Click **Change adapter options**.
   - Right-click the NIC > **Properties**.
   - Select **Internet Protocol Version 4 (TCP/IPv4)** > **Properties**.
   - Configure the following:
     - **IP Address:** 192.168.1.10
     - **Subnet Mask:** 255.255.255.0
     - **Default Gateway:** 192.168.1.1
     - **Preferred DNS:** 8.8.8.8
   - Click **OK** and **Close**.
2. **Verify Network Connectivity:**
   - Open **Command Prompt**.
   - Run `ipconfig` to verify the IP configuration.
   - Run `ping 192.168.1.1` to test connectivity with the gateway.

### Step 5: Post-Installation Tasks
1. **Windows Updates:**
   - Go to **Settings > Update & Security**.
   - Click **Check for updates**.
   - Install all available updates and restart the server if necessary.
2. **Install Server Roles and Features:**
   - Open **Server Manager**.
   - Click **Manage > Add Roles and Features**.
   - Select **Role-based or feature-based installation**.
   - Choose the local server.
   - Select and install the required roles, such as:
     - **Active Directory Domain Services (AD DS)**.
     - **DNS Server**.
     - **File and Storage Services**.
   - Complete the installation and reboot if prompted.
3. **Backup Configuration:**
   - Open **Windows Server Backup** (install the feature if not already present).
   - Select **Local Backup > Backup Schedule**.
   - Choose the backup items (system state, full server, or custom).
   - Set the schedule (e.g., daily at 2 AM).
   - Select the backup destination.
   - Confirm and finish the configuration.

---

## Resources
- Windows Server 2025 ISO
- VMware Workstation Player or Hyper-V
- Administrator credentials
- Network configuration details

---
