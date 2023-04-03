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
Open the dropdown for World Wide Web Services and then again for Application Development Features. 
</p>
<br />




<p>
<img src="https://user-images.githubusercontent.com/128980344/229405976-3c9e725a-40fa-438b-8d84-aa6a4ff773e5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To start downloading the necessary files osTicket needs we will have to open Microsoft Edge. Open this link in your VM's browser. These are the files we will be using. https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6. 
</p>
<br />

