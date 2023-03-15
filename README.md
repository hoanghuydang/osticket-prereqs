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
- Microsoft Remote Desktop

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
  - Then after validation click "create"
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
<img src="https://i.imgur.com/IqBd3Nz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
  <p>
<img src="https://i.imgur.com/3NQ1U4j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 3: REMOTE DESKTOP INTO YOUR VIRTUAL MACHINE</h2>

  - Go to portal.Azure.com 
  - Search and click on "Virtual Machines" - then select the VM-osTicket
  - On the right side you can find the public IP address, copy it
  - Next open Microsoft Remote Desktop and add a PC - Paste the IP address and use the same username and login that was created when creating the VM 
</p>
<br />

 <p>
<img src="https://i.imgur.com/rFL3fXX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
   <p>
<img src="https://i.imgur.com/JHRsjwb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</h2>STEP 4: INSTALL/ENABLE IIS IN WINDOWS</h2>

  - In your Virtual Machine, on the bottom left search "Control Panel" 
  - Select "Programs" then select "Turn Windows features on and off"
  - You will Find "Internet Information Services" make sure to check it, and click the + icon to expand it
  - Then find "World Wide Web Services" expand that.
  - Then find "Application Development Features" expand that and make sure to check CGI.
  - Install CGI and wait for it to finish
  - To test that our web server is working open a new tab and open 127.0.0.1 it should load the default IIS server
  - You should have an image like the one above.
</p>
<br />

 <p>
<img src="https://i.imgur.com/QgHePV7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 5: DOWNLOAD PHP MANAGER FOR IIS</h2>

  -  Google and Download Microsoft PHP Manager</p>
<br />

 <p>
<img src="https://i.imgur.com/3NQ1U4j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 6: DOWNLOAD AND INSTALL REWRITE MODULE</h2>

  - Go to portal.Azure.com 
  - Search and click on "Virtual Machines" - then select the VM-osTicket
  - On the right side you can find the public IP address, copy it
  - Next open Microsoft Remote Desktop and add a PC - Paste the IP address and use the same username and login that was created when creating the VM 
</p>
<br />
