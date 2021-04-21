---
layout: default
title: Chrome
parent: Application Management
---
## SCCM - Chrome

1. Download Chrome MSI from [here](https://www.google.com/work/chrome/browser/).
2. Browse to \\Server\SCCM\Source\Software\
3. Create new folder and name "Chrome" (If folder exists, skip this step.)
4. Move Downloaded MSI file to the above directory created in step 3.
5. Open System Center Configuration Manager
6. Browse and expand to Software Library -> Application Management -> Applications -> STUAFF -> ASI
7. Expand ASI folder, if Chrome folder does not exists, Right click on ASI, Folder -> "Create Folder" Folder Name: "Chrome"
8. Right Click on Chrome folder and Create Application
9. Make sure radio button is active on "Automatically detect information about this ....
10. Browse to and Select the Adobe Reader MSI file
11. Next, Next
12. Fill out Specific information for Chrome, Make Sure to input Software Version
13. Installation Program: msiexec /i "Chrome_51.0.2704.63.msi" /q
14. Install behavior: change to "Install for system"
15. Next, Next, Close
16. Right Click on the package created.
17. Distribute Content
18. Next, Next
19. Click Add on right side and select "Distribution Point Group"
20. Check Box "All Distribution Points" then Ok
21. Next, Next, Close
22. Select the package created.
23. Bottom half of the screen select "Deployment Types"
24. Right click on deployment software then properties
25. Select User Experience tab, set "logon requirements: "Whether or not a user is logged on" and Installation Program Visibility: "hidden"
26. Apply, Ok