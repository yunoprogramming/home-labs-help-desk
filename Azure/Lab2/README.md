☁️ Azure Lab: Windows Server 2022 (AD, DHCP, DNS, Printer Services)

This lab demonstrates deploying a Windows Server 2022 VM in Azure, assigning a static IP, connecting via Azure Bastion, and configuring core server roles: Active Directory Domain Services, DHCP, DNS, and Print Services

📖 Lab Overview

| Component            | Configuration                                 |
| -------------------- | --------------------------------------------- |
| Azure VM             | Windows Server 2022 Datacenter                |
| Connectivity         | Azure Bastion (no public IP required for RDP) |
| Static IP assignment | Private IP set on NIC-level                   |
| Server Roles         | AD DS, DNS, DHCP, Print & Document Services   |

📝 Step-by-Step Workflow

1. Provision VM in Azure

* Navigate to Azure Portal → Virtual Machines → Create a VM

* Select Windows Server 2022 Datacenter: Azure Edition Hotpatch - x64 Gen2 with size (e.g. Standard_E2s_v6 - 2 vcpus, 16 GiB memory)

* No need to allow RDP port since we're using Azure Bastion to connect to this VM

![Server 2022 setup](/Azure/Lab2/Screenshots/createvm.png)

2. Assign Static Private IP

* Access your VM’s Network settings → IP Configurations → ipconfig1

* Change from Dynamic to Static, and assign a private IP within the subnet range or leave as default. Azure will restart NIC to apply

![Assign Static Private IP](/Azure/Lab2/Screenshots/ipconfig.png)

3. Connect Using Azure Bastion

* Deploy Azure Bastion from your Vm settings via Connect → Bastion → Deploy

* Use Bastion to connect to your VM securely (no public IP needed) through the Azure Portal

![Server 2022](/Azure/Lab2/Screenshots/server2022.png)

4. Install Server Roles & Features

* Open Server Manager → Manage → Add Roles and Features.

* Choose Role-based installation → select your local server.

* Select and install the following roles (click add features when prompted):

* Active Directory Domain Services
* DNS Server
* DHCP Server
* Print and Document Services
* Web Server (IIS)

![Adding roles and features](/Azure/Lab2/Screenshots/addroles.png)
![Server Manager](/Azure/Lab2/Screenshots/servermanager.png)
![Roles and features](/Azure/Lab2/Screenshots/roles.png)