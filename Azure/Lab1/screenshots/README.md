☁️ Azure Lab: Setting Up and Managing Windows VMs

This lab demonstrates how to provision, configure, and access two virtual machines (VMs) on Microsoft Azure: one running Windows Server 2019 and another with Windows 10. The goal is to become familiar with Azure VM provisioning and RDP access from macOS

📖 Lab Overview

| Component   | Configuration                    |
| ----------- | -------------------------------- |
| VM 1        | Windows Server 2019 Datacenter   |
| VM 2        | Windows 10 Pro                   |
| Platform    | Microsoft Azure (Free Tier)      |
| RDP Client  | Microsoft Remote Desktop (macOS) |
| Host Device | MacBook (Intel-based)            |


📝 Step-by-Step Workflow

1. Provisioning the Virtual Machines

* Create two separate VMs:

* VM 1: Windows Server 2019 Datacenter 

* VM 2: Windows 10 Pro

* Choose default settings for networking (allow RDP port 3389)

* Assign a username and password for both VMs

* Allow Azure to assign public IPs for RDP access

![Server 2019 setup](/Azure/Lab1/screenshots/azuresetup1.png)
![Windows 10 setup](/Azure/Lab1/screenshots/azuresetup2.png)

2. Accessing VMs via RDP on macOS

* Download the .rdp file for each VM

* Install Windows app from the Mac App Store

* Double-click each .rdp file, then log in with the VM credentials

* Successfully establish RDP sessions for both VMs

![Server 2019](/Azure/Lab1/screenshots/server2019.png)
![Windows 10](/Azure/Lab1/screenshots/windows10.png)

3. Initial configuration within the OS

* Rename each computer

* Adjust Date and Time settings for local timezone

![Renamed Server 2019](/Azure/Lab1/screenshots/renameserver.png)
![Renamed Windows 10](/Azure/Lab1/screenshots/renamedesktop.png)

🛠️ Troubleshooting: Login issue after renaming Windows Server 2019

* After renaming the Windows Server 2019 machine and restarting, I received a login error

* Fix: Edited the .rdp file settings in Azure and changed the local machine OS to macOS 

![Renamed Server 2019](/Azure/Lab1/screenshots/error.png)
![Renamed Windows 10](/Azure/Lab1/screenshots/troubleshoot.png)