
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png"/>
</p>

<h1> How to Install osTicket </h1>
This is an easy guide to installing a help desk ticketing system called osTicket.<br/>

<h2> Files You Need to Download</h2>

- ### [Download Now](https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) 📁

<h2> Software & Technologies  Used</h2>

- Windows 10 (Build 19044)
- Microsoft Azure (Virtual Machines)
- Windows App for Mac (previously named Microsoft Remote Desktop)
- Internet Information Services (IIS)

  <h2> Prerequisites </h2>

- Create a Virtual Machine in Azure
- Install osTicket v1.15.8
- Install HeidiSQL
- Install MySQL
- Install PHP
- install Microsoft Visual C++ Redistributable
  <h2>Steps</h2>
<h3 align="center">Create Virtual Machine in Azure</h3>
<br />
<p>
<h3 align="center">First, start by creating a Resource Group inside Azure.</h3>
<br />
</p>
<p>
	<img src="https://i.imgur.com/K9ZwCvB.png" height="75%" width="100%" />
</p>
<p>
<h3 align="center">Now, create a Windows 10 Virtual Machine (VM), typically with 2-4 Virtual CPUs. For username and password, it can be anything as we'll be using this info to remote in with our main computer. When creating the Virtual Machine (VM), allow Azure to create a new Virtual Network (Vnet):</h3>
<br />
</p>
<p>
	<img src="https://i.imgur.com/3t6wNqG.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Open your Windows app on your computer and connect to your Virtual Machine that was created in Azure. </h3>
<br />
<p>
	<img src="https://i.imgur.com/LJdZNhw.png"/>
	

</p>
<br />
<br />
<h3 align="center">Now we need to install / Enable IIS in Windows. Go to your Search Bar > Type "Control Panel" > Click "Programs" > "Turn Windows features on or off" > Scroll down to "Internet Information Services (IIS).</h3>
<br />
<p>
	<img src="https://i.imgur.com/769QK2K.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Once clicked, find the "Internet Information Services" expand it and then expand the "World Wide Web" tab. Afterward, expand the application Developer tab. Finally check the "CGI" button & press Ok. You will need CGI to download the PHP Manager. The PHP manager is a back-end web programming language that allows osTicket to run off a web browser.</h3>
<br />
<p>
  <img src="https://i.imgur.com/KcAD10o.png" height="75%" width="100%"/>
</p>
<br />
<h3 align="center">Install PHP Manager</h3>
<br />
<p>
<h3 align="center">Download the PHP manager file, and agree with all the terms. We've now downloaded the PHP manager into our operating system.</h3>
<p>
  <img src="https://i.imgur.com/jw6J0Lv.png"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">Install Rewrite Module</h3>
<br />
<p>
<h3 align="center">Download the Rewrite Module file, agree with all the terms and it should now be installed onto the Computer.</h3>
<p>
  <img src="https://i.imgur.com/OzHLaMY.png"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">CREATE DIRECTORY C:\PHP</h3>
<br />
<p>
<h3 align="center"> Open File Explorer, type, "C:\" in the search bar, Right-click and create a new folder called, "PHP". Download php-7.3.8-nts-Win32-VC15-x86.zip from<a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> Files You Need to Download</a>, Extract it by going to where you download the file, Right-click the PHP 7.3.8 file and press extract to the PHP Folder you just created.
</h3>
<p>
  <img src="https://i.imgur.com/WZr7iek.png"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">VC_REDIST DOWNLOAD</h3>
<br/>
<h3 align="center"> Download and install VC_Redist, Agree with any terms and agreements and finish installing.
</h3>
<p>
  <img src="https://i.imgur.com/lfEhZ1z.png"75%" width="100%"/>
</p>
<br/>
<h3 align="center">DOWNLOAD MySQL </h3>
<h3 align="center"> Download and install MySQL, Agree with any terms and agreements up until you get to the password portion. Here you can create a username and password for the database that you'll be using to store the Ticket Information used in osTicket. 
</h3>
<p>
  <img src="https://i.imgur.com/Cw6cVFv.png"75%" width="100%"/>
<br/>
  <img src="https://i.imgur.com/PaSnB27.png" height="75%" width="100%" />
</p>
<br/>
<h3 align="center">Install osTicket v1.15.8</h3>
<br />
<p>
  Download osTicket (download from within lab files: link).
</p>
<p>
	From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot:”
</p>
	<img src="https://i.imgur.com/HIyGDbL.png" height="75%" width="100%" />
<p>
	Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”:
</p>
<p>
	<img src="https://i.imgur.com/96SFzQL.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Reload IIS (Open IIS, Stop and Start the server)</h3>
<br />
<p>
	Go to sites -> Default -> osTicket:
</p>
<p>
	<img src="https://i.imgur.com/WwsdVLI.png" height="75%" width="100%" />
</p>
<p>
	On the right, click “Browse *:80”:
</p>
<p>
	<img src="https://i.imgur.com/uQ4DX5K.png" height="75%" width="100%"/>
</p>
<br />
<br />
<h3 align="center">Enable Extensions in IIS: Note that some extensions are not enabled</h3>
<br />
<p>
	Go back to IIS, sites -> Default -> osTicket.
</p>
<p>
	Double-click PHP Manager:
</p>
<p>
	<img src="https://i.imgur.com/FdNMtu4.png" height="75%" width="100%" />
</p>
<p>
	Click “Enable or disable an extension”.
</p>
<p>
	Enable: php_imap.dll.
</p>
<p>
	Enable: php_intl.dll.
</p>
<p>
	Enable: php_opcache.dll:
</p>
<p>
	<img src="https://i.imgur.com/zVCf6CV.png" height="75%" width="100%"/>
</p>
<br />
<br />
<h3 align="center">Refresh the osTicket site in your browser, observe the changes</h3>
<br />
<p>
	<img src="https://i.imgur.com/e9rkaoK.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Rename</h3>
<br />
<p>
	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php.
</p>
<p>
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://i.imgur.com/3gLoeo3.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Assign Permissions: ost-config.php</h3>
<br />
<p>
	Disable inheritance -> Remove All:
</p>
<p>
	<img src="https://i.imgur.com/RddWiqF.png" height="75%" width="100%" />
</p>
<p>
	New Permissions -> Everyone -> All:
</p>
<p>
	<img src="https://i.imgur.com/FBTgEuz.png" height="75%" width="100%" />
</p>
<p>
	<img src="https://i.imgur.com/jdl7Xqr.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser (click Continue)</h3>
<br />
<p>
	Name Helpdesk.
</p>
<p>
	Default email (receives email from customers):
</p>
<p>
	<img src="https://i.imgur.com/gzvXSdV.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Download and Install HeidiSQL</h3>
<br />
<p>
	<img src="https://i.imgur.com/F2S0CX7.png" height="75%" width="100%" />
</p>
<p>
	Create a new session, root/root
</p>
<p>
	Connect to the session:
</p>
<p>
	<img src="https://i.imgur.com/fjtNvW4.png" height="75%" width="100%" "/>
</p>
<p>
	Create a database called “osTicket”:
</p>
<p>
	<img src="https://i.imgur.com/J6sXZQh.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser</h3>
<br />
<p>MySQL Database: osTicket</p>
<p>
	MySQL Username: root
</p>
<p>
	MySQL Password: root:
</p>
<p>
	<img src="https://i.imgur.com/6uKct7u.png" height="75%" width="100%" />
</p>
<p>Click “Install Now!”</p>
<p>Congratulations, hopefully it is installed with no errors!</hp>
<p>
	<img src="https://i.imgur.com/rhP6TaV.png" height="75%" width="100%" />
</p>
<br />
<br />

<h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</h3>
<p>
	<img src="https://i.imgur.com/0q0V3o4.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center"> Congrats, You've Finished Installing osTicket.</h3>
