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
<img src="https://i.imgur.com/SqcwgVC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Install mysql-5.5.62-win32 from the osTicket-installation-files. You can select typical setup. Select to launch after install. When it launches select standard configuration. Under modify security settings for the password choose root. Select next then execute. 
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
<img src="https://i.imgur.com/SqcwgVC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Install mysql-5.5.62-win32 from the osTicket-installation-files. You can select typical setup. Select to launch after install. When it launches select standard configuration. Under modify security settings for the password choose root. Select next then execute. 
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
<img src="https://i.imgur.com/SqcwgVC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
Install mysql-5.5.62-win32 from the osTicket-installation-files. You can select typical setup. Select to launch after install. When it launches select standard configuration. Under modify security settings for the password choose root. Select next then execute. 
</p>
<br />
