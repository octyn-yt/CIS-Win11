# CIS-Win11
A LGPO Configuration to apply CIS Windows 11 Standalone V3.0 settings.
This is only for computers with group policy so basically windows 11 Pro as home doesnt have it included.

Tutorial:

Step 1 - Download lgpo.exe from here: https://techcommunity.microsoft.com/blog/microsoft-security-baselines/lgpo-exe---local-group-policy-object-utility-v1-0/701045

Step 2 - Place the LGPO.exe file in C:\Windows\System32

Step 3 - Download this as a zip and extract it. Put the extracted {57575CD3-B412-457B-9CD0-672A38BA438C} folder in the root of a usb or the location you want it to be in. This should be the folder with Backup.xml, etc.

Step 4 - Make a backup of your group policy settings just in case. Open command prompt as administrator and run 'LGPO.exe /b (the directory to where you want the backup - NOT THE SAME AS THE DOWNLOADED FILE)' without the quotes and changing the brackets to the directory.

Step 5 - Now run the following command in command prompt as admin 'LGPO.exe /g (The directory with {57575CD3-B412-457B-9CD0-672A38BA438C} in)'. If it gives you an error then run it again. If it shows the bitlocker prompt just close that instead of selecting an option.

Step 6 - Finally, run this last command 'gpupdate /force'. If it throws and error then run it again. Now restart your computer.
