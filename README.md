PS3 Update Downloader
-=-=-=-=-=-=-=-=-=-=-

written by neocatzeo
https://www.youtube.com/user/neocatzeo
twitter: @neocatzeo
Date: June 12 2022
Version 1.0


Overview:
This program will load a list of PS3 game title ids, create folders for each, download update package XML manifests, and download update package files.  This is meant to automate the process of downloading the enourmous number of package files that can exist for a collection of ps3 games.  The ultimate purpose is for archiving update files.


Usage:
Update games.txt with a list of desired game title ids.  Each PS3 game has it's title id on the spine of the case at the bottom.  When reading codes off of game cases, sometimes the last few characters sometimes need to be omitted.  Example Batman:Arkam City "BLUS30538L" should instead be listed as "BLUS30538".  When you are satisfied with your list, simply run PS3UpdateDownloader.exe.  This will process the list and create folders for each game in the same directory.


A log will be generated in log.txt, you will want to check this to see a list of files that did not download correctly.  In some cases you can paste the url given into a web broswer and manually download the the file.  Otherwise running the program again will make it try to fill in the missing files.  A browser is a bit more sophisticated and sometimes has an easier time grabbing the odd file.


Microsoft Background Intelligent Transfer Service (BITS):
This program will download Sony's update manifests, which are stored as XML files using BITS.  These store the links to updates and other things.  This is because Sony's HTTPS certificate is expired, and this is a way for the program to ignore the error and download the file.  You'll see this come up in a separate window.  This was a work around for the programming language this tool was programmed in.


Failed Downloads:
Due to how the app is made, how Sony operates their servers, and the internet, you'll likely see a bunch of failed file downloads.  It's always best to run the tool several times to try and get it to fill in any failed downloads.  The app will attempt to retry, however it seems sometimes that doesn't work and running the app later can.  If it reports a complete failure, then it's likely that game id is not on the server at all (double check your game id).  Otherwise you can copy any failed download links from the log file.  In many cases a browser can just grab failed files that didn't cooperate.


Requirements:
This is tested on Windows 10, however it should run on most versions of Windows, XP, Vista, 7, 8, 10, 11.
You may need to download and install Microsoft C++, Direct X 9.0c redistributables.
You need write permissions to the programs folder since it dumps everything into it's folder.


Open source:
The source code is provided, written in Dark Basic Professional 1.077


Liability:
This program is provided as is without warranty.  You are free to use and distribute as you see fit.  Please include the original files.
