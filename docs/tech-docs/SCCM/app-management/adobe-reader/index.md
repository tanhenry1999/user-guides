---
layout: default
title: Adobe Reader
parent: Application Management
---
## SCCM - Adobe Reader
---
1. Download Adobe Reader MSI from [here](ftp://ftp.adobe.com/pub/adobe/reader/win/).
2. Browse to \\Server\SCCM\Source\Software\
3. Create new folder and name "Adobe Reader DC" (If folder exists, skip this step.)
4. Move Downloaded MSI file to the above directory created in step 3.
5. Open System Center Configuration Manager
6. Browse and expand to Software Library -> Application Management -> Applications -> STUAFF -> ASI
7. Expand ASI folder, if Adobe Reader DC folder does not exists, Right click on ASI, Folder -> "Create Folder" Folder Name: "Adobe Reader DC"
8. Right Click on Adobe Reader DC folder and Create Application
9. Make sure radio button is active on "Automatically detect infromation about this ....
10. Browse to and Select the Adobe Reader MSI file
11. Next, Next
12. Fill out Specific information for Adobe Reader, Make Sure to input Software Version
13. Installation Program: msiexec.exe /i "AcroRdrDC1500720033_en_US.msi" /qn /norestart
14. Install behavior: change to "Install for system if resource is device; otherwise install for user"
15. Next, Next, Close
16. Right Click on the package created.
17. Distribute Content
18. Next, Next
19. Click Add on right side and select "Distribution Point Group"
20. Check Box "All Distribution Points" then Ok
21. Next, Next, Close