# Standard Operating Procedure (SOP)

## jashandeep singh
130 Henlow Bay 
MITT 

**Version:** 1.0  
**Written by:** Jashan  
**Approved by:** Filex  
**Date:** 03/26/2025  

---

## Purpose
This SOP is the procedure for creating Windows Server 2025, Which inckudes installation, basic setup, and networking.

---

## Application
Applies to IT administrators who are deploying Windows Server 2025 in virtual environment to test  or physical environments.

---

## Definitions
- **ISO:** Disk image format for OS installation.
- **NIC:** Network Interface Card.
- **DNS:** Domain Name System for hostname resolution.

---

## Procedure Steps

### Step 1: Prerequisites
- **Hardware:** 4-core CPU, 16 GB RAM, 100 GB storage.
- **Software:** Windows Server 2025 ISO, VMware Workstation Player.

### Step 2: Installation
1. **Create VM:**
   - Launch VMware, create a new VM, and attach the ISO.
   - Assign 16 GB RAM, 4 cores, and 100 GB storage.
2. **Install Server:**
   - Boot from ISO, select **Windows Server 2025 Standard**.
   - Follow the wizard, format the disk, and complete the installation.

### Step 3: Initial Setup
1. **Set Admin Password:** Create a strong password.
2. **Rename Server:** Change name to `WS2025-01` and restart.
3. **Time Zone:** Set the correct region.
4. **Activate Windows:** Enter the product key.

### Step 4: Network Configuration
1. **Assign Static IP:**
   - Go to **Ethernet Settings > Adapter Options**.
   - Set IP: `192.168.1.10`, Mask: `255.255.255.0`, Gateway: `192.168.1.1`.
2. **Test Connectivity:** Use `ipconfig` and `ping` commands.

### Step 5: Post-Installation
1. **Windows Updates:** Install all updates.
2. **Install Roles:**
   - Open **Server Manager**.
   - Add roles: **AD DS**, **DNS Server**, **File Services**.
3. **Backup:** Configure regular backups using **Windows Server Backup**.

---

## Resources
- Windows Server 2025 ISO
- VMware Workstation Player
- Network configuration details

---

✅ **End of SOP**
