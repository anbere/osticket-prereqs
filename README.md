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
  
  - Download the (4) PHP folder. Create an empty folder in the C Drive named 'PHP'. Once PHP has finished downloading, extract the contents into the C:\PHP folder we just created.
  
  ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/9c64a299-b63d-47b8-9414-bfa9424c5a15)
  
  - Download and install (5) MySQL. Select `Typical Install`. Once installed, make sure to launch the `MySQL Instance Configuration Wizard`. Proceed through the dialogue boxes and select 
  `Standard Configuration`, and choose a `root password`. Finally Execute the Configuration. Make sure to keep track of your chosen password!
  
  | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/e83a67c9-8465-454a-b6b0-f0f9c196b03f) | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/913d6414-968f-4983-b275-18e58eafe399) |
  |:---:|:---:|
  | | |
  | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/bf6e4bcf-9e9a-4f19-b745-511f23534ed1) | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/9a809fe2-91c7-4a03-b277-899f252741d0) |

  <h2>Great, now onto the next step!</h2>
</p>
<br />

<p>
  <h3>Step 3: IIS Configuration </h3>

  - Press the Start button and search for 'IIS'. Right click on Internet Information Services Manager and Run as administrator.

  ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/8823a214-30a9-4104-bd45-8afa8bf52413)

  - From the Manager homepage, double click on PHP Manager, and then click on `Register new PHP version`.

  | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/304ffdb7-ed70-4434-8911-f0e8cd04a824) | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/f82f0c59-83ae-4c8a-88a9-344c3de36073) |
  |:---:|:---:|

  - A Dialogue window will appear asking for a path to the php executable file. Click on the three dots to browse your files, and navigate to our C:\PHP folder. Choose the only `php-cgi` executable in that folder and continue.

  - Then return to the Homepage by clicking on vm-osticket on the left side of the window, and then click Restart on the right side, to restart the server with the new configuration.

  | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/253445bf-e3f7-41bb-8a47-c7612b87e5e3) |
  |:---:|
  | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/4e61b45e-f4c4-4ae7-b459-064f176916fa)


  <h2>IIS is now configured!</h2>
</p>
<br />

<p>

  <h3>Step 4: Install and Set Up osTicket</h3>

  - We will download the (7) osTicket zipped folder from the Google drive installation files, and then Extract the contents of the folder. Within the unzipped folder, copy the `upload` folder into `C:\inetpub\wwwroot`.

  - Within C:\inetpub\wwwroot, rename `upload` to `osTicket`.


  ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/241a8fb8-45e4-430b-9b2d-e54269411d20)

  ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/c77a6f58-e040-4c95-964d-18c0c0246426)

  - Same as before, open up the IIS Manager and Restart the server. (Click restart on the upper right side of the window.

  - Now, on the left side, starting by clicking the arrow next to our hostname (`vm-osticket`), expand the dropdown from Sites -> Default Web Site -> then click on osTicket. Then click on `Browse *:80 (http)` which will now appear on the right side of the IIS Manager window.

  <img src='https://github.com/anbere/osticket-prereqs/assets/90169033/3383a305-7f3f-41b3-85e3-2afc3734c154' width=400> | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/14b143b2-6dd0-48b6-8915-533520990d54)
  |:---:|:---:|

  - A webpage at `http://localhost/osTicket/setup/` will open and begin loading. Notice some features are not enabled.

  ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/60b02444-80d6-4640-a05a-2f6f4bc607b0)


  - Return to the IIS Manager, Sites -> Default -> osTicket and double click on `PHP Manager`. On the next page, click on `Enable or Disable an extenstion`. We want to enable the following extensions by right clicking them and clicking `Enable`.

    - php_imap.dll
    - php_intl.dll
    - php_opcache.dll

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/728efcd8-6f5b-4676-9d66-589e8860ddb9) | | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/cb2862e4-31a6-4818-a721-b9c993cf22b7) 
|:---:|:---:|:---:|

- Once enabled, refresh the osTicket site in the browser and observe the changes.

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/548d07cc-af1f-4c0b-9d94-5d05e1d3e1db)

Next we are going to rename a configuration file. Browse file explorer to this location `C:\inetpub\wwwroot\osTicket\include\`. Rename the file `ost-sampleconfig.php` to `ost-config.php`.

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/487f154f-17c8-4eea-aa75-8a323a8d03b6) | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/17eb57c6-17d5-4e5a-8d59-0f8102af7896)
|:---:|:---:|

- Right click that file we just renamed and click on `Properties`.Navigate to the Security tab and then click on `Advanced` and choose `Disable inheritance`, and click `Remove all inherited permissions from this object`.

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/c86c4b3c-029d-48eb-8fdf-70112b65a0b3) | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/60a5d5bb-d76d-4806-a552-7020c94371a4)
|:---:|:---:|


- Then we will click on `Add` to add permissions. Click on `Select a principal`. In the dialogue box type 'Everyone', select `Check Names` then click `OK`. On the following window, give full access and click `OK` and Apply the changes.

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/25088c63-a781-45bd-bba5-2c2accf6a334) 

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/e3340cd0-905a-4c0f-b3f3-a1242a092537)

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/a85363f5-82cc-4640-86b0-6e287262ff90)

- Return to the osTicket Installer in the browser and click `Continue`. Fill the text fields, naming the help desk and adding a default email. For the scope of this project, the email does not have to be real.

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/47dc1baf-54f9-49e2-9ba5-c67458c89cc6)

- Enter information for the admin user, remember the username and password you use here.

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/1f6b8e15-9fe7-4eca-9d92-d550ea545615)

- Before we continue with this, we will set up our local SQL database. We will now install (6) HeidiSQL from our Google drive links. Download the installer and begin the installation and proceed with all the default settings, making sure to launch HeidiSQL after the installation completes.

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/0852a437-6b6c-4619-91f9-0c5290bc7db1)

- Once launched, we will create a new connection by clicking on `New` in the bottem left corner, then using the credentials we decided when installing SQL, we will type the username and password we chose, and then click on `Open`.

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/c5bf0508-609d-4047-a670-d0c378b9ea1f)

- Now, right click on `Unnamed` on the left side, travel to Create new -> Database, and title the database 'osTicket' and click `OK`.

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/145c82df-e973-4961-9ea8-dc97081d7c02) | ![image](https://github.com/anbere/osticket-prereqs/assets/90169033/b2a77b73-9f69-49be-aa08-e46b1c66020a)
|:---:|:---:|

- We return to the browser now to finish the osTicket installation. enter the database information, 'osTicket' in the MySQL Database text field, and the MySQL username and password we used to connect to our databse in HeidiSQL.

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/7ea9bd66-9fee-4cc3-a3e8-45f6b7b5ff18)

- Click on `Install Now`, and after some time you will see a successful installation page!

![image](https://github.com/anbere/osticket-prereqs/assets/90169033/44d216e2-366b-4993-8923-ea1b97a5c4ad)

<h2>Congratulations, osTicket has now been installed and can be used!</h2>

- Follow along my next Tutorial to see how to use osTicket.

</p>
