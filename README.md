<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system, osTicket.<br />

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
- HeidiSQL
- MySQL
- osTicket
- Please use this link of <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a> to try on your own.<br />

<h2>Installation Steps</h2>

<p>
<img width="648" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/40ba4631-55d2-485a-a8bb-cd64f6e43fd0"/>
</p>
<p>
1. Install/ Enable IIS- Open the Control Panel from your Windows VM by right-clicking the Start menu. Search for 'Control Panel' and select 'Programs'. Click on 'Turn Windows features on or off'. Check box for the 'Internet Information Services' folder and expand it. Locate the folder labeled 'World Wide Web Services' and expand it. Expand the 'Application Development Features' folder and check the box for 'CGI'. Next, expand the folder labeled 'Common HTTP Features' and make sure each box under it is checked. When complete, select 'OK' for IIS to begin installing.
</p>
<br />

<p>
<img width="342" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/2fdb7417-aeb0-4305-8c0f-a920644d89b0">
<img width="356" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/6de6a7ff-2fda-49cd-a1ba-96d23a9c51ec">
</p>
<p>
2. Download and Install PHP Manager and the URL Rewrite Model- For the next steps, download and install PHP Manager and Rewrite Module from the installation files link provided in the List of Prerequisites section above. There are no extra steps needed; just use the default settings as you proceed with each installation. 
</p>
<br />

<p>
<img width="392" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/379034d2-e4d0-4900-9c99-0484bea8dfae">
<img width="362" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/598017c5-0111-45fa-934e-4db8231a0c7a">
</p>
<p>
3. Create new PHP Directory in C Drive, Download and Unzip- Create a directory (new folder) for PHP on your Windows VM's C drive. This folder will be used to store the files from the 'PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip)' installation file. Therefore, after creating the folder, download the file and extract its contents into the new C:\PHP folder.
</p>
<br />

<p>
<img width="456" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/75326dad-f58f-437b-b9a6-95dd4ad95d6f">
</p>
<p>
4. Download and Install VC Redistributable- Download and install VC Redist from the installation files list.
</p>
<br />

<p>
<img width="368" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/6fb343f7-cfe7-46d4-9eed-73c4841bbb10">
<img width="380" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/19350341-6328-42be-849e-bd574ff1bc61">
</p>
<p>
5. Download and Install MySQL- From the Installations Files list, download and install the MySQL Server software. This software is important fore creating a database to store files and information for osTicket. While moving throught the installation setup, select the 'Typcal' option. After that, you'll need to create some credentials that will be needed later on. Be sure to select the 'Standard Configuration' option. Take note of the username and password you've used in case you forget. Click 'Finish' to close out the prompt.
</p>
<br />

<p>
<img width="557" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/8450d17a-2f37-4138-8cce-f3818f9caf14"> 
<img width="413" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/ac1d6902-abdf-4d1d-9870-13d62ab9b48c">
</p>
<p>
6. Open IIS as Admin and Register PHP- Open IIS by clicking on the Start menu. Search 'IIS', right-click to open as Administrator. Once it open, double-click the icon labeled 'PHP Manager'. Slect the option to 'Register new PHP version' and click on the box with 3 dots in it in order to browse the C-drive to select the file named 'php-cgi'. Before leaving IIS, be sure to click the 'Restart' button located in the top right corner of the window. 
</p>
<br />

<p>
<img width="538" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/2c1f0c04-799a-4fe3-aecc-d09d3d82a9f5">
</p>
<p>
7. Download and Install osTicket- The next step will be to download osTicket from the list of Installation Files. Once its dowloaded, open the zip file and you will see a folder named 'upload'. Next, open a new 'File Explorer' window. Follow this path: c:\inetpub\wwwroot and copy and paste the 'upload' folder into it. When the contents finish extracting, rename the folder 'osTicket'.
</p>
<br />

<p>
<img width="538" alt="image" src="https://github.com/chandy619/osticket-prereqs/assets/144288806/12cd8406-fde0-400b-a092-8f1864437fa6">
</p>
<p>
8. Complete osTicket Configuration via IIS- Return to IIS. Begin by reloadinging the server by clicking the 'Restart' button in the top right corner. Now,  in the top left corner, follow the path: Sites > Default Web Site > osTicket. Back  on the right side of the IIS window, click on 'Browse *80 (http)'
</p>
<br />
