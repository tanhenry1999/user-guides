---
layout: default
title: CC Kiosk Setup
parent: Technical Documents
---

# CC Kiosk Setup

## Implementation of CC KIOSK Package
{: .no_toc }
---
Created by: Evan Wolfe, 04/24/2017

## Steps
---
1. Create CC laptop object in the AS OU in AD (top of the AS chain) for adding to the domain


2. Image laptop with created SCCM "BareInstall" offline image USB key


3. Log in as local admin, change computer name and add to the domain if the task sequence has not already.


4. Log out of local admin and log into windows with CCTEACHER domain account once computer has restarted and is on the domain (check DLINK for info). THIS IS REQUIRED FOR THE PROCESS TO WORK CORRECTLY, THE ACCOUNT NEEDS TO BE LOGGED IN PRIOR TO ANY OTHER STEPS.


5. Install the LockDown application. Run the install from the Downloads folder, so you do not get any desktop redirection errors.


6. Open the LockDown application, ensure that the CCTEACHER domain account is selected as the account to modify settings for. This should be default since you are loading the LockDown app while logged in as CCTEACHER. Import the CCteacher LockDown configuration settings file.

6.1. From the X: drive, copy the RDP file of the corresponding NUC that you are going to use, to the downloads folder.

6.2. In the LockDown app, navigate to Startup & Shutdown -> Windows Shell. Select custom, and ensure that the entry field is blank. Paste in: C:\Users\ccteacher\Downloads\NUCXXXX.rdp

NOTE: replace XXXX with the NUC name, for example: 130T

6.3. Save the settings to the CCTEACHER account in LockDown.


7. When you hit save in LockDown once the settings are imported, it is going to ask if you want to create a system restore point, just uncheck the box and save.


8. Close the application. Leave the machine logged on.


9. On a separate machine, log in with a domain admin account. In the AS OU, select the laptop you have added, and right click and select "move". Move the computer object to the proper AD OU (AS -> AS Childrens Center -> NUCLaptops).


10. Just to be sure, open Group Policy Management and verify that the OU is receiving the "STUAFF-AS-MSTSC" policy, and the "STUAFF-AS-CC-AUTOWIFI" policy.


11. Back on the CC laptop, open CMD and run a GPUpdate /force (run a couple of times to be sure)


12. Restart the laptop, and it should auto login and run the MSTSC kiosk mode. Verify the script is working by closing the MSTSC application and seeing if it automatically reloads.