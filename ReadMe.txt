ReadMe.txt for the App Rest Web Panel Evolution by Fix
    1. License Declaration Associated with a Software Program
    2. Introduction
    3. Features
    4. Installation Requirements and Setup of the Operating Environment
    5. Configuration Files (serv_inc.php and config.php) to Edit
    6. Configuration of the Rest Server Plugin on the RadioDJ Control Room
    7. Download and Installation of XAMPP
    8. Choosing the Old Database Manager or the New MySQL of XAMPP
    9. Copying the ArtWork (mp3 file covers) from the Control Room Folder to the Web App Folder
    10. How to Run Applications in Administrator Mode
    11. Testing the App Rest Web Panel and Troubleshooting
    12. How to Get the Best Performance with the App
    13. Mode and Order of Starting the RadioDJ, Xampp, and App Rest Web Panel Evolution Applications
    14. Connections Between Mixer and Sound Card for Live Broadcast with Rest Web Panel and Remote Speaker
    15. Procedure and Setup for Broadcasting with the Remote Speaker
    16. Restricting Access to phpMyAdmin in Your XAMPP Environment to Localhost Only
    17. Using a Strong Password for the MySQL Root Account in XAMPP
    18. Restricting Access to the App Rest Web Panel Evolution

    1. License Declaration Associated with a Software Program
Version 3, June 29, 2007
Copyright © 2007 Free Software Foundation, Inc. https://fsf.org/ All rights reserved.
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.
This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
You should have received a copy of the GNU General Public License along with this program. If not, see https://www.gnu.org/licenses/.

    2. Introduction The developer provides the software for free and asks users, if they appreciated the purpose of the remote control panel, to make a voluntary donation to support the continuous development of the App, and in this case, the donation is not required to use the software. No liability is accepted for damages caused by the use of the software or by an incorrect configuration of the operating environment, including editorial errors contained in the readme.txt file. The App Rest Web Panel Evolution is neither owned by RadioDJ nor by any company associated with RadioDJ. For any doubts about installation and/or configuration, please contact the developer first, or connect to the RadioDJ forum where a topic has been opened at: https://www.radiodj.ro/community/index.php/topic,17558.0.html. The same topic can be accessed directly from the App by following the “ASSISTANCE” link.
The Rest Web Panel Evolution interface is an excellent tool for web radios and on-air radios, making many control room features available within the remote control panel via internet connection and HTTP protocol. The interface was created by Fix, an IT enthusiast who studied and analyzed various web languages (HTML, CSS, PHP, SQL, JSON) and analyzed various GPL-licensed interfaces. The Rest Web Panel Evolution interface allows for remote broadcasting with one or more speakers located in a remote location compared to the RadioDJ control room. The remote speaker has a Web control panel accessible via a web browser at: http://REMOTE-IP/example-radiodj-example/. For the features of the App Rest Web Panel Evolution, see Features in Chapter 3.

3 – Features The Rest Web Panel Evolution interface offers the following features:
    1. Display on the top left of intro, outro, remaining, elapsed, duration counters, cover photo, artist, title, and year. Additionally, the now playing and next track as artist and title are displayed in the center left. The next track is displayed when the remaining time is less than 40 seconds.
    2. Display on the bottom left is an area for the playlist where tracks are placed. These provide information about the artist and title, duration counter, intro, outro, end_of_the_track, year, SongID, and a thumbnail of the mp3 file cover.
    3. Search for audio tracks within the database, i.e., Music, stationID, Jingle, Commercials, then you can choose the music genre and also keep an eye on the Count played parameter. When this parameter is zero (count played = 0), it indicates a track never played. The search form is very intuitive and easy to use while allowing you to articulate the query to the database. Additionally, the form has memory for the last keyword entered and a progressive searching system, meaning a query is made for each character entered. However, the search button remains operational for compatibility with browsers that have JavaScript disabled.
    4. Build an on-the-fly playlist for live broadcasting with a remote speaker. After finding the tracks through the right section “search,” you can build the playlist by stacking the tracks in top or bottom mode. To stack a track on top, there must be at least 2 tracks in the playlist area; otherwise, the track will always be inserted in bottom mode.
    5. Progressive numerical indication of the order of tracks plus the indication of the last element in the playlist. This allows you to know how many tracks are in our automatic playlist (tracks rotation) or on-the-fly.
    6. Display of the history of played tracks in descending mode.
    7. Display of the ranking (internal hit) of the most played tracks.
    8. Deletion of the entire playlist via the CANC. PLAYLIST button.
    9. Deletion of individual audio tracks via the red square with the X.
    10. Deletion of the history of played tracks.
    11. Catalog of tracks sorted by artist or group present in the Database.
    12. Change the AUTODJ/MANUAL status. The AUTODJ status (green button) allows generating automatic playlists through tracks rotation, suitable for broadcasts without a remote speaker or for music rotations, while the MANUAL status (red button) requires manual loading of tracks and playlists, suitable for broadcasts with a remote speaker. During live broadcasting with a remote speaker, it is necessary to switch to MANUAL (red button) to have the playlist area free only for on-the-fly playlists. This setting prevents on-the-fly playlists from mixing with automatic playlists produced with tracks rotation. Switching from AUTODJ to MANUAL may leave the playlist area not yet free, containing some tracks produced by tracks rotation. If you want to clear the playlist area, select the CANC. PLAYLIST button.
    13. Change the AUTOMATED/ASSISTED status. In AUTOMATED mode, the playlist tracks are played automatically, while in ASSISTED mode, operator intervention is required to start the track. During live broadcasting, the remote speaker can choose to select the AUTOMATED mode (green button), allowing the control room to intervene in inserting live tracks, or the ASSISTED mode (red button) to allow the speaker to insert tracks respecting the fade-out of musical tracks and the speaker’s vocal intervention times.
    14. Play any track from the automatic or on-the-fly playlist without following the preset order. Click on the area showing the progressive numbering of the track, and the operation will be performed.
    15. Pause a track.
    16. Restart a track.
    17. Start a track after the intro.
    18. Stop a track.
    19. Play a track.
    20. Songs details is a detailed summary of the information on the track being played.
    21. Instant player from 1 to 24. Allows playing tracks instantly, overlapping the audio being played. To use this mode, you need to pre-set the 24 tracks that will go live in the control room.
    22. MICROPHONE-OFF/ON-AIR button to enable the audio input of the RadioDJ control room. A VOIP service (Facebook chat, Skype, or others) and connections between the physical mixer and the sound card are required.

4 - Installation Requirements and Setup of the Operating Environment
    1. Have already installed the RadioDJ 1.8.2.0 or higher (2.0.X.X) application on the PC that will serve as the control room.
    2. Install Xampp version 7.1.26 for Windows 10/11 on the control room PC. The App you are going to install has not been verified on a PHP version higher than 7.1.26, so stick to the recommended Xampp version. Do not seek the latest technology by installing Xampp 8.2.12, as the app is not validated for this version and may not work correctly. Xampp is an integrated environment that allows us to use the functionalities of the MariaDB (MySQL) database manager, PHP, an APACHE Web server, etc. The Xampp packages you need to install are: PHP and Apache, while the MariaDB (MySQL) package, which is the MySQL database manager, will not be necessary if you continue to use your current database manager, i.e., the one used by the RadioDJ control room. It seems obvious, but in this case, the MySQL database manager should not be installed. If you have installed Xampp with the MariaDB database manager and no longer want to use your current database manager, you will not be able to maintain the current database connection, so you will need to remove/uninstall the old database manager and deconfigure the DatabaseSetup.exe utility, then follow the procedure in Chapter 8.
    3. The app has been created in two versions; one for RadioDJ 1.8.2.0 and one for higher versions. Why this distinction? Some construction differences in the database did not allow for a single App. The difference lies in the different column name containing the mp3 file covers. The database has the “songs” table with the “Album_Art” field name in the RadioDJ 1.8.2.0 version, while the table has the “image” field name in the higher versions of RadioDJ 2.0.x.x. After choosing the version, you need to extract the zip package of the Web App under the previously created folder named “WebApp” in the path: C:\xampp\htdocs\WebApp.
    4. For the operation of the control room and the third-party VOIP system, a second sound card will be necessary. The first will be used for the live broadcast of the RadioDJ application, which you already have, while the second will be used to make connections with the physical mixer for broadcasting with a remote speaker.
    5. A Fiber or ADSL2+ Internet connection to ensure the proper functioning of the third-party VoIP services you will use. Using a mobile Hot Spot is not recommended, as there is a lot of latency, and it is not possible to configure PORT-FORWARDING, so the App would not be reachable from the outside, which is crucial.
    6. Port Forwarding Configuration: Port forwarding is not optional, as it is useful for making the Web App accessible from outside. Port forwarding is a procedure that allows redirecting traffic from a specific port on the router to a device or program within the local network. In other words, if you want to access a web page or service within the LAN from an external location, you need to configure port forwarding to allow this access. Here’s how to set up port forwarding on your router: a) Access the router control panel: Open the browser and type the router’s IP address (usually 192.168.1.1 or 192.168.0.1) in the address bar. Enter the credentials to access the router settings. b) Find the Port Forwarding section: Navigate to the advanced settings or port forwarding options. This section may have different names depending on the router model. c) Configure port forwarding:
        ? Select the type of service or application for which you want to open the port (e.g., HTTP for a web page, which is our case).
        ? Set the local IP address of the device (the computer or server hosting the web page has a local LAN IP address).
        ? Specify the external port (the one that will be opened) and the internal port (the port of the local device).
        ? Choose the protocol (TCP or UDP. TCP in our case).
        ? Enable the port forwarding rule. d) Save the changes: Once configured, save the settings and restart the router if necessary.
Note: Each router has a different interface, so the steps may vary. Therefore, no other procedures for configuring Port Forwarding are provided, as each user’s router is different from another’s, so consult your router’s manual or search for specific Port Forwarding guides on the Internet. Ask your Internet service provider if the service needs to be activated by your ISP or if you can act independently through your router. The rules vary from provider to provider. Also, ask if the Port Forwarding configuration is available for a fee (by calling 199*****) or if it is completely free. 7. Activate a DDNS Service (Optional): Activate a DDNS service (optional) that provides a fixed domain (www.ddns.domain.com) through which the Web App can be accessed remotely. Note: not mandatory, as the app is also accessible via IP, but the director will always have to communicate any changes to the control room IP to the remote speaker.
8. Browser Compatibility: Chrome Version 126.0.6478.127 (Official Build 64-bit), Edge Version 126.0.2592.87 (Official Build) (64-bit), and Firefox 127.0 (64-bit). Internet browsers must support the JavaScript language, so make sure it is enabled to use all the features offered by the App. 9. Minimum Graphic Resolution: Minimum graphic resolution of 1600x900 pixels (HD) and minimum text size. For lower resolutions, the correct layout of the contents is not guaranteed. 10. PC Requirements: PC with iCore5, at least 16GB RAM, Windows 10 or 11, and a minimum 250GB SSD.
11 - Physical Mixer Solution An audio device with at least 3 channels (1 Mic and 2 tape/aux) and a number of physical cables whose number and type depend on the connections to be made. The number of connections to be made is 2; the first between the output of sound card 2 and the AUX input of the mixer, while the second connection is between the OUTPUT of the mixer and the LINE IN input of sound card 2. Note: sound card 1 will be used only for the audio output of the RadioDJ control room.

5 - Configuration Files (serv_inc.php and config.php) to Edit The files are located in the folder C:\xampp\htdocs\YourWebAppFolder. They contain lines related to database access data and information for the correct functioning of the Rest Server plugin. The information must be consistent with the environment in which the Web App is running. Below are some lines from the files that need to be modified with the correct data:
PHP
// Insert MySQL Server information
---------------------------------------------- serv_inc.php -----------------------------------------------------
$mysqli_server = "127.0.0.1"; // IP of the MySQL server; If the Web App is installed on the same PC as RadioDJ, the IP is 127.0.0.1;
$mysqli_database = "InsertDBName"; // name of the MySQL database;
$mysqli_user = "root"; // MySQL database username. Usually "root";
$mysqli_pass = "InsertYourPassword"; // MySQL database password;
$mysqli_port = "3306"; // MySQL port number. The default value is 3306;
$def_timezone = 'Europe/Rome'; // Time-zone setting. For Italy, the value Europe/Rome is correct;
-----------------------------------------------------------------------------------------------------------------------
// Insert REST server plugin configuration data.
$ipAddress = "127.0.0.1"; // IP of the Rest Server. Leave the default IP 127.0.0.1;
$restPort = "5555"; // TCP/IP port. Leave the default value 5555;
$restPassword = "InsertYourPassword"; // must be identical to the one configured on the plugin in the control room (see also Chapter 6)
---------------------------------------------- serv_inc.php ------------------------------------------------------
------------------------------------------------ config.php ------------------------------------------------------
// Insert REST server plugin configuration data.
$ipAddress = "127.0.0.1"; // IP of the Rest Server. Leave the default IP 127.0.0.1;
$restPort = "5555"; // TCP/IP port. Leave the default value 5555;
$restPassword = "InsertYourPassword"; // must be identical to the one configured on the plugin in the control room (see also Chapter 6)
------------------------------------------------ config.php ------------------------------------------------------
6 - Configuration of the Rest Server Plugin on the RadioDJ Control Room Start the RadioDJ control room and from the OPTIONS>PLUG-INS toolbar, click on the Rest Server plugin. A window will open where parameters need to be configured, such as:
    1. IP and port. In this field, enter http://127.0.0.1:5555;
    2. Password. In this field, enter a password that must match the password you entered in the serv_inc.php or config.php file (see Chapter 5);
    3. Auto start. Check the blue square. The square must have a checkmark;
    4. Log Activity. Check the blue square. The square must have a checkmark;
    5. The service start button must be on started and green. If you notice that the service is STOPPED, click on stopped to start the service.

7 - Download and Installation of Xampp Version 7.1.26 This is the procedure to download and install XAMPP on a 64-bit PC with Windows 10/11:
    1. Go to the XAMPP website at www.apachefriends.org. Now you need to download the version for which the App has already been tested. To get this version, select “DOWNLOAD” > then “MORE DOWNLOAD” > then “XAMPP WINDOWS”, then look at the bottom of the older packages and click on “7.1.26” to download xampp-windows-x64-7.1.26-1-VC14-installer.exe, finally double-click on the installation file.
    2. Click the Yes button when prompted. This will start the XAMPP installation wizard.
    3. Click the Next button. Before selecting the XAMPP features you want to install, you need to choose whether to continue using the current database manager or the new MySQL database manager of XAMPP. If you decide not to install the XAMPP database manager, it will not be necessary to select it, so it will be one less element to install. If you want to use the new MariaDB (MySQL) database manager, you will need to check MYSQL to install the element. The configuration is described in the following chapter, which is Chapter 8;
    4. Select the XAMPP features you want to install (in our case MariaDB[MySQL] (YES/NO), the choice depends on the database manager you have chosen to use (see point 3), PHP (mandatory), and APACHE (mandatory)). Review the list of XAMPP features displayed on the left side of the window.
    5. Click the Next button. Select the installation folder. Click on the folder icon to the left of the current installation directory. Click OK. This way, the selected folder will be used as the installation directory for XAMPP.
    6. Click the Next button. Uncheck the “Learn more about Bitnami” checkbox, then click Next to start the actual installation of XAMPP.
    7. Once the installation is complete, you can start the XAMPP control panel, where you can start and stop services like Apache and MySQL (optional). You can test your installation by opening your browser and typing localhost, which will take you to the XAMPP dashboard.
8 - Choosing the New MariaDB (MySQL) Database Manager of XAMPP Before performing any operations on the database, it is necessary to export/backup the database using the DATABASE SETUP utility of RadioDJ located at C:\RadioDJ\Setup\DatabaseSetup.exe. Start the utility, select BACKUP DATABASE, and the message EXPORT COMPLETED will be displayed. The produced file is located in the folder C:\RadioDJ\Setup\Backup and is a file with a name like (20240707 160000) and with a .SQL extension. The name indicates the year, month, day, and time it was created.
If you have chosen to keep the current database manager during the XAMPP installation, it will not be necessary to choose MySQL among the services to install, but it will be useful to select only the PHP and APACHE modules.
If you no longer want to use the current database manager and want to switch to MySQL of XAMPP, you must first proceed with the installation and start of the service and configure it as follows: a) Start XAMPP’s phpMyAdmin at http://127.0.0.1/ b) From the toolbar, select PHPMYADMIN and then select DATABASE; c) A window will open where you can enter the DATABASE name and select the CHARACTER SET; d) Enter the DATABASE NAME and leave the default CHARACTER SET unchanged, which is LATIN1_SWEDISH_CI, then select the CREATE button;
e) At the top left, you will see the database that has just been created along with others already existing. Click on the newly created database, then go to PRIVILEGES to create the database user and related permissions;
f) Click on ADD USER ACCOUNT and fill in the login information by choosing: – USERNAME > testing010824 – HOSTNAME > localhost – PASSWORD > mypassword – RE-ENTER PASSWORD > mypassword scroll down to – PRIVILEGES > click on SELECT ALL; go to EXECUTE by scrolling down to the bottom right. g) Now it is necessary to copy the information just entered onto a sheet, as it will be reported on the DATABASE SETUP utility of RadioDJ located at C:\RadioDJ\Setup\DatabaseSetup.exe. Start the utility and enter the following information in order:
    1. MySQL Server > IP_LOCALHOST < is 127.0.0.1
    2. MySQL Database > DATABASE_NAME (the one you chose in Chapter 5)
    3. MySQL Username > YOUR_USERNAME (the one you chose in Chapter 5)
    4. MySQL Password > YOUR_PASSWORD (the one you chose in Chapter 5) Select VALIDATE and check at the bottom left if the database is online. If everything went well, you will see - MSQL SERVER IS ON-LINE - in green. Finally, edit the serv_inc.php file with the information (see Chapter 5).

9 - Moving the ArtWork (mp3 file covers) from the Control Room Folder to the Web App Folder This operation is necessary to avoid the lack of ArtWork display within the Web App. Proceed as follows: from the RadioDJ toolbar, click on OPTIONS> OPTIONS>Other Settings, then go to Artwork Storage Path and take note of the path. Move all the ArtWork from the Artwork Storage Path (the one you noted) to the Xampp path, for example: C:\xampp\htdocs\AppFolder\Album-Art. Then, to avoid repeating the same operation of moving the ArtWork every time you import new audio tracks, change the control room’s Artwork Storage Path to that of the Web App so that each imported mp3 file saves the ArtWork on the Web App path: C:\xampp\htdocs\WebApp\Album-Art.
10 - Starting RadioDJ and Xampp in Administrator Mode This procedure is strictly necessary because without this permission, you cannot access the configuration mode to modify some parameters of RadioDJ and Xampp. To access Administrator mode, select the application icon to start; in this case, RadioDJ or Xampp, and right-click, select “Show more options”> Properties > Advanced > then > Run as administrator (check the box)> OK > Ok and exit.

11 - Testing the App Rest Web Panel and Troubleshooting At the end of the various configurations and settings, it is necessary to test the App locally before making it available to the remote speaker. Therefore, at the address http:\localhost\WebApp or http:\127.0.0.1\WebApp, you can view the App. This consists of a right part and a left part that will show warnings in case of configuration problems with the serv_inc.php or config.php files. The left part will give warnings of any issues related to the Rest Server plugin, while the right part will give warnings of any database-related problems. For issues with the lack of ArtWork display, repeat the steps in Chapter 9, while for display problems in the right or left section, refer to Chapters 5 and 6.

12 - How to Get the Best Performance and Operating Conditions from the App Rest Web Panel Evolution The App normally operates in the foreground and only in some cases will it operate in the background, for example, when working with another application simultaneously. In the latter case, the timings may vary compared to the control room counters. To remedy any timing variations, it is necessary to reload the web page so that all counters will be synchronized with those of the RadioDJ control room. Another case where you need to reload the App is when there are HTTP errors (data transmission errors) detected by some App scripts, and the errors appear in the left window. The displayed messages can and should be cleared with a reload to avoid blocking the App.

13 - Mode and Order of Starting the RadioDJ, Xampp, and App Rest Web Panel Evolution Applications a) Start XAMPP (with or without MySQL) and APACHE through the control panel, then verify through DatabaseSetup.exe that the MYSQL server is online, and if everything is ok, you can proceed to the next step. b) Start RadioDJ, and when it is playing audio tracks, you can proceed further. c) Start Rest Web Panel Evolution to perform a test, which can be done by opening the web browser at the address: http://127.0.0.1/YourWebAppFolder.

14 - Connections Between Mixer and Sound Card for Live Broadcast with Rest Web Panel and Remote Speaker Audio contributions can be derived from Facebook or Skype chats (single or group), etc., and will be channeled into the control room through a physical mixer and physical cable connections. For this setup, you will need an audio mixer with two available audio channels: one for the microphone and the other for auxiliary (aux). The microphone channel will be used in the studio where the RadioDJ control room is located by a speaker or a director as an intercom to communicate with the remote speaker. The AUX channel must be connected to the output of the second sound card 2 (the additional one). Finally, the mixer output must be connected to the LINE IN input of the same sound card. Perform tests to adjust the levels of the various sliders. This setup allows for smooth and high-quality communication during live broadcasting with a remote speaker. Remember, sound quality can also depend on the quality of your hardware (microphone and mixer) and the internet connection. Once done, the remote speaker must activate the communication channel by pressing the MICROPHONE-OFF button from the remote control panel, which will turn RED flashing with the ON-AIR indication. After finishing speaking, click the ON-AIR (RED flashing) button to close the communication channel, and the button will change from ON-AIR (RED flashing) to MICROPHONE-OFF, making it impossible to speak.

15 - Procedure and Setup for Broadcasting with the Remote Speaker The remote speaker/director, after connecting and authenticating at the address http:\IP_ADDRESS\WebApp, must set the AUTODJ/MANUAL selector to MANUAL (RED button). In this mode, the playlist will no longer be generated automatically by track rotation, but an on-the-fly playlist must be created by adding tracks with ADD TOP or ADD BOTTOM from the search section on the right. Then, operate the AUTOMATED/ASSISTED selector to decide whether the tracks should go live automatically or with the intervention of the speaker/director. If you have chosen the AUTOMATED mode (GREEN button), the tracks will be started automatically, while in ASSISTED mode (RED button), you will manually start the on-the-fly playlist tracks and can intersperse the speaker’s vocal part with the musical tracks.

16 - Restricting Access to phpMyAdmin in Your XAMPP Environment to Localhost Only Modify your Apache server settings to allow access only from localhost (127.0.0.1). Here’s how you can do it: a) Find the Apache configuration file (httpd.conf), usually located in the apache\conf folder in the XAMPP installation directory. b) Open the httpd.conf file with a text editor. c) Look for the <Directory> section that contains the path to the phpMyAdmin directory. It might look like this:
<Directory "c:/xampp/phpMyAdmin">
</Directory>
d) Inside this <Directory> section, add the following lines:
Order Deny,Allow
Deny from All
Allow from 127.0.0.1
Your file should now look like this:
<Directory "c:/xampp/phpMyAdmin">
    Order Deny,Allow
    Deny from All
    Allow from 127.0.0.1
</Directory>
e) Save the httpd.conf file and restart Apache. This should restrict access to phpMyAdmin to localhost (127.0.0.1), meaning only the computer hosting the XAMPP server can access phpMyAdmin. You should also consider using a strong password for the MySQL root account (see Chapter 17).

17 - Using a Strong Password for the MySQL Root Account in XAMPP It is very important to use a strong password for the MySQL (MariaDB) root account in XAMPP to enhance security. Here’s how you can change the root account password in XAMPP: a) Open the XAMPP control panel and click on ‘Shell’ to open it. b) In the command prompt, type the following command to change the password:
mysqladmin.exe -u root password NewPassword
Where NewPassword is the new password you want to set. When using the command mysqladmin.exe -u root password NewPassword, you do not need to enter the old password. Replace NewPassword with the new password you want to set for the MySQL root account. Additionally, it is good security practice to change passwords periodically. This helps prevent malicious activities, especially if you use the same password for multiple accounts. Finally, make sure to update the password in the phpMyAdmin configuration file located in the ‘C:\xampp\phpMyAdmin’ folder (config.inc.php). Look for the following line and replace it with your new password:
PHP
$cfg['Servers'][$i]['password'] = 'NewPassword';
Remember to restart Apache and MySQL after changing the password.

