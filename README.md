<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Tenant created on Azure.portal.com
- Subscription to Azure
- Create Resource Groups
- Create Virtual Network and Subnet
- Create Virtual Machine (Windows)

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/hTFSLnz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 1: CREATE A RESOURCE GROUP</h2>

  - Go to portal.Azure.com and create a tenant and free subscription.
  - After that you are able to create a resource group.
  - Search "Resource Groups" in the search bar and select it.
  - Next select "Create Resource Group"
  - Name Resource Group "RG-osTicket" and select the appropriate region.
  - Then select "review + create"
</p>
<br />

<p>
<img src="https://i.imgur.com/okBCM6x.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
  <p>
<img src="https://i.imgur.com/zrtCMo4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
</h2>STEP 2: CREATE A VIRTUAL MACHINE</h2>

  - Go to portal.Azure.com
  - Search "Virtual Machines" in the search bar and select it.
  - Next select "Create - Azure Virtual Machine"
  - Select the Resource Group "RG-osTicket"
  - Name the Virtual Machine "VM-osTicket" and select the appropriate region (make sure it matches the Resource Group Region)
  - For Image select "Windows 10 Pro"
  - For Size Select Standard_D4s_v3 - 4 vcpus, 16 GiB memory
  - Create a Username and Password (make sure to make note or remember this)
  - Under Licensing make sure to check the box
  - Go to Next: Disks --> Go to Next: Networking
  - In "Networking" it will automatically create a Virtual Network and Subnet
  - Then Select "Review + Create"
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
