<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This lab outlines the prerequisites and installation of the open-source help desk ticketing system, osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Internet Information Services (IIS)
- PHP Manager for IIS
- IIS URL Rewrite Module
- VC Redistributable
- MySQL Server
- osTicket
- HeidiSQL
- Please use this link of <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a> to try on your own.<br />

<h2>Installation Steps</h2>

<p>
<img width="648" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/40ba4631-55d2-485a-a8bb-cd64f6e43fd0"/>
</p>
<p>
1. Install/ Enable IIS: Open the Control Panel from your Windows VM by right-clicking the 'Start' menu. Search for 'Control Panel' and select 'Programs'. Click on 'Turn Windows features on or off'. Check box for the 'Internet Information Services' folder and expand it. Locate the folder labeled 'World Wide Web Services' and expand it. Expand the 'Application Development Features' folder and check the box for 'CGI'. Next, expand the folder labeled 'Common HTTP Features' and make sure each box under it is checked. When complete, select 'OK' for IIS to begin installing.
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/b9d9cc04-42c4-40f4-8261-b0169c4f427e">
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/1b3d2b5f-a658-410c-b507-facdf17c7acc">
</p>
<p>
2. Download and Install PHP Manager and the URL Rewrite Module: For the next steps, download and install PHP Manager and Rewrite Module from the Installation Files link provided in the List of Prerequisites section above. There are no extra steps needed; just use the default settings as you proceed with each installation. 
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/13a5eff4-0975-4227-9d86-2bc7ec53fb4f">
</p>
<p>
3. Create new PHP Folder in C Drive, Download, and Unzip: Create a directory (new folder) for PHP on your Windows VM's C drive. This folder will be used to store the files from the 'PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip)' installation file. Therefore, after creating the folder, download the file and extract its contents into the new C:\PHP folder.
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/8464ecd2-1501-4040-945c-279ea2e6a753">
</p>
<p>
4. Download and Install VC Redistributable: Download and install VC Redist from the Installation Files list.
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/56fee55f-e35c-4a72-81b8-2a37ba53758e">
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/422c09ed-3902-452a-95fb-2ba9840664cb">
</p>
<p>
5. Download and Install MySQL Server: From the Installations Files list, download and install the MySQL Server software. This software is important for creating a database to store files and information for osTicket. While moving throughout the installation setup, select the 'Typcal' option. After that, you'll need to create some credentials that will be needed later on in this tutorial. Be sure to select the 'Standard Configuration' option. Take note of the username and password you've used in case you forget. Click 'Finish' to close out the prompt.
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/bdf0479f-b6ed-4a18-a857-22508ba78587">
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/be849bb5-70aa-48bb-8820-6096c01407a5">
</p>
<p>
6. Open IIS as Admin and Register PHP: Open IIS by clicking on the 'Start' menu. Search 'IIS', right-click to open as Administrator. Once it opens, double-click the icon labeled 'PHP Manager'. Select the option to 'Register new PHP version' and click on the browse box in order to find the C-drive to select the file named 'php-cgi'. Before leaving IIS, be sure to click the 'Restart' button located in the top right corner of the window. 
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/98be344d-0d01-4aae-8f7e-e4ce2d37e153">
</p>
<p>
7. Download and Install osTicket: The next step will be to download osTicket from the list of Installation Files. Once it's dowloaded, open the zip file and you will see a folder named 'upload'. Next, open a new 'File Explorer' window. Follow this path: c:\inetpub\wwwroot and copy and paste the 'upload' folder into it. When the contents finish extracting, rename the folder 'osTicket'.
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/979659f7-3ee9-45b0-8fe5-3ba83c0093ae">
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/4cd07a07-b635-4749-a060-9a26832d2441">
</p>
<p>
8. osTicket Configuration via IIS: Return to IIS. Begin by reloadinging the server by clicking the 'Restart' button in the top right corner. Now, in the top left corner, follow the path: Sites > Default Web Site > osTicket. On the right-hand side of the IIS window, click on 'Browse *.80 (http)'. An osTicket Installer webpage will open via Microsoft Edge. 
</p>
<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/f86fbc1d-896c-469e-9fab-8a2ea91127a9">
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/8eaa1173-a5cb-41d9-bea9-cd40c548d8b3">
</p>
<p>
Notice that some extensions are not enabled, so return to IIS. Click on the 'osTicket' folder located on the left-hand side and double-click on PHP Manager. Click on 'Enable or disable an extension'. You'll find a list of PHP Extensions. Click on each of the following:'php_imap.dll', 'php_intl.dll', and 'php_opache.dll'. and click 'Enable' in the top right corner. Lastly, return to the browser page of the osTicket Installer and refresh the page.
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/59d1e0a8-36df-4ff9-a558-929c7fad1987">
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/bc4c5d2a-cbed-4e6c-8f30-0f5ab6231435">
</p>
<p>
9. Rename and Assign Permissions: Return to the 'File Explorer' window that holds the 'osTicket' folder. Follow the path C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php. Rename the file 'ost-config.php'. Right-click on the file to update permissions. Follow the string of actions: Properties > Security > Advanced > Disable inheritance > Remove all permissions > Add > Select a principle > Type 'Everyone' > Check Names > OK > Full Control > OK > Apply > OK.
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/f5ae4d30-33a8-4ffd-b3ad-c2649ce78526">
</p>
<p>
10. Continue Setting up osTicket in Browser: Return to the osTicket Installer web browser and click 'Continue'. Fill out the necessary fields, i.e., Helpdesk Name, Default Email and Admin User information. Remember to keep track of the username and password information for the next tutorial. For the remaining portion (Database Settings), you'll need to download and install the HiediSQL.For the remaining portion (Database Settings), you'll need to download and install the HiediSQL.
</p>
<br/>

<p>
<img width="340" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/97fbcdde-773a-4da2-8f23-357c810467e5">
<img width="460" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/fb4aced7-bdfc-4984-9639-3fae51d6f414">
</p>
<p>
11. Download and Install HeidiSQL: Go back to the list of Installation Files to download and install the HeidiSQL. Once its installed, login by using the username and password you entered when installing MySQL Server. To begin creating a new database, right-click over 'Unnamed' on the left-side of the window. Name the database 'osTicket'.
</p>
<br />

</p>
<img width="396" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/7b33b7f8-15c9-4933-a23a-e84d9d6bf441">
<img width="407" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/d02e7333-d3f4-4014-95c5-cdbd6b54efee">
</p>
<p>
12. Complete osTIcket Installation in Browser: Return to your osTicket Installer webpage to fill-in the remaining  'Database Setting' fields. Click 'Install Now!' Once the installation is complete, the webpage will confirm if osTicket was successfully installed or not. Before continuing to use osTicket, there are a couple housekeeping items to take care of. First, delete the 'setup' folder locate in C:\inetpub\wwwroot\osTicket. Lastly, return to C:\inetpub\wwwroot\osTicket\include/ost-config.php and update the file's permissions to 'read only' access.
</p>
