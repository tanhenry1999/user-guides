---
layout: default
title: AS Budget Sheets
nav_order: 3
---
## Introduction
{: .no_toc }
This technical document is intended for instruction on how to use the AS Monthly Budget using Google Sheets.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Location on Google Drive

1. Navigate to:
	- -> Google Drive -> Accounting
	- -> AS Monthly Budget Reports

	![gd-1](./images/gd-1.jpg)

## Folders and Files Within "AS Monthly Budget Reports" Folder

1.	- The “AS Monthly Reports” folder is where accounting will upload the files/report.  

	- The “AS Monthly Reports Project Backend (IT USE ONLY)” will be explained later.

	- The “Inactive Agency & Budget” spreadsheet will be maintained by accounting. It contains all the inactive emails for agencies and departments.

	- The “Send Mass Emails for AG01” spreadsheet is maintained by accounting. This spreadsheet is used to send monthly emails to AG01 (Axxxx) accounts and it store emails addresses and information for each account.

	- The “Send Mass Emails for CR02 & IS03” is also maintained by accounting. This spreadsheet will send monthly emails to CR02 (4xxxx) and IS03 (4xxxx) accounts. It also stores email addresses and information for each account.


## AS Monthly Reports Folder

1.	- As stated before, the “AS Monthly Reports” folder is where Accounting will upload all the reports. 
	- Inside the “AS Monthly Reports”  folder, there will be folders dedicated to each year and all the reports for that year, will go into that year’s folder. For instance, all the reports for 2020 will be uploaded in the 2020 folder. 

	![gd-2](./images/gd-2.jpg)

	- Inside each yearly folder, there will be 12 sub-folders, one for each period.

	![gd-3](./images/gd-3.jpg)

	- When Accounting uploads  the folder containing the reports, by default, each folder has the following name format: the word “PER” and a period “#”. For example, PER8. Each period folder will also have a sub-folder. By default, the sub-folder is called  “INCOME STATEMENT PROJECTS”.

	- It is important to rename each period folder and its sub folder when uploading them. If not, the script will detect multiple folder with the same name and it will not run successfully. For example, it will detect a folder called “PER8” in both 2019 and 2020 folder. 


	- Accounting will use a similar naming algorithm like the following, when renaming the folders. 

	- Renaming “PER#” folders:
		- YEAR | “PER”| period # 
		- 2020|PER|8
		- 2020PER8 🡨 final folder name.

	- Renaming “INCOME STATEMENT PROJECTS” folders:
		- YEAR | “PER” | # | “IS”
		- 2020 | “PER” | 8 | “IS”
		- 2020 PER8 IS 🡨 final folder name.


	![gd-4](./images/gd-4.jpg)

## Inactive Agency and Budget

1. 	- This sheet contains all the inactive email addresses for both Agencies & Budget. This sheet is maintained by accounting. This sheet is not connected to any script and it is just holds data for accounting. 

	![gd-5](./images/gd-5.jpg)

## Send Mass Emails For AG01

1.	- “Send Mass Emails for AG01” contains two sheet. The first sheet is called “AGENCY(Agency App. form)” and the second sheet is called “Send Emails”.

	- **“AGENCY(Agency App. form)” Sheet**:
		- This sheet contains all the email addresses and information for the AG01 (Axxxx) accounts. The data on this sheet is maintained by Accounting. 

	![gd-6](./images/gd-6.jpg)

	- **"Send Emails" Sheet:**
		- This is the sheet that Accounting will use to send monthly mass emails.

	![gd-7](./images/gd-7.jpg)

###  How to use “Send Emails” Sheet for “Send Mass Emails for AG01”

1. The user will input the name of the folder where reports/files for AG01 (Axxxx) accounts are located.

	![gd-8](./images/gd-8.jpg)

2. Next, the user will click on “Update Files”

	![gd-9](./images/gd-9.jpg)

	- When the “Update Files” button is clicked, the script will find the filename associated with each account and it will input the result in the columns below.  
	
	![gd-10](./images/gd-10.jpg)

3. The date will be entered next.

	![gd-11](./images/gd-11.jpg)

4. Once ready, the user will click on “Send Emails” button to send the mass emails.

	![gd-12](./images/gd-12.jpg)

5. When “Send Emails” button is clicked, a message will be shown on the screen. If the users clicks on “Yes” the emails will be send and if the user clicks on “No” the emails will not be send out.

	![gd-13](./images/gd-13.jpg)

	- When emails begin to be send out, the cells in  the “Fund Number” column will begin to have a red background color. The red color will indicates  that the email associated to that account has been sent out. The “Fund Number” column can be seen as a progress bar. Once the entire column is red, that means all emails have been sent out.   Sometimes the background color can be white and that means there is no email address associated with that account and therefore, the script will skip that account and jump to the next one. 

	![gds-1](./images/gds-1.jpg)

	![gd-14](./images/gd-14.jpg)

6. To clear the spreadsheet click on “Clear”.

	![gd-15](./images/gd-15.jpg)

### Simple Troubleshooting for “Send Emails” Sheet

1.	- Sometimes the functions attached to each button may be detached by user error. In order to solve this issue, attach the function back to each button. 
		- updateFiles() Function is attached to the “Update Files” button.
		- clear() function is attached to the “clear” button.
		- sendEmails() function is attached to the “Send Emails” button.
	- Follow the steps below to attach a function back to its button. 

	![gd-16](./images/gd-16.jpg)

	![gd-17](./images/gd-17.jpg)

	![gd-18](./images/gd-18.jpg)

## Send Mass Emails For CR02 & ISO3

1.	- The “Send Mass Emails for CR02 & IS03” contains two sheets. The first sheet is called “BUDGET(Auth Sig Form)” and the second sheet is called “Send Emails”. 

	- **“BUDGET(Auth Sig Form)” sheet:**
		- This sheet contains all the email addresses and information for CR02 & IS03 (4xxxx) accounts.  
	
	![gds-2](./images/gds-2.jpg)

	- **“Send Emails” Sheet:**
		- This is the sheet that Accounting will use to send monthly mass emails for CR02 & IS03 accounts.
	
	![gds-3](./images/gds-3.jpg)

### How to use “Send Emails” Sheet for “Send Mass Emails for AG01”

1. The user will input the name of the folder where reports/files for CR02 or IS03 accounts are located in the grey box shown below. (Both CR02 and IS03 account numbers start with 4xxxx).

	![gds-4](./images/gds-4.jpg)

2. Next, user will click on “Update Files”.

	![gds-5](./images/gds-5.jpg)

	- When the “Update Files” button is clicked, the script will find the filename associated with each account and it will input the result in the columns below.  

	![gds-6](./images/gds-6.jpg)

3. The date will be entered next

	![gds-7](./images/gds-7.jpg)

4. Once ready, the user will click on “Send Emails” button to send the mass emails.

	![gds-8](./images/gds-8.jpg)	

5. When “Send Emails” button is clicked, a message will be shown on the screen. If the users clicks on “Yes” the emails will be send and if the user clicks on “No” the emails will not be send out.

	![gds-9](./images/gds-9.jpg)

	- When emails begin to be send out, the cells in  the “Fund Number” column will begin to have a purple background color. The purple color will indicates  that the email associated to that account has been sent out. The “Fund Number” column can be seen as a progress bar. Once the entire column is purple, that means all emails have been sent out.   Sometimes the background color can be white and that means there is no email address associated with that account and therefore, the script will skip that account and jump to the next one. 

	![gds-10](./images/gds-10.jpg)

	![gds-11](./images/gds-11.jpg)

6. To clear the spreadsheet click on “Clear”.

	![gds-12](./images/gds-12.jpg)

### Simple troubleshooting for “Send Emails” Sheet

1.	- Sometimes the functions attached to each button may be detached by user error. In order to solve this issue, attach the function back to each button. 
		- updateFiles()Function is attached to the “Update Files” button.
		- clear() function is attached to the “clear” button.
		- sendEmails() function is attached to the “Send Emails” button.
	- Follow the steps below to attach a function back to its button. 

	![gds-13](./images/gds-13.jpg)

	![gds-14](./images/gds-14.jpg)

	![gd-18](./images/gd-18.jpg)

## How The Script Works For "Send Mass Emails For AG01"

The two spreadsheets which are used by the script are:

1.	- **Send Mass Emails for AG01 Spreadsheet**

	![gd-19](./images/gd-19.jpg)

2.	- **Agency Backend(IT USED ONLY) Spreadsheet**

	![gd-20](./images/gd-20.jpg)

	![gd-21](./images/gd-21.jpg)

### "Agency Backend (IT USE ONLY)" Spreadsheet

1.	- This is the backend sheet for AG01 or (Axxxx) accounts. The “B11:G1500” range on this sheet is synced with “B11:G1500” range on the “Send Mass Emails for AG01” spreadsheet. 
	- The formula used is “=IMPORTRANGE("https://docs.google.com/spreadsheets/d/1K2HGUUzYpS-CvqBXw-j3fCAKPBZSNOcnaAGItlXLYGY/edit#gid=0","B12:G1500")”  in cell B12 of the backend sheet. This formula allows the sync to happen. 

	![gd-22](./images/gd-22.jpg)

### How the script uses “AS Monthly Reports Project Backend (IT USE ONLY)” and “Send Mass Emails for AG01”  spreadsheets together. 

1. When the “Update Files” button is clicked, the script will go to Google Drive where “Send Mass Emails for AG01” sheet is located  and look for the folder name entered by the user in every folder and sub-folder. In this case the folder name is “2020PER8”.  

	![gd-23](./images/gd-23.jpg)

2. Once the folder has been found, the script will write all the file names in the “Agency Backend (IT USE ONLY)” Spreadsheet, column ‘O’. 

	![gd-24](./images/gd-24.jpg)

3. Then, the script will automatically match the first 5 characters of the filenames to the account numbers which are 5 characters long. If a match is found, then the data related to that filename will be placed under the columns with green headers. 

	![gd-25](./images/gd-25.jpg)

4. Then, the script will automatically copy and paste the information under the green headers to the “Email Sheet”.

	![gd-26](./images/gd-26.jpg)

5. After the script finishes running for “Update Files” button, then the user can put the date and click on “Send Emails”. The button “Send Emails” has been attached to the sendEmails() function in the script. So when clicked, the script will run and the emails will be send out. 

	![gd-27](./images/gd-27.jpg)

### Accessing the scripts for “Send Mass Emails for AG01”

In order to access the script for “Send Mass Emails for AG01”, click on tools and then <> Script Editor.
	![gds-15](./images/gds-15.jpg)

##### Button Functions location on the script 

To edit/update the updateFiles() function , click on mainData.gs file and look for the function.
	![gds-16](./images/gds-16.jpg)

To edit/update the clear() function , click on mainData.gs file and look for the function.
	![gd-28](./images/gd-28.jpg)

To edit/update the sendEmails() function , click on sendEmails.gs file and look for the function.
	![gd-29](./images/gd-29.jpg)

The scripts have been commented; therefore, easier to follow and make changes. 


## HOW THE SCRIPT WORKS FOR “SEND MASS EMAILS FOR CR02 & IS03” SPREADSHEET

“Send Mass Emails for CR02 & IS03” has the exact same logic as “Send Mass Emails for AG01”; however, it has different number of columns and different account number. The account numbers for CR02 and IS03 start with 4xxxx.

1.	- The two spreadsheets are used by the script:

**“Send Mass Emails for CR02 & IS03” Spreadsheet**
	![gd-30](./images/gd-30.jpg)

**Dep Backend (IT USE ONLY) Spreadsheet**
	![gd-31](./images/gd-31.jpg)
	![gd-32](./images/gd-32.jpg)

### Dep Backend (IT USE ONLY) Spreadsheet

1. 	- This is the backend sheet for CR02 & IS03 (4xxxx) accounts. The “B12:F1500” range on this sheet is synced with “B12:F1500” range on the “Send Mass Emails for CR02 & IS03” spreadsheet. 
	- The formula used is “=IMPORTRANGE("https://docs.google.com/spreadsheets/d/1K9R4ZDiBN_Ai7bpvjCMXNHOGsPGiUk0VArkt9dp46kI/edit#gid=0","B12:F1500")”  in cell B12 of the backend sheet. This formula allows the sync to happen. 

	![gd-33](./images/gd-33.jpg)

### How the script uses “Dep Backend (IT USE ONLY)” and the “Send Mass Emails for CR02 & IS03” spreadsheets together.

1. When the “Update Files” button is clicked, the script will go to Google Drive where “Send Mass Emails for CR02 & IS03” sheet is located  and look for the folder name entered by the user in every folder and sub-folder. In this case the folder name is “2020PER8”. 

	![gd-34](./images/gd-34.jpg)

2. Once the folder has been found, the script will write all the file names in the “Dep Backend (IT USE ONLY)” Spreadsheet, column ‘M’. 

	![gd-35](./images/gd-35.jpg)

3. Then, the script will automatically match the first 5 characters of the filenames to the account numbers which are 5 characters long. If a match is found, then the data related to that filename will be placed under the columns with yellow headers. 

	![gd-36](./images/gd-36.jpg)

4. Then, the script will automatically copy and paste the information under the purple  headers to the “Email Sheet”.

	![gd-37](./images/gd-37.jpg)

5. After the script finishes running for “Update Files” button, then the user can click on “Send Emails”. The button “Send Emails” has been attached to the sendEmails() function in the script. So when clicked, the script will run and the emails will be send out. 

	![gd-38](./images/gd-38.jpg)

### Accessing the scripts for “Send Mass Emails for CR02 & IS03”

In order to access the script for “Send Mass Emails for CR02 & IS03”, click on tools and then <> Script Editor.
	![gd-39](./images/gd-39.jpg)

##### Button Functions location on the script 

To edit/update the updateFiles() function , click on main.gs file and look for the function.
	![gd-40](./images/gd-40.jpg)