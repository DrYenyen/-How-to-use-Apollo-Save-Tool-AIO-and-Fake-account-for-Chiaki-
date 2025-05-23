# Usage Instructions

> This usage guide is maintained by [DrYenyen](https://github.com/DrYenyen/)

## NOTICE 
You must have a fake activated account or already have a real PSN account on the console to use saves from other users and properly export saves. 
* See [Activating offline profiles](#activating-offline-profiles) for instructions on how to activate an offline profile using your real PSN ID or allowing Apollo to create one.

## Table of Contents
1. [Title ID, User ID, and Account ID](#title-id-user-id-and-account-id)
2. [Apollo Save Tool Features and Options Overview](#apollo-save-tool-features-and-options-overview)
3. [Save Data Options](#save-data-options)
4. [Activating offline profiles](#activating-offline-profiles)  
5. [Getting saves and or managing them](#getting-saves-and-or-managing-them)    
6. [Fixing Keystone issues with savedata](#fixing-keystone-issues-with-savedata)
7. [Using FTP to Manage Saves](#using-ftp-to-manage-saves)    

## Title ID, User ID, and Account ID 
### What is a Title ID 
The Title ID is the Product code along with the unique numerical identifier of the game.     

The product code depends on the region, and the standard codes you’ll see are `CUSA`, `PCAS`, and `PLAS`.  
- R1 USA: `CUSA`        
- R2 Europe: `CUSA`     
- R3 Asia: `PLAS`, `PCAS`        
   
The product code is followed by a 5-digit unique number identifier.      
* For example Minecraft USA is `CUSA00744` while Minecraft EU is `CUSA00265`
* Another example: Resident Evil 2, USA is `CUSA09193` while Asia is `PLAS10335`
* The majority of games you come across will use `CUSA`.    

### What is a User-ID 
The user ID is the internal description for the local user account. (Example - `11cd8de`)

### What is an Account-ID
The Account ID is a PSN ID assigned to the local user. It must be 16 hex characters. (Example - `abcdef01234556789`) 
* To see yours and activate your offline console's user account with it or to generate a fake one for fake activation, read below.


## Apollo Save Tool Features and Options Overview 
The Apollo Main Menu has the following options.
### Trophies 
* Here you can backup or import trophies.
### USB Saves
* Here you can manage savadata you've put on the USB either from a PC or by copying it from the HDD by using the `Copy save game` option. Or import data you've moved around with PS4 Explorer. You can also import or export keystones when having a rare issue with save files see `Fixing Keystone issues with savedata` for instructions.
### HDD Saves
* Here you can manage savedata on the internal drive back it up, Resign it or export it for certain situations see `Managing save files from different CUSA IDs` for more information. Or import data you've moved around with PS4 Explorer. You can also import or export keystones when having a rare issue with save files see `Fixing Keystone issues with savedata` for instructions.
### Online DB/FTP Server
* To use this you need an active internet connection it will give you access to save files shared by the community. Alternatively if you have an FTP Server you can set it to show up instead of the Online DB by setting a FTP URL in settings and chagiong the Onilne Saves Server. 
### User Tools
* Here you can activate your local account with your real PSN Account-ID or allow Apollo to generate one for you to fake activate see `Activating offline profiles` for instructions. And you can also rebuild or backup your database. See `I rebuilt my database` for instructions.    
  * NOTICE restoring a database backup when the original users are not present or new ones have been added can cause issues. 
### User Tools Overview
1. Activate PS4 Accounts.
* This option allows you to fake activate accounts on your PS4 with either an auto generated ID or with your real PSN Account-ID for use with savedata transfers. See: [Activating offline profiles](#activating-offline-profiles)
2. App.db Database Management.
* This opton allows you to backuup, restore or rebuild your database. 

3. Show Parent Security Passcode. 
* This option allows you to view the parent code set to the current account. 
4. Network Tools (Downloader, Web Server)
1. Local Web Server (full system access)
*This option allows you to browse the internal storage and download files. The address is http://yourps4ip:8080. 
2. Toggel Web Browser history. 
* This option disables Browser history. 
3. URL link Downloader (http, https, ftp, ftps)
* This option allows you to download a file from a URL to the `/data/` path.
5. Extract Archives (RAR, Zip, 7z)
* This option allows you to extract available archives in the `/data/` path to their own folder in that path. 
### Settings 
* Here you can turn off the background music and animations.
* Select how saves are sorted. 
### Settings Overview
1. Background Music. 
* Toggles the background music. 
2. Menu Animations. 
* Toggles menu animations. 
3. Sort Saves. 
* Sets the savedata display order. 
4. USB Saves Sources. 
* Toggles between auto and specific possible locations.
5. Version Update Check. 
* Toggles version check when opening the app. 
6. Set FTP Server URL
* Allows you to set your FTP Server Address. 
7. Online Saves Server. 
* Changes between Online DB and FTP Server source for the home menu. 
8. Clear Local Cache. 
* Clears any cached files that Apollo uses for browsing OnlineDB and etc.
9. Update Application Data. 
* Updates savepatch data. 
10. Enable Debug Log. 
* Enables logging file location: /data/apollo/apollo.log
### About
Has credits, current Account-ID and console details.

### Icons to the right and left of saves
* Save files will have an indicator on the right and left based on user input and savedata status. 
1. The lock. (Located on the right when applicable)
* The lock indicates an encrypted save. If a lock is not present then the save is decrypted. 
2. Bookmark. (Located on the right when applicable)
* The bookmark indicates the save has the same Account-ID as the current user. 
  * An encrypted save can have both the lock and a bookmark. A decrypted save will have the bookmark when copied from the HDD (current user based) or resigned with the "Apply Changes & Resign" option.
3. The star. (Located on the left when applicable)
* The star shows up on the left of a save by clicking the touchpad while a save is highlighted which selects it, multiple saves can be selected.
4. Warning sign in red with "!"
* This usually indicates that the savedata is not in the appropriate folder structure and or location. (--- Encrypted save requires fimrware ???---)

## Save Data Options
* While accessing  USB Saves/HDD Saves submenus and Save file submenus you will see the following options. 
### Bulk Save Management
### In HDD Saves
1. Copy selected Saves to USB.
* This option copies saves highlighted with the touchpad to the plugged in USB drive in a decrypted format.
2. Copy all Saves to USB.
* This option copies all saves to the plugged in USB drive in a decrypted format. 
3. Start local Web Server.
* Starts Web Server (needs active internet connection) for easy browser access to backup savedata in decrypted format.
4. Dump all fingerprints
* Dumps all keystone fingerprints to a txt. 
### In USB Saves
1. Resign selected Saves. 
* Resigns all saves highlighted with the touchpad to the current Account-ID of the user. 
2. Resign all decrypted Save files. 
* Resigns all decrypted saves on the USB.
3. Copy selected Saves to HDD.
* This option copies encrypted and decrypted saves highlighted with the touchpad to the HDD. 
4. Copy all decrypted Saves to HDD. 
* This option copies all decrypted saves to the HDD. 
5. Start local Web Server. 
* Starts Web Server (needs active internet connection) for easy browser access to backup savedata in decrypted format.
6. Dump all decrypted Save Fingerprints.
* Dumps all keystone fingerprints to a txt. 

### In save file menus
1. Apply changes and resign. 
* Resigns after editing the HEX. Resigns after applying savepatch hacks. Resigns a save that was placed there externally.
2. View Save Details. 
* Displays Save details including location, Account ID and etc. 
3. Delete Save Game.
* WARNING THIS DELETES THE SAVE GAME FROM THE CURRENT STORAGE LOCATION.
### File Backup
1. Copy save game.
* This option copies decrypted savedata to a desired location.
2. Upload save backup to FTP.
* This option allows you to uplaod the current save file to your active FTP Server.   
  * Only shows up if an FTP Server has been set. Only availble in HDD Saves.
3. Export save game to Zip.
* This option copies savedata in an encrypted format in a zip to the USB.
4. Export decrypted save files.
* This option exports decrypted savedata to /data/apollo/User-ID/Title-IDofgame-metainfo.
5. Import decrypted save files. 
* This option imports decrypted savedata from /data/apollo/User-ID/Title-IDofgame-metainfo.
6. Hex Edit save game files. 
* Allows you to edit the savedata in HEX. 
### Keystone Backup
1. Export Keystone. 
* Exports Keystone to /data/apollo/User-ID/Title-IDofgame/keystone from the save. 
2. Import Keystone.
* Imports Keystone from /data/apollo/User-ID/Title-IDofgame/keystone to the save. 
3. Show Keystone Fingerprint. 
### Cheats
* Notice this option will show up only on supported games. It will allow you to edit the save file to add money, change stats and etc. 
1.  Select the options you want to load then select "Apply changes and resign" to save. 

## Activating offline profiles
* You can offline activate your local account on a jailbroken console to either match your legitimate PSN Account ID which will allow you to directly transfer save files via USB with no need for Save Wizard. 
* Or activate a local account for use with Chiaki and and proper save data management.
### To fake activate the account and make it match your PSN Account ID and use your PSN saves and Chiaki 
### Activated Console

1. On a console that has your legitimate PSN account copy a save file to a USB Drive.
2. Plug the USB Drive into a PC
   * On the USB, you will find the following folder path: `PS4/SAVEDATA/abcdef01234556789/CUSAxxxxx`
   * `abcdef01234556789` (is an example here), but for you, the one you see there is your PSN account ID. Take note of it for the next step.

### No console
1. If you don't have a console with your PSN account already activated.
   * Then go to [this website](https://psn.flipscreen.games/) put in your PSN username and then take the Account ID (for PSPlay) and convert it on [this website](https://www.rapidtables.com/convert/number/decimal-to-hex.html) from decimal to hex.
   * `abcdef01234556789` (is an example here) but for you the one you see there is your PSN account ID take note of it for the next step.

#### Account activation
3. Open Apollo Save Tool, navigate to User Tools.
4. Select Activate PS4 Accounts.
5. Select your profile.
6. Select the account you want to activate and press X.
7. A string of letters and numbers will show up you can replace them with the PSN account ID you got earlier.
8. Then press R2 then X and then keep pressing O till you are asked if you want to exit to the XMB accept then restart the console or sign out and back in.
9. Any saves you have can now be transferred via USB to a legit console as long as the title id matches and the game version is the same or higher.

### To fake activate for use with Chiaki and general save management 
Ignore if you have done the above option and already have an activated account go to Getting the ID needed for Chiaki if needed.

1. Open Apollo Save Tool, navigate to User Tools.
2. Select Activate PS4 Accounts.
3. Select your profile.
4. Select the account you want to activate and press X.
5. A string of letters and numbers will show up copy them CORRECTLY then press R2 then X and then keep pressing O till you are asked if you want to exit to the XMB accept then restart the console
* The string can be found in About in Apollo Save Tool in case you lose it.

### Getting the ID needed for Chiaki
This works for both the PSN account ID activated profile and for a normal Apollo fake activated account.   
1. You will take your Account-ID and convert it on the website below.    
   * [Already loaded here](https://trinket.io/embed/python3/ba2ff26973)
3. Once you are ready to run the code paste the string of the ACCOUNT-ID (example > `abcdef01234556789`) in the `user_id = "here"` between the 2 "" as seen in the code then run it. (ignore that it is named user-id in the script it is the account-id)
4. You will then receive a new string of letters and numbers (example > `CN8aubEclS6=`) you can then use that with Chiaki to use remote play or continue to utilise the offline activated account for savedata management.


## Getting saves and or managing them 
There are many ways to download or manage savedata here are some of the easiest ways.   

### Online database  
The online database is an ever-growing collection of save files for PS2, PS3, and PS4 games. Users can also submit their own save files.
1. Simply navigate to online database section, select your game, and download to a USB drive or to your internal HDD.
2. Navigate to either USB saves or HDD saves, depending on where you chose to save them.
* If you selected HDD saves, check to see if they appear in the HDD saves section.
* If you selected USB saves, navigate to USB Saves and select `Copy save game` to HDD.

### Copying saves between multiple profiles
This is useful if you have multiple accounts like User1, User2, etc.
1. Simply navigate to HDD saves  `Copy save game` and select to USB.
2. Log in to your secondary profile.
3. Navigate to USB, select `Copy save game` and select the HDD.

### Managing your Decrypted saves 
1. You can export and import decrypted savedata by using the option `Copy save game` in Apollo. Or the Export/Import Decrypted save files options but they send the data to the internal drive. Or the Export to Zip option.
2. When using the `Copy save game` option Apollo copies decrypted savadata to the following path
   *  `/PS4/APOLLO/<USER-ID>_<title-id>_<Save-name>`       
with files and a sce_sys folder inside.   
3. When importing it not needed for the folder path to end with  
   * `<USER-ID><title-id><Save-name>` the `title-id` is enough.      
But a proper structure with savedata and a sce_sys folder is needed.
4. When you decrypt a save file you are then one step closer to editing it if tools or documented methods exist for the specific game.
To copy it back to the HDD later select `Copy save game` and select the HDD.

### Managing Encrypted save data tied to your account
You can import and export savadata by using the Application Saved Data Management option in Settings on the PS4.
* This exports encrypted saves signed to the account id of the user exporting them and can usually only be used on the same user even on a different console unless Apollo or Save Wizard are used.
* To use your savedata on a jailbroken and retail console see Activating offline profiles. Otherwise export and import as needed. Using the option `Copy save game` or `Export save game to Zip` in Apollo and backing it up to a USB is suggested as it gives you decrypted savedata.

### Managing Encrypted saves acquired online
Encrypted saves are saves made from retail/unjailbroken PS4s made via Account Data Management feature or come from Save Wizard. 
* Note that Save Wizard is not needed. 
* Note that the saves must be from 11.00 or lower.

1. On a USB drive formatted as exFAT, put the saves in the following structure: `/PS4/SAVEDATA/ <ACCOUNT-ID> / <title-id>` and inside the ACCOUNT-ID should be a folder with the title id of the game `CUSAxxxxx` and inside it the save files.
   * The ACCOUNT-ID can be  `0000000000000000` or `abcdef01234556789` or any 16 hex characters. 
   * The title-id is that of the game for example `CUSA09193`. 
2. Back to the PS4, open the game the save was made for, and make a brand new save. 
3. Open Apollo Save Tool.
4. Navigate to USB Saves. Select the save.
5. Select copy to HDD. Select yes to resign it.
6. Check to see if the save is present in HDD Saves.
   * Note sometimes save files may display a ??? firmware warning in this case try the following.
7. Delete all savedata of the game on the HDD and create new savedata.
8. Export it via the Account Data Management feature from settings. Or for decrypted data `Copy save game` to USB.
9. Compare the online savedata names and make it match the one you just got from the console then try again.

### Managing Decrypted savedata acquired online
Decrypted saves are usually your own but sometimes are shared online.
* Note that Save Wizard is not needed. 
* If the save file you have has a `sce_sys` folder with a keystone and `param.sfo`
1. Put it in the following path on a USB drive formatted as exFAT `/PS4/APOLLO/<title-id>` and in Apollo go to USB saves choose the `Copy save game` option and copy it to the HDD.
   * If the save file is a file on it's own.
2. Plug in a USB drive formatted as exFAT into the PS4.
3. You will need to create a save in the game and then from Apollo in HDD saves use the `Copy save game` to copy the savedata to the USB.
4. Then in this path on the USB `/PS4/APOLLO/<USER-ID>_<title-id>_<Save-name>` find and replace the file inside with the file you alread have then back in Apollo in USB saves use the `Copy save game` option and copy it to the HDD.

### Managing save files from different CUSA IDs
This is a fix if you want to make use of files that are for the same game but different CUSA IDs or versions (such as standard vs deluxe/GOTY editions).
1. On the game you want the save to be applied to, make a new save.
2. Open Apollo Save Tool, select HDD saves. Select your save and select Export decrypted save files. Export all the files one by one.
3. Open PS4Xplorer, navigate to `/data/apollo/yourprofileid/` and simply rename the folder of the CUSA ID to the version of the game you need to have the game to.
4. Back to Apollo Save Tool, select HDD saves. Select your new game title ID, select Import decrypted save files. Import them one by one. Select Apply Changes & Resign.
5. Open your game. You should see the same name as before, but a different size or at a different point in the game.

### Managing save files from different Regions or Game versions
* This method also works like the option above it but is easier to do in some cases. 
* This is for if you have a save from EUR version of the game and want to make it work on a US game and etc. 
  * Source save means the save you want to convert to the other region. 
  * Target save means the donor save FROM the other region.
1. Decrypt the source savedata by copying it to the USB drive. 
2. Decrypt a target donor save from the other region of the game. 
* In the following steps ignore the sce_sys folder only copy and replace files outside of it. 
3. Copy the decrypted savedata from the Source save and paste it into the folder of the Target save and overwrite any duplicates. 
4. Go back to Apollo and copy the decrypted Target save to the HDD. 
5. Open the game.

### Fixing Keystone issues with savedata 
* Assuming the title id of the game or game version are not the issue sometimes you may do everything right but savedata always shows as corrupted. 
* This usually means the game you have or the game the save came from does not have a matching keystone this is usually an issue with dumped games as they are not rebuilt with the original keystone.
1. To fix this export the keystone from an already working save file and import it into the save file that you want to fix then copy the save file to the HDD and try it out.

### I rebuilt my database and now all my homebrew and games are gone how do I get them back?
1. Download the latest version Apollo Save Tool and put it in the root of a USB drive ( Has to be formatted in Exfat) then plug it into your PS4. 
2. Jailbreak your console as you usually do.
3. In GoldHEN Debug Settings before entering the Package Installer under it are some options make sure Enable Background Installation is NOT enabled.
4. Install Apollo and select yes to reinstall it if it asks you to ( This happens only if it was previously installed)
5. Open Apollo Save Tool and go to User Tools.
6. Then select App.db Database Management.
7. There you can select Rebuild App.db Database (Restore missing XMB items) and you can also select Rebuild DLC Database (`addcont.db`)
8. Then close Apollo and log out of and log in the user account for everything to properly show up.
* If you cannot see the games and apps on the home screen check in the PS4 Library App.
* Optionally you can then create a backup of your current database to use in the future with the restore option.

* NOTICE restoring a database backup when the original users are not present or new ones have been added can cause issues.


## Using FTP to Manage Saves
* The Apollo Save Tool FTP Server feature allows you to download and upload saves from an FTP server. 
## For local LAN servers you must be connected to the same network on both devices and a set up the necessary permissions. Optionally if you have a ftp server webhost or from a company ftp://66.77.88.99 , ftp://mywebhost.com , etc you can connect to the external server. 
* Local LAN is faster.
### FileZilla
1. Download and install FileZilla Server.
2. Open it and create a host user and password. 
3. Go to "Server" then "Configure" and in "Users" add a user and set a password for it from the right side under "Authentication:".
4. Go to "Mount points:" set the "Virtual path" as / and set the folder where you want the saves to be stored by pasting it's path or writing it manually.
5. To ther right of "Mount points:" make sure "Acess mode:" is set to "Read + Write" and that the first 2 boxes are ticked then press "Apply". 
6. Go to "Server listeners" and set the Protocol for all entries to "Explicits FTP over TLS and insecure plain FTP". 
7. Open the search bar and type in "Windows Defender Firewall with Advanced Security" go to Inbound Rules.
8. Choose "New Rule", set it to "Port" then press "Next". Set it to "TCP" and set the port to 21, then press "Next".
9. Leave "Action" at "Allow the Connection" and press "Next".
10. Tick all the boxes for "Where does this rule apply?" and press "Next" 
11. Finally name the rule and press "Finish"

### Native Windows FTP
* For Windows one of the best options is the FTP server that comes with it. Here is how to enable it.
1. In the search bar type in "Turn Windows features on or off" and open it.
2. Under "Internet Information Services" enable "FTP Server" and "Web Management Tools". Restart the PC to enable the features. 
3. If you do not want to use the credentials of your main user account create a new one.
4. Right click the Windows icon and choose "Computer Management" or search it in the search bar. 
5. Go to "Local Users and Groups" then go to "Users".
6. Create a new user name it and set the password, and remember them. (Set the password to never expire.)
7. Go back to the search bar and type in "Internet Information Services (IIS)" and open it. 
8. Open the dropdown on the left with the name of your device.
9. Click on the device name and under "IIS" find "Server Certificates" and go into it. 
10. Right click in empty space and choose "Create Self-Signed Certificate" give it a name and press "OK".
11. Right click on "Sites" and choose "Add FTP Site". 
12. Name it anything you want and set the path to where you want your saves to be uploaded to then click on "Next".
13. In "Binding" set the "IP Address" from "All Unassigned" to your current IP from the dropdown.(Open CMD and type in "ipconfig" if needed)
14. Leave the "Start FTP site automatically" enabled. 
15. Under "SSL" set it to "No SSL" or "Allow SSL".
16. Set "Authentication to "Basic". Set "Authorization" to "All users". Tick both "Read" and "Write" for permissions and click "Finish"
17. In "FTP SSL Settings" set the "SSL Policy" to "Allow SSL Connections".
18. Set the SSL certificate to the one you created previously you can select it from the dropdown then press "Apply" on the right side of the window.
19. Go to the FTP server you created and go to "FTP Firewall Support".
20. Under Data "Channel Range:" set it to 5000-51000.
21. Under "External IP Address of Firewall" set it to your current IP then press "Apply" on the right side of the window. (Open CMD and type in "ipconfig" if needed)
22. Open the search bar and type in "Windows Defender Firewall with Advanced Security" go to both Inbound and Outbound Rules and enable the FTP rules as seen in the pictures below.   
![-](imgs/1.PNG) 
![-](imgs/2.PNG) 
23. Back in "Internet Information Services (IIS)" right click on the FTP Site you created and go to "Manage FTP Site" and choose to restart it.
24. Restart the PC if you cannot connect from Apollo.
 

### On Android
1. On Android download any app that will allow you to be the HOST FTP server. The app "WiFi FTP Server" was tested and works for this. 
2. You have to set a username and password for the server WiFi FTP Server comes with the defaults of "android" for both but you can change them. 
3. Connect your phone to the same network as the PS4 and open Apollo. 

### On a NAS
* TrueNAS Scale will be used as an example. 
1. Add a new Dataset and name it whatever you want. For example: PS3saves
2. Go to "Credentials and make a new User and set a password and set the user directory as the Dataset you just created. 
3. Go to "System Settings" then "Services" and enable the FTP service, setting its path to the Dataset. 

### Connecting to the Server from Apollo
* The previously created FTP server credentials and IP are required. 
1. Download and install the latest version of [Apollo](https://github.com/bucanero/apollo-ps4/releases/latest).
2. Open Apollo and go to Settings.
3. Select "Set User FTP Server URL" and enter in your FTP server IP along with the username and password then press the start button.
4. The following structure is a template: ftp://username:password@192.168.0.1/
5. An example: ftp://peaches:mono58672@192.168.1.9
6. You can now upload saves to your FTP server by going into the save and choosing "Upload save backup to FTP". 
7. To download saves you have uploaded go to Settings and set the "Online Saves Server" to "FTP Server" as the source.
8. Return to the Apollo home screen , navigate to FTP Server, and download the desired saves.  