# CIS-Hosted CSAT User Guide


## Browser Requirements 

CIS-CSAT Hosted officially supports the Google Chrome Browser. Using other browsers, such as Firefox or Edge, can cause issues. 


## Terms of Use

Please read the [CIS-Hosted CSAT Terms of Use](https://csat.cisecurity.org/accounts/terms-of-use) prior to using CIS-Hosted CSAT.


## Privacy Policy 

Please read the [CIS-Hosted CSAT Privacy Policy](https://csat.cisecurity.org/accounts/privacy-policy) prior to using CIS-Hosted CSAT.


## Creating an Account

To create an account for CIS-Hosted CSAT, navigate to [https://csat.cisecurity.org](https://csat.cisecurity.org/) and select Register Now. Fill out the required information and select Sign Up. If your organization already has an account but you are not sure who is the owner, or if the owner is no longer with the organization, please submit a ticket to [CIS Product Support](https://cisecurity.org/support). 

If the organization website domain does not match the email domain, please follow these steps: 

1. Register for CSAT, entering your email domain in the Website field on the CSAT registration page.
2. Activate the new CSAT account using the activation email that you receive.
3. Once you are successfully logged into CSAT, click Administration on the left menu.
4. In the Administration page, click the Edit button for your organization.
5. In the Edit Organization pop-up, enter your organization’s correct website domain information.
6. Note: the website change might not immediately show up. You might need to click onto your Assessment Dashboard, and then go back into the Administration page to see the change.

If you already have a CSAT account, are an admin, and would like add new users, see this [knowledge base article](https://cisecurity.atlassian.net/l/cp/pLhyB1PX). 

## The Basics

This section describes the basic CSAT Pro concepts including users, organizations, and assessments, as well as how they relate to each other.


### Login Page

Users can enter their username and password here to login. Usernames are not case sensitive. Users will receive a “Login failed. Username/Password was incorrect” message if the username was not recognized, or if the password provided was not the correct password for that username. If an account is disabled, login attempts for that username will receive an “Account disabled. Please contact your Administrator” message.

The Login page also has a “Forgot Password?” link below the username/password fields. Doing so will send an email to the email address on file for that username. The email will contain a link that will allow the user to reset the password for that account.


### Two-Factor Authentication
Multi-Factor Authentication (MFA) is required to login. After successfully entering their username and password, users will be brought to the OTP page. Here users will submit the One Time Passcode (OTP) that was sent to the email account associated with the username. If too much time has passed since the login, or the user enters too many incorrect OTPs, the OTP will become invalid and the user will need to login again to receive a new OTP.


### Users and Privileges [source](https://cisecurity.atlassian.net/wiki/spaces/SCFKB/pages/625672294/Users+and+Permission+for+CIS+CSAT+tool)

There are 3 types of users in CIS-Hosted CSAT: 

| User Type   | Permissions |
| ----------- | ----------- |
| Primary Owner      | Access to full functionality for the organization and all sub-organizations       |
| Admin   | Access to all the functionality and dashboard for the organization, but does not have access to sub-organizations        |
| Basic User/Member  |  Access to Sub-Controls that are assigned to the user

Here are some use case examples;

- Admin user would have access to the full assessment and assessment history of the organization in question, but not of the sub-organizations.  The Admin would be able to create/delete assessments for their organization, and would be able to add/delete users to that organization, not for any of the sub-organizations.

- If you do not want a user to have access to add/delete users, or create/delete assessments in that organization, you could go with a basic user/member, and assign that basic user to all Sub-Controls or a subset of the Sub-Controls.  With the new bulk assignment ability in CIS CSAT v1.3.0 it is easier to assign a large number of Sub-Controls to a single user.

  
### Home Page

Upon logging in to CSAT, a user will arrive at the Dashboard page. This page displays organization and assessment information that is specific to the current user. You can return to the Dashboard page by selecting “Dashboard” from the side menu at any point. The Dashboard page contains the following sections:

#### Organization & Industry Average, Completion & Validation Percentage [source](https://cisecurity.atlassian.net/wiki/spaces/SCFKB/pages/276267293/How+are+individual+organization+assessment+and+industry+average+scores+calculated+in+CSAT) 

**Organization Average** - 
The assessment average for the organization (shown as "Organization Average" on the main Dashboard and "Overall Score" on the pages for particular Controls) is calculated by averaging the scores of all applicable Controls in the assessment. All applicable Sub-Controls within a Control are averaged together to calculate the Control Average Score for that assessment. A Sub-Control's score is calculated based on the applicable scoring categories within that Sub-Control.

**Industry Average** - 
The assessment average for the industry your organization is apart of. The assessment level Industry Average(displayed on the Dashboard) for that industry is calculated by averaging the Organization Averages for all of the organizations in that industry.  (Note: this is different than averaging the Control Industry Average scores for all Controls in that industry). The Control Industry Average Score(Spiderweb on the Dashboard) for a particular Control is calculated by averaging the Control Average Scores for that Control in each of the organizations in that industry that have identified that Control as applicable. 

The industry type was selected during the creation of the organizaiton's CSAT account. If you don't remember which industry you selected, you can check by selecting "Adminstration" from the side menu. This will display the industry selected for the organization, as well as any sub-organizations. Selecting "edit" on the organization block will allow you to change industries. 

**Completion %** - 
The percentage of applicable Controls that have been completed. Once an applicable Control's four scoring categories have been filled out, the Complete button will appear. Once the Control is completed, the Completion % will be updated to reflect the change. 


**Validation %** - 
The percentage of applicable Controls that have been completed and validated. Once a Control has been completed, it needs to be validated. Once the control is validated, the Validation % will be updated to reflect the change. 


#### Sub-Organizations
Sub-organizations can be created in a CSAT instance. Only the organization's primary-owner can add sub-organizations. To do so, navigate to the 'Administration' section, and there will be a green 'Create' button to add sub-organizations.


![image](https://github.com/user-attachments/assets/d4622c75-576c-4994-806b-a43fdae46967)




### Assessments 
Admins can create assessments in the organizations that they administer. Each assessment will be open or closed. There can only be one open assessment per organization. Assessments begin “open” which means that users in that organization can work on those assessments based on their Organization Role. When an assessment is completed, an Admin can close the assessment. A “closed” assessment can still be viewed, but it cannot be edited. An Admin can re-open a closed assessment as needed. 

**Assessment History** - 
The Assessment History page displays all assessments that have completed for the organization. The Assessment Scores Graph displays the score for all previously completed assessments. To view an old assessment, click on the assessment box. This will bring you to the Dashboard page, and across the top of the screen the Assessment period will be displayed. The old assessment cannot be edited, it is view-only. 
Within the assessment block there are three icons. The green hourglass icon starts a new assessment using the data from this previous assessment. The green pen icon edits the name of the assessment. The red trashcan icon deletes the old assessment. 

#### Creating a New Assessment 
To start a new assessment, select the green box with the assessment name: 


![image](https://github.com/user-attachments/assets/8798f8bb-55f2-4003-9279-35a8c70e4dde)


The three options are: 

**Start New Blank Assessment** - Starts a new blank assessment 
**Start New Assessment Using Current Data** - Starts a new assessment with the current assessments data
**Start New Assessment With File Upload** - Starts a new assessment using a .xlsx file of a previously exported assessment

The CIS Controls version for an assessment can only be changed by starting a new assessment. 

