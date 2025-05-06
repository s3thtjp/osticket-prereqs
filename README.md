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

- Sign up for a free Azure account
- Set up your virtual machine with Windows 10
- Connect to your virtual machine using Remote Desktop Connection
- Download files to set up osTicket on virtual machine
- Install osTicket

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/UBfQLNI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Create your virtual machine through the Azure portal by selecting virtual machines link and selecting create azure virtual machine (make sure image is set to Windows 10). Wait for the virtual machine to finish setting up. Once complete, click on the virtual machine with Windows 10 link and copy down your public ip address as you will be needing it for the next step with logging into the virtual machine using remote desktop connection. 
</p>
<br />

<p>
<img src="https://i.imgur.com/copLjni.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Connect to the virtual machine using Windows 10 through remote desktop connection. After logged onto the virtual machine open up the microsoft edge to download the necessary <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">files</a> to set up osTicket. Open up the folder containing the osTicket tools and right click on it, then click extract all and point it to the desktop. After all the files have extracted to the folder you no longer need the zip file and can safely move it to the trash bin. Next we are going to enable ISS on the virtual machine by opening up the control panel then selecting programs and turn on off windows features. 
</p>
<br />

<p>
<img src="https://i.imgur.com/dDWQPxP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the window check the box for Internet Information Services then click the plus sign to drop down more folders. Click the plus sign of World Wide Web Services then the plus sign to Application Development Features and check the box for CGI. *This must be enabled to install the ISS file from the osTicket tools*
</p>
<br />

<p>
<img src="https://i.imgur.com/suYIZu8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Now go back to the osTicket-installation-files and install the PHPManagerForIIS_V1.5.0.
</p>
<br />

<p>
<img src="https://i.imgur.com/DA74aEh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Then install the rewrite_amd64_en-US file found in osTicket-installation-files.
</p>
<br />

<p>
<img src="https://i.imgur.com/LAq8hVC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Now create a new folder in the C: directory called PHP. From the osTicket-installation-files extract php-7.3.8-nts-Win32-VC15-x86 to the new folder that you created by selecting browse and finding the directory to PHP on the C:.
</p>
<br />

<p>
<img src="https://i.imgur.com/pNMApim.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Now open the VC_redist.x86 and install the redistributable.
</p>
<br />

<p>
<img src="https://i.imgur.com/SqcwgVC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Install mysql-5.5.62-win32 from the osTicket-installation-files. You can select typical setup. Select to launch after install. When it launches select standard configuration. Under modify security settings for the password choose root. Select next then execute. 
</p>
<br />

<p>
<img src="https://i.imgur.com/yZSj1mp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Click in the search box by the start button and look for iss and right click on the Internet Information Services Manager and run as administrator. 
</p>
<br />

<p>
<img src="https://i.imgur.com/QrQ0U2j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Click on the PHP Manager then click on register new PHP version and point the manager to the php-cgi.exe that was extracted in the PHP directory on the C: drive.
</p>
<br />

<p>
<img src="https://i.imgur.com/0VsVSvW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Next we are going to stop and start the IIS by right clicking on the virtual machine name on the top left and dragging down to stop. After a few seconds we are going to right click on the same virtual machine name and start.
</p>
<br />

<p>
<img src="https://i.imgur.com/p4NFS76.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
</p>
<br />

<p>
<img src="https://i.imgur.com/0VsVSvW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Next we are going to stop and start the IIS like we did a couple steps ago.
</p>
<br />

<p>
<img src="https://i.imgur.com/rM6NAOx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Now we are going to go to the "osTicket" directory within ISS by expanding the drop down of "Sites" then again with "Default Web Site" and clicking on the "osTicket" folder. On the right side column under "Manage Folder" we are going to then click on "Browse *.80 http" 
</p>
<br />

<p>
<img src="https://i.imgur.com/fsr8B3T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Next we are going to enable the following extensions in the PHP Manager: php_imap.dll, php_intl.dll and php_opcache.dl. In the ISS double click on PHP Manager. At the bottom select "Enable or disable an extension" and look for the files and right click then select enable to enable the extensions. Refresh your browser and it should have the new extensions enabled.

</p>
<br />

<p>
<img src="https://i.imgur.com/8q1qDbO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Next we are going to Rename: ost-config.php. From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>
<br />

<p>
<img src="https://i.imgur.com/ERGz8AD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Now we are going to set up permissions for this file to everyone. Right click on ost-config.php and click on properties. In the new window select the "Security" tab on the top then click on the "Advanced" button. Click on the "Disable Inheritance" button and remove all current permissions. Next click on the "Add" button and "Select a principal" at the top in the field under "Enter the object name to select" type everyone then click on check names and select the "Everyone" object then click "OK" Add Everyone to have full access permissions to this file.
</p>
<br />

<p>
<img src="https://i.imgur.com/5JE3Jj9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Next we are going to click on "Continue" in the web browser with osTicket Installer and fill in the appropriate fields stopping at the database settings section. The emails do not have to be your actual emails. Then we are going to install HeidiSQL_12.3.0.6589_Setup from the osTicket-Installation-Files folder. Make sure the box is checked to launch after installation. When it opens click on skip.
</p>
<br />

<p>
<img src="https://i.imgur.com/e0NkUBm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Next we are going to click on "New" in the bottom left and input the password root into the field on the right. When completed it should connect to the backend database that we installed previously.
</p>
<br />

<p>
<img src="https://i.imgur.com/3TwlQ5u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Next we are going to create a new database by right clicking on "Unamed" dragging down to "Create New" and clicking on database. We are going to name it "osTicket" then click "OK". A new database should now be entered into the left field of HeidiSQL. 
</p>
<br />

<p>
<img src="https://i.imgur.com/sokIA8F.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Next we are going to fill in the remaining fields of the osTicket Installation within the browser. Under MySQL Database we are going to enter "osTicket". Under MySQL Username we are going to put "root" and under MySQL Password we going to enter "root".
</p>
<br />

<p>
<img src="https://i.imgur.com/Y8VVdZD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Next we are going to click on "Install" and it will finish installing osTicket.
</p>
<br />
