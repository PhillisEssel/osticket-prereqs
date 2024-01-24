<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- php-7.3.8, heidiSQL, odTicketv1.15.8
- mySQL, Rewrite_amd64_en-US.msi, 
- VC_redist.x86.exe,
- PHP Manager
- IIS

<h2>Installation Steps</h2>

<p>


![Step 1](https://github.com/PhillisEssel/osticket-prereqs/assets/156061642/8893e501-f59f-46b4-a546-8661cdbbebd8)
<p><a href="https://imgur.com/a/MeTaVF4">More</a></p>

</p>
<p>
Create a Virtual Machine on Azure with a resource group, windows 10/11 & Virtual Network. Name the virtual machine vm-osticket along with creating a username and password to connect via Remote Desktop. Install/enable IIS in Windows. iis>World Wide Web Services>Application Development Features> enable CGI & common HTTP Features. IIS>Wed Management Tools>IIS Management Console. Next Install PHP Manager for IIS, Rewrite Module, in files create a folder under windows c name "PHP." Then install PHP7.3.8 and unzip the contents to the C:\PHP Folder.


</p>
<br />

<p>


![Step 21](https://github.com/PhillisEssel/osticket-prereqs/assets/156061642/1038e7e3-d9d3-43e3-97ec-d9de81c74d7e)
<p><a href="https://imgur.com/a/V0N6z7A">More</a></p>
</p>
<p>
 Next download and install VC redist.x86.exe. Download and Install My SQL 5.5.62, Press Typical setup, launch, standard configuration, and create a password under the username root. Open IIS as an administrator. Register PHP from within IIS, then reload IIS (stop/start). Download and Install osTicket v1.15.8. extract and put the "upload" folder to windows c>inetpub>wwwroot then change it "osticket." Reload IIS (stop/start) then go to Sites>Default>osTicket then to the right click "Browse *:80" You should see "Congratulations." osTicket should have been installed.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back to IIS>SITES>DEFAULT>OStICKET and double click PHP Manager and "click enable or disable an entension" and enable: php_imap.dll/php_intl.dll/php_opcache.dll. then go back to osTicket browser and refresh. Next go to files>c>inetpub>wwwwroot>osTicket>include>ost-sampleconfig.php and change the name to ost-config.php. Next assign permissions for ost-config.php (disable inheritance>remove all, New Permissions.everyone>all. Next go to osTicket, type default email then go back to installation files and install HeidiSQL. Create a new session root/your password. connect and create a database called "osTicket" then continue setting up osTicket in browser (mySQL Database:osTicket/mySQL Username:root/mySQL Password:your password) click "install."
</p>
<br />
