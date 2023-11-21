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

- Install IIS with CGI
- Download and install PHP Manager for IIS, Rewrite Module, PHP, VC Redist, and MYSQL
- IIS Configuration
- Install and set up osTicket
- Item 5

<h2>Installation Steps</h2>

This project is all completed within an Azure Virtual Machine running Windows 10, and created with default settings.

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/62bc8ec1-674c-4103-84d0-1b5988db89b2)

<p>
  <h3>Step 1: Install IIS with CGI</h3>
  
  - Press 'Windows Key + R' to open the Run dialog box, and enter "optionalfeatures" 
  
  
![image](https://github.com/anbere/osticket-prereqs/assets/90169033/e7d4e11a-856e-44cc-b25b-04238063bf08)

  - Find and check "Internet Information Services", then continue to make sure every highlighted 
    option is checked on your machine.

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/1cb30f60-7983-41f1-b128-a07bd8633e9d)

  - After pressing 'OK', Windows will begin to Install the IIS Web Server. Once complete we can verify it was succesful by using our browser to navigate to '127.0.0.1'. The following landing page should be displayed:

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/62612d84-0960-4686-9562-74d0c5c0877e)

  <h2>Congratulations, you completed Step 1!</h2>
</p>
<br />

<p>
  <h3>Step 2: Downloading and Installing</h3>

  - We will be using this Google Drive [link](https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) for our installation files.
  - Start by downloading and installing (1) PHPManagerForIIS, the (2) Rewrite Module and (3) Microsoft Visual C++ Redistributable, accepting their license and conditions.

| ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/99c45e69-3360-4c10-af15-d57a195b260a)
|:--:| 
|*Use this image and numbering for reference in the entire install step*|

Download the (4) PHP folder. Create an empty folder in the C Drive named 'PHP'. Once PHP has finished downloading, extract the contents into the C:\PHP folder we just created.

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/9c64a299-b63d-47b8-9414-bfa9424c5a15)

Download and install (5) MySQL. Select `Typical Install`. Once installed, make sure to launch the `MySQL Instance Configuration Wizard`. Proceed through the dialogue boxes and select `Standard Configuration`, and choose a `root password`. Finally Execute the Configuration. Make sure to keep track of your chosen password!

| ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/e83a67c9-8465-454a-b6b0-f0f9c196b03f) | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/913d6414-968f-4983-b275-18e58eafe399) |
|:---:|:---:|
| | |
| ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/bf6e4bcf-9e9a-4f19-b745-511f23534ed1) | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/9a809fe2-91c7-4a03-b277-899f252741d0) |

  <h2>Great, now onto the next step!</h2>
</p>
<br />

<p>
  <h3>Step 3: IIS Configuration </h3>

  Press the Start button and search for 'IIS'. Right click on Internet Information Services Manager and Run as administrator.

  ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/8823a214-30a9-4104-bd45-8afa8bf52413)

  From the Manager homepage, double click on PHP Manager, and then click on `Register new PHP version`.

  | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/304ffdb7-ed70-4434-8911-f0e8cd04a824) | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/f82f0c59-83ae-4c8a-88a9-344c3de36073) |
  |:---:|:---:|

  A Dialogue window will appear asking for a path to the php executable file. Click on the three dots to browse your files, and navigate to our C:\PHP folder. Choose the only `php-cgi` executable in that folder and continue.

  Then return to the Homepage by clicking on vm-osticket on the left side of the window, and then click Restart on the right side, to restart the server with the new configuration.

  | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/253445bf-e3f7-41bb-8a47-c7612b87e5e3) |
  |:---:|
  | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/4e61b45e-f4c4-4ae7-b459-064f176916fa)





</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
