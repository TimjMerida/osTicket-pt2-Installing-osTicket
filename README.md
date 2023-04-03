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
The first download is going to be PHP manager for IIS. In the download files double click PHPmanagerforIIS and click download (if it says file type might be dangerous click download anyway). Then go to file explorer and under downloads double click php manager. Click through (Click I accept when asked) until its done. then click close.
</p>
<br />

