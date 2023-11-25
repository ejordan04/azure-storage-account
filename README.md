<p align="center">
<img src="https://i.imgur.com/VKW4EGV.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Creating a Storage Account in Microsoft Azure</h1>
This tutorial outlines a step-by-step process for deploying a storage account in Azure.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure 

- Microsoft Azure Storage Accounts

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)

<h2>Objectives</h2>

- Create a Resource Group
- Deploy a Storage Account 
- Add a Container within the Storage Account
- Upload/Edit a File inside the Container 

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/KK6b2H7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a resource group in Azure by searching "Resource Group" in the search bar at the top of the web page. Next, click "Create" located in the upper left corner. Name your resource group and then click "Review and Create" at the bottom. 
</p>
<br />

<p>
<img src="https://i.imgur.com/wltSUAd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Search "Storage Accounts" in the same search bar as before. Select "Create". Put the Storage Account in the Resource Group created from the previous step. Give the Storage account a name. Click "Review" and then "Create".
</p>
<br />

<p>
<img src="https://i.imgur.com/JP3fxtO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Let's now log in to DC-1 and install Active Directory Domain Services. When the installation is complete, promote it as a DC. Then setup a new forest to anything you want. I'll be calling my domain example.com. After that, restart the VM and log back into DC-1 using the new domain (example.com\user)
</p>
<br />

<p>
<img src="https://i.imgur.com/PGHftGO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we're going to create an admin and normal user account in Active Directory. Under the tools tab in Server Manager, click Active Directory Users and Computers (ADUC) and then create an Organizational Unit (OU) called _EMPLOYEES. Also, create a new OU named _ADMINS. We'll create a new employee named Jane Doe with the username of jane_admin. Next, we'll add jane_admin to the Domain Admins Security Group, and once that's done we'll log out and log back in with example.com\jane_admin.
</p>
<br />
