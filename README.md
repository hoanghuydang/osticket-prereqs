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
<img src="https://i.imgur.com/BItyj2p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 6: DOWNLOAD AND INSTALL REWRITE MODULE</h2>

  - Google and Download IIS URL Rewrite Module 2
</p>
<br />

 <p>
<img src="https://i.imgur.com/CsF40tk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 7: CREATE THE DIRECTORY C:\PHP</h2>

  - In your Windows virtual machine go to the bottom left search bar and type "File Explorer"
  - Click on "This PC"
  - Click on the Windows (C:)
  - In Windows (C:) right click, then click "New", then click "Folder" and Name is PHP.
</p>
<br />

 <p>
<img src="https://i.imgur.com/FX6S70C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 8: DOWNLOAD PHP 7.3.8 & UNZIP THE CONTENTS INTO PHP FOLDER</h2>

  - Google and Download PHP 7.3.8.
  - After download is finished right click the php zip file and "Extract All"
  - Select "Browse" --> "This PC" --> Windows (C:) --> PHP and click "Select Folder"
  - Select "Extract" and contents will be unzipped into the PHP file.
</p>
<br />

 <p>
<img src="https://i.imgur.com/YKpMsef.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 9: DOWNLOAD AND INSTALL VC_redist.86.exe</h2>

  - Google and Download VC_redist.8.exe
</p>
<br />

<p>
<img src="https://i.imgur.com/7snmuV6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 10: DOWNLOAD AND INSTALL MySQL 5.5.62</h2>

  - Google and Download MySQL 5.5.62
  - Agree to terms - check the box
  - Choose Set Up Type - "Select" Typical and install
  - For the MySQL wizard configuration click "Next"
  - Select "Standard Configuration" --> "Next" 
  - Create a MySQL password for Root user, then click next
  - Select "Execute" to install a database onto the VM
</p>
<br />

<p>
<img src="https://i.imgur.com/fWlcBGb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  <p>
<img src="https://i.imgur.com/79oxpNr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  <p>
<img src="https://i.imgur.com/nFAGdwC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 11: Open IIS as an Admin</h2>

  - In the Windows VM search in the bottom left "ISS" and right click it and "Run as administrator"
  - Click on "PHP Manager" and "Register new PHP Version"
  - Browse --> PHP Folder --> php-cgi then select that file
  - Go back to ISS and click "restart" near the green icon on the right
</p>
<br />

<p>
<img src="https://i.imgur.com/afjVZAM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/4eeLKxX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/0JcUqps.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/AOC0sAX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 12: DOWNLOAD OSTICKET</h2>

  - Google and Download osTicket
  - Extract and copy "upload folder to c:\inetpub\root
  - Within c:\inet\www.root, Rename upload to osTicket
  - Restart the ISS Server
  - In the ISS Server go on the left to expand the vm-osticket --> expand "Sites" --> expand "Default Web Site" --> Select osTicket
  - Then on the Rght click "Browse*80"
  - You should be able to see the osTicket Installer like the image above
  - Now go back to ISS go back to the osTicket Folder and click "PHP Manager"
  - Click "Enable or disable an extension"
  - Enable: php_imap.dll
  - Enable: php_intl.dll
  - Enable: php_opache.dll
  - Refresh the osTicket site int your browser, observe the changes
</p>
<br />

<p>
<img src="https://i.imgur.com/8AniI5r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 13: RENAME: ost-config.php </h2>

  - From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
  - To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>
<br />

<p>
<img src="https://i.imgur.com/XYUWz9r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 14: ASSIGN PERMISSIONS: OST-CONFIG.PHP</h2>

  - Right click the ost-config.php file and select properties 
  - Then Security --> Advanced
  - Then Disable inheritance --> Remove All
  - New Permissions --> Everyone --> All
  - Now everyone has permissions to ost-config.php
</p>
<br />

 <p>
<img src="https://i.imgur.com/z6VvP49.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 15: CONTINUE SETTING UP OSTICKET IN THE BROWSER</h2>

  - Name Helpdesk
  - Default email (receives email from customers)
  - Fill out information, make note or remember the credentials
</p>
<br />

 <p>
<img src="https://i.imgur.com/YKpMsef.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</h2>STEP 16: DOWNLOAD AND INSTALL VC_redist.86.exe</h2>

  - Google and Download VC_redist.8.exe
</p>
<br />
