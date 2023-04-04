<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installing osTicket on VM</h1>
This tutorial outlines the installation of osTicket the open-source help desk ticketing system .<br />

<h1>Prerequisites</h1>

- Have completed part <a href="https://github.com/TimjMerida/osTicket-pt1-VM-setup">one</a> of the 4 part tutorial
- Be connected to the Windows VM via RDP 

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)


<h2> Outline of steps</h2>
In this part we will
- Enable IIS
- Download necessary files for osTicket to run
- Register PHP in IIS
- Download osTicket 
- Assign permissions

<h2>Installation Steps</h2>

<p>
<img src="https://user-images.githubusercontent.com/128980344/229406984-b4b5c8ae-8006-4158-850e-b2c58aac5ba5.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> <img src="https://user-images.githubusercontent.com/128980344/229407872-477dbdf5-71b8-4257-9667-56f48db3643c.png" "80%" width="80%" alt="Disk Sanitization Steps"/>/> 
</p>
<p>
Before we can start downloading the files we have to enable IIS. To do so right click the start menu and click run. Type control for the contol pannel and click ok. Then go to programs and under programs and features click turn Windows features on or off. Check the box for Intenet information services and click the plus to the left. 
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/229408368-dcf30696-e77e-4cb1-b333-00ce1095558e.png" "80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://user-images.githubusercontent.com/128980344/229409125-1c2a8e0a-833d-4cd3-bde3-e3d3bd8f7a84.png" "80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
Open the dropdown for World Wide Web Services and then again for Application Development Features. Check the box for CGI and then click ok. This will allow us to install PHP manager which osTicket runs off. Once its completed click close. To test if this worked open a new tab in your VM and type 127.0.0.1. We should see a IIS webpage. 
</p>
<br />




<p>
<img src="https://user-images.githubusercontent.com/128980344/229405976-3c9e725a-40fa-438b-8d84-aa6a4ff773e5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To start downloading the necessary files osTicket needs we will have to open Microsoft Edge. Open this link in your VM's browser. These are the files we will be using. https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6. 
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/229410068-93cf103c-86a9-40df-9ca5-0c9b24524e70.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The first download is going to be PHP manager for IIS. In the download files double click PHPmanagerforIIS and click download (if it says file type might be dangerous click download anyway). Then go to file explorer and under downloads double click php manager. Click through (Click I accept when asked) until its done. then click close. Follow the same process for the rewrite file in the downloads link.
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/229669484-6869358a-fe59-4c57-83cc-430867a68957.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After these are downloaded we have to create a directory for PHP on the local hard drive. Go to the file explorer on the VM and under this pc click (c:). Create a new folder and name it PHP (you can do this by right clicking and picking new folder). This is where we will end up putting the PHP install. Now that we have the folder we can install PHP. Go to the downloads and download the PHP-7.3.8 file (download the whole file at once). Once downloaded go to downloads and right click the file. We need to extract all. Then click browse and choose the PHP folder we created under (C:). 
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/229671789-ae7d7302-8cb7-4a1f-9b20-425fdd216b43.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next download the VC_redist file. Then double click and install it.
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/229677862-67b57978-6847-4d09-b8b4-28e303392318.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After we have to download the MySql 5.5.62 file. We then have to install MySql. We will be doing a typical install. When done we want to launch the configuration wizard. We will be making credentials for MySql (write down the credentials you create). We will be doing a standard configuration. Click next and proceed to create credentials. The username is set to root (this is preset) and the password I am using is Password12321. We can click next and then execute. When done we can close.  
</p>
<br />

<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we need to register PHP in IIS. On the VM click start and search for IIS. We need to open IIS as an administrator. Right click IIS and use run as administrator.    
</p>
<br />


