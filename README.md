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
<img src="https://user-images.githubusercontent.com/128980344/231492351-f59b0822-df6c-4a4d-b672-e09e2a29b043.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we need to register PHP in IIS. On the VM click start and search for IIS. We need to open IIS as an administrator. Right click IIS and use run as administrator. We can see URl rewrite and PHP manager we installed earlier. Open PHP manager and then register new PHP version. We will browse and go to PHP - CGI. Open it and click ok. Since we have made changes in IIS we should restart IIS. On the right under manage servers click restart.     
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/231493096-39e8dfe0-692b-4f56-968f-bcb11a9d3574.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Since we have made changes in IIS we should restart IIS. On the right under manage servers click restart.     
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/231494675-868964c9-d27d-4b2f-ac7d-4a5cfdffdd80.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we are going to download osTicket 1.15.8 from the instillation files. We then need to extract and copy the "Uploads" folder which is in the osTicket file we downloaded. We will be putting the copy int the c:\inetpub\wwwroot folder. Open a new file explorer next to the Uploads folder and go to c:\inetpub\wwwroot drag and drop the Uploads folder into its new location which will create a copy. When the file is done copying we need to rename it to osTicket * It must be named exactly osTicket to function properly * Since we made changes in IIS we need to restart the server again.       
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/231496054-01791d8f-f8bc-41a0-80fb-e9abf423dfdf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://user-images.githubusercontent.com/128980344/231496858-1f8359f8-e16d-413a-b654-eb3f91d677c3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We then are going to enable extensions for osTicket. In IIS click on server-sites-default-osTicket on the right click browse 80. We now have a osTicket webpage where we can check our extensions. Back in IIs go to PHP manager and under PHP extensions click enable or disable an extension. We need to enable php_imap.dll php_inti.dll and php_opcahe.dll. Click on them and enable on the right. When done we can refresh the webpage and we should see sone of the extensions activate.    
</p>
<br />



