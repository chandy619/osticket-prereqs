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
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/f82db133-902d-4742-ae41-8fff016e4acb">
</p>
<p>
1. Install/ Enable IIS: Open the Control Panel from your Windows VM by clicking the Start menu. Search for 'Control Panel' and select 'Programs'. Click on 'Turn Windows features on or off'. Check the box for 'Internet Information Services' folder then click the '+' sign to expand it. Locate the folder labeled 'World Wide Web Services' and expand it. Next, expand the 'Application Development Features' folder and check the box for 'CGI'. Lastly, expand the folder labeled 'Common HTTP Features' and select the remaining boxes that are uncheck. When complete, select 'OK' for IIS to begin installing. * To check if you properly installed IIS, open a web browswer page and enter '127.0.0.1' into the url box. The screen should reflect a Windows Internet Information Services webpage.*
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/b9d9cc04-42c4-40f4-8261-b0169c4f427e">
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/1b3d2b5f-a658-410c-b507-facdf17c7acc">
</p>
<p>
2. Download and Install PHP Manager and the URL Rewrite Module: For the next steps, download and install PHP Manager and Rewrite Module from the Installation Files link provided in the 'List of Prerequisites' section above. There are no extra steps needed; just use the default settings as you proceed with each installation. 
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/13a5eff4-0975-4227-9d86-2bc7ec53fb4f">
</p>
<p>
3. Create new PHP Folder in C Drive, Download, and Unzip: Create a directory (new folder) for PHP on your Windows VM's C drive. This folder will be used to store the files from the PHP installation zip file. Therefore, after creating the folder, download the file and extract its contents into the new C:\PHP folder. *In case you run into issues downloading the zip file, try downloading and installing the zip file from a Google Chrome web browser versus Microsoft Edge.* 
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/8464ecd2-1501-4040-945c-279ea2e6a753">
</p>
<p>
4. Download and Install VC Redistributable: This step is quite simple. Download and install VC Redist from the Installation Files list.
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/56fee55f-e35c-4a72-81b8-2a37ba53758e">
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/422c09ed-3902-452a-95fb-2ba9840664cb">
</p>
<p>
5. Download and Install MySQL Server: Next up, download and install the MySQL Server software from the Installation Files list. This software is important for creating a database to store files and information for osTicket. While moving throughout the installation setup, select the 'Typcal' option. After that, you'll need to create some credentials that will be used later on in this tutorial. Be sure to select the 'Standard Configuration' option. Take note of the username and password you've created in case you forget. Click 'Finish' to close out the prompt.
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/bdf0479f-b6ed-4a18-a857-22508ba78587">
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/be849bb5-70aa-48bb-8820-6096c01407a5">
</p>
<p>
6. Open IIS as Admin and Register PHP: Open IIS by clicking on the Start menu. Search 'IIS' and select the option to 'Run as Administrator'. Once it opens, double-click the icon labeled 'PHP Manager'. Select the option to 'Register new PHP version' and click on the browse box. To locate the correct file, follow the path example provided to you: C:\PHP\php-cgi.exe. Before leaving IIS, be sure to click the green 'Restart' button located on the left side of the window.
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/98be344d-0d01-4aae-8f7e-e4ce2d37e153">
</p>
<p>
7. Download and Install osTicket: The next step will be to download osTicket from the list of Installation Files. Once it's dowloaded, open the zip file where you will find a folder named 'upload'. Next, open a new 'File Explorer' window. Follow this path: c:\inetpub\wwwroot and copy and paste the 'upload' folder into it. When the contents finish extracting, rename the folder 'osTicket'.
</p>
<br />

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/979659f7-3ee9-45b0-8fe5-3ba83c0093ae">
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/4cd07a07-b635-4749-a060-9a26832d2441">
</p>
<p>
8. osTicket Configuration via IIS: Return to IIS. Begin by reloading the server by clicking the green 'Restart' button again. Now, in the top left corner, follow the path: Sites > Default Web Site > osTicket. On the right-hand side of the IIS window, click on 'Browse *.80 (http)'. An osTicket Installer webpage will open via Microsoft Edge or whereever web browser you prefer it to open in. 
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
10. Continue Setting up osTicket in Browser: Return to the osTicket Installer web browser and click 'Continue'. Fill out the necessary fields, i.e., Helpdesk Name, Default Email and Admin User Information. Remember to keep track of the username and password information for the next lab. For the remaining portion (Database Settings), you'll need to download and install the HiediSQL.
</p>
<br/>

<p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/6065f79e-38a2-4487-8ca4-64bb5fdce5ed">
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/3b71fc00-3529-4756-a061-cb7f58bec0cd">
</p>
<p>
11. Download and Install HeidiSQL: Go back to the list of Installation Files to download and install the HeidiSQL. Once its installed, click the 'New' button and login by using the username 'root' and the password you created when installing MySQL Server. To begin creating a new database, right-click over 'Unnamed' on the left-side of the window > select 'Create new' > select 'database'. Name the database 'osTicket'.
</p>
<br />

</p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/c7d00c3b-acde-475a-b7e4-e05c812cb294">
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/5c692ecd-69c3-4fff-b62c-68a6048827ee">
</p>
<p>
12. Complete osTicket Installation in Browser: Return to your osTicket Installer webpage to fill-in the remaining 'Database Settings' fields with the credentials you used for HeidiSQL, then click 'Install Now!'. Once the installation is complete, the webpage will confirm if osTicket was successfully installed or not. Before continuing to use osTicket, there are a couple housekeeping items to take care of. First, delete the 'setup' folder located in C:\inetpub\wwwroot\osTicket. Lastly, return to C:\inetpub\wwwroot\osTicket\include/ost-config.php and update the file's permissions to 'read only' access. Now you may login using the admin user credentials you created for osTicket as final proof that you've succeeded!
</p>
</p>
<img width="960" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/62cd7e72-f561-434b-9a29-cc176f581709">
</p>
