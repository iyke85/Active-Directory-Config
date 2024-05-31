<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>  Active Directory Deployed in the Cloud (Azure)</h1>
This project involves setting up a basic Active Directory (AD) environment in Azure, including creating and configuring virtual machines (VMs), establishing network connectivity, configuring AD services, and managing user accounts. The goal is to demonstrate proficiency in deploying and managing a Windows Server environment with Active Directory in a cloud infrastructure.<br />
<h2>Environments and Technologies Used</h2>
- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

 Create the Domain Controller VM:

VM Name: DC-1
OS: Windows Server 2022
Configuration:
Created a new Resource Group and Virtual Network (VNet) during VM creation.
Set the NIC Private IP address of DC-1 to static.
![image](https://github.com/iyke85/Active-Directory-Config/assets/159981310/501948f7-50b9-4553-8dda-fa6bf5eacd31)


 Create the Client VM:

VM Name: Client-1
OS: Windows 10
Configuration:
I used the same Resource Group and VNet created for DC-1.
Ensured both VMs were in the same VNet (verified using Network Watcher).


![Screenshot 2024-05-26 154341](https://github.com/iyke85/Active-Directory-Config/assets/159981310/753367dd-f62b-4c98-a0cc-aa19242e91ed)



- Step 3
- Step 4

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
