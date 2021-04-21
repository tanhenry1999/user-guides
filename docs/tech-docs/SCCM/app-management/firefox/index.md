---
layout: default
title: Firefox
parent: Application Management
---
## SCCM - Firefox

1. Download Firefox from [here](https://www.mozilla.org/en-US/firefox/organizations/all/).
2. Browse to \\Server\SCCM\Source\Software\
3. Create new folder and name "FireFox" (If folder exists, skip this step.) then create folder with version number
4. Move Downloaded .EXE file to the above directory created in step 3.
5. Copy install.bat, install.cmd, local-settings.js, mozilla.cfg, override.ini files from \\Server\SCCM\Source\Software\FIREFOX to \\Server\SCCM\Source\Software\FIREFOX\(NEW VERSION DIRECTORY)
6. Right click on install.cmd and edit
7. Replace all occurrences of version# from old to new (3 locations)
8. Ctrl S to save, close
9. Open System Center Configuration Manager
10. Browse and expand to Software Library -> Application Management -> Packages -> STUAFF -> ASI
11. Expand ASI folder, if Firefox folder does not exists, Right click on ASI, Folder -> "Create Folder" Folder Name: "FireFox"
12. Right Click on FireFox folder and Create Package
13. Give Name: "Firefox ESR VER#", language: en_us, Version: ver#
14. Check "This package contains source files:" browse to the source \\Server\SCCM\Source\Software\Firefox\Ver#
15. Next, Next
16. Input Name "Firefox ver#", Command Line: Brose to source and change from "Executable files" to "all files"
17. Select install.cmd, open
18. Run: "Hidden", Program can run: "whether or not a user is logged on"
19. Uncheck "Allow users to view and interact with the program installation"
20. Next, Next, Next, Close.
21. Right Click on the package created.
22. Distribute Content
23. Next
24. Click Add on right side and select "Distribution Point Group"
25. Check Box "All Distribution Points" then Ok
26. Next, Next, Close
27. Select the package created.
28. Bottom half of the screen select "Programs"
29. Right click on deployment software then properties
30. Select Advanced tab
31. Check "allow this program to be installed from the install packages task sequence without being deployed"
32. Apply, Ok