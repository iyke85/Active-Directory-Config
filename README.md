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

![Screenshot 2024-05-26 154341](https://github.com/iyke85/Active-Directory-Config/assets/159981310/8d45e979-cc18-4de0-a417-75134359c6e9)


 Ensure Connectivity Between Client and Domain Controller
 
 Test Connectivity:

Logged into Client-1 via Remote Desktop.
Performed a continuous ping (ping -t <DC-1_private_IP_address>) to DC-1's private IP address to check connectivity. 

Enable ICMPv4 on DC-1:

Logged into DC-1 and enabled ICMPv4 through the local Windows Firewall.
Verified successful ping responses from Client-1.

![Screenshot 2024-05-26 154902](https://github.com/iyke85/Active-Directory-Config/assets/159981310/362c3e37-22b8-4c88-a07e-befcc64e7e70)

![Screenshot 2024-05-26 155645](https://github.com/iyke85/Active-Directory-Config/assets/159981310/f2045f33-f824-4b67-b950-e772155a1e4d)

![DC-1 PING SUCCESSFUL](https://github.com/iyke85/Active-Directory-Config/assets/159981310/5889b1c0-c49f-483d-ab40-40d58813568e)



- Install Active Directory
1. Install AD DS:

Logged into DC-1 and installed Active Directory Domain Services (AD DS).
Promoted DC-1 to a Domain Controller by setting up a new forest named iyke27.com.
Restarted DC-1 and logged back in as iyke27.com\OLA_ADMIN.
2. Create User Accounts in AD:

Created an Organizational Unit (OU) named _EMPLOYEES in Active Directory Users and Computers (ADUC).
Created another OU named _ADMINS.
Created a new user Olachi Onwuanaibe with the username OLA_ADMIN and added her to the Domain Admins security group.
Logged out and logged back in as iyke27.com\OLA_ADMIN.

![INSTALL AD](https://github.com/iyke85/Active-Directory-Config/assets/159981310/717ae47d-dc24-4121-9a96-d132b035f4c6)

![AD 2](https://github.com/iyke85/Active-Directory-Config/assets/159981310/06a70675-eb35-4c7d-8e49-b4dc1f2343c4)


![OLA_ADMIN](https://github.com/iyke85/Active-Directory-Config/assets/159981310/49fbe99b-4d1b-44b8-9cbc-0011f0c21c63)

![OLA DOMAIN WELCOM](https://github.com/iyke85/Active-Directory-Config/assets/159981310/87163af2-3956-46ca-9767-16a62748ff53)

<h2>
</h2>

<h2>Deployment and Configuration Steps</h2>

Join Client-1 to the Domain

1. Configure DNS Settings:

Set Client-1’s DNS settings in Azure to point to DC-1's private IP address.
Restarted Client-1 from the Azure Portal.

2. Join Domain:

Logged into Client-1 as the local admin (OLA_ADMIN) and joined it to the domain iyke27.com.
Verified that Client-1 appeared in ADUC under the Computers container.
Moved Client-1 to a new OU named _CLIENTS for organizational purposes.

Setup Remote Desktop for Non-Administrative Users

1. Allow Remote Desktop Access:

Logged into Client-1 as mydomain.com\OLA_ADMIN.
Opened system properties and configured Remote Desktop settings to allow domain users access.
Verified the ability to log into Client-1 as a non-administrative user.



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
