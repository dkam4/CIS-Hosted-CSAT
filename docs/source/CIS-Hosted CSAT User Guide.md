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


### User Verificiation and Creation [source](https://cisecurity.atlassian.net/servicedesk/customer/portal/15/article/2536898747)

In CIS-Hosted CSAT, user verification generally happens automatically when a new user logs in for the first time.  There are two main ways a user can be created in CIS-Hosted CSAT:

1. A Primary Owner can add new users to the sub-organization
   a. This can be done by clicking Administration on the left menu
   b. Then clicking the Add button next to the Active Users heading on the Administration page
   c. And then entering the user's First name, last name, and email on the Add User page.  Adding that User should send an email to that user allowing the user to create a password and login.

2. If a user attempts to register for CIS-Hosted CSAT, and the email domain already matches an existing organization domain in CIS-Hosted CSAT, the user will need to be accepted by the Primary Owner of the organization. Note: the Primary Owner will not get an email that the user is trying to be added.  To accept a user in this way:
   a. The Primary Owner must visit the Administration page in the tool by clicking Administration on the left menu
   b. There is a User Requests section on the Administration page; if there are users waiting to be accepted, they should appear there, and the Primary Owner can click the Manage button there.
   c. This will go to the Users page; at the bottom of the Users page, the Primary Owner should see a "New User Requests" section if there are requests.  The Primary Owner can click the three dots in the Actions column and then click "Accept request" if they wish to accept that user, or "Decline request" if they wish to decline the user.

   **NOTE** Please note that the user request in option 2) will be directed by email domain and organization domain.  So, if the organization has a top-level organization and sub-organizations, it's possible that the user's request will end up in a different sub-organization than expected, or in the top-level organization when you're expecting it in a particular sub-organization, depending on the matching of the email domain to the organization domain in CIS-Hosted CSAT.

## The Basics

This section describes the basic CSAT Pro concepts including users, organizations, and assessments, as well as how they relate to each other.


### Login Page

Users can enter their username and password here to login. Usernames are not case sensitive. Users will receive a “Login failed. Username/Password was incorrect” message if the username was not recognized, or if the password provided was not the correct password for that username. If an account is disabled, login attempts for that username will receive an “Account disabled. Please contact your Administrator” message.

The Login page also has a “Forgot Password?” link below the username/password fields. Doing so will send an email to the email address on file for that username. The email will contain a link that will allow the user to reset the password for that account.


### Two-Factor Authentication
Multi-Factor Authentication (MFA) is required to login. After successfully entering their username and password, users will be brought to the OTP page. Here users will submit the One Time Passcode (OTP) that was sent to the email account associated with the username. If too much time has passed since the login, or the user enters too many incorrect OTPs, the OTP will become invalid and the user will need to login again to receive a new OTP.


### Home Page

Upon logging in to CSAT, a user will arrive at the Dashboard. This page displays organization and assessment information that is specific to the current user. You can return to the Dashboard by selecting “Dashboard” from the side menu at any point. 


Example of an admin's Dashboard: 

![image](https://github.com/user-attachments/assets/156d06e2-af2e-4f85-a7fe-4f0dda6df6f9)

<br> 

## Users and Privileges [source](https://cisecurity.atlassian.net/wiki/spaces/SCFKB/pages/625672294/Users+and+Permission+for+CIS+CSAT+tool)

There are 3 types of users in CIS-Hosted CSAT: 

| User Type   | Permissions |
| ----------- | ----------- |
| Primary Owner      | Access to full functionality for the organization and all sub-organizations       |
| Admin   | Access to all the functionality and dashboard for the organization, but does not have access to sub-organizations        |
| Basic User/Member  |  Access to Sub-Controls that are assigned to the user

Here are some use case examples;

- Admin user would have access to the full assessment and assessment history of the organization in question, but not of the sub-organizations.  The Admin would be able to create/delete assessments for their organization, and would be able to add/delete users to that organization, not for any of the sub-organizations.

- If you do not want a user to have access to add/delete users, or create/delete assessments in that organization, you could go with a basic user/member, and assign that basic user to all Sub-Controls or a subset of the Sub-Controls.  With the new bulk assignment ability in CIS CSAT v1.3.0 it is easier to assign a large number of Sub-Controls to a single user.

  

### Organization & Industry Average, Completion & Validation Percentage [source](https://cisecurity.atlassian.net/wiki/spaces/SCFKB/pages/276267293/How+are+individual+organization+assessment+and+industry+average+scores+calculated+in+CSAT) 


![image](https://github.com/user-attachments/assets/62ca4ae2-526e-45b9-a13b-32965a37c6a5)



**Organization Average** - 
The assessment average for the organization (shown as "Organization Average" on the main Dashboard and "Overall Score" on the pages for particular Controls) is calculated by averaging the scores of all applicable Controls in the assessment. All applicable Sub-Controls within a Control are averaged together to calculate the Control Average Score for that assessment. A Sub-Control's score is calculated based on the applicable scoring categories within that Sub-Control.

**Industry Average** - 
The assessment average for the industry your organization is apart of. The assessment level Industry Average(displayed on the Dashboard) for that industry is calculated by averaging the Organization Averages for all of the organizations in that industry.  (Note: this is different than averaging the Control Industry Average scores for all Controls in that industry). The Control Industry Average Score(Spiderweb on the Dashboard) for a particular Control is calculated by averaging the Control Average Scores for that Control in each of the organizations in that industry that have identified that Control as applicable. 

The industry type was selected during the creation of the organizaiton's CSAT account. If you don't remember which industry you selected, you can check by selecting "Adminstration" from the side menu. This will display the industry selected for the organization, as well as any sub-organizations. Selecting "edit" on the organization block will allow you to change industries. 

While the industry average information can be useful as a point of comparison for your organization, it should not be used to determine when your organization has reached an acceptable level of maturity in your implementation of the CIS Controls; the decision of what is an acceptable level of maturity for the CIS Controls implementation for your organization should be made only after performing a thorough risk analysis for your organization. The industry average information provided is based on the self-assessed industry identification and self-assessed Safeguard scoring of CSAT users; as such, this information is provided as a point of reference, and should not be the basis for organizational decisions.

There are separate industry averages based on which version of the CIS Controls (v7.1 or v8.0) is specified for the assessment.

**Completion %** - 
The percentage of applicable Controls that have been completed. Once an applicable Control's four scoring categories have been filled out, the Complete button will appear. Once the Control is completed, the Completion % will be updated to reflect the change. 


**Validation %** - 
The percentage of applicable Controls that have been completed and validated. Once a Control has been completed, it needs to be validated. Once the control is validated, the Validation % will be updated to reflect the change. 


## Control Implementation Average Bar Graph 

The Control Implementation Average Bar Graph can be found by scrolling down on the Dashboard. The numerical scores for the Control Implementation Averages bar graph (that determine the height of the bars and are displayed when you hover over a bar) represent the average for just the "Control Implemented" scoring category (and exclude the other 3 scoring categories). However, the colors of the bars in the graph correspond to the Control Average Score for that Control (which includes all 4 applicable scoring categories). This way, the bar colors for a Control are the same as the colors displayed in the heat map for the corresponding Control at the top of the Dashboard. It is the Control Average Score for the Control that matches the score ranges in the color legend. 

<br> 

![image](https://github.com/user-attachments/assets/0cb84bb1-e0da-4583-990b-05eed01ce965)



## Sub-Organizations [source](https://cisecurity.atlassian.net/servicedesk/customer/portal/15/article/2588705049)
Sub-organizations can be created in a CSAT instance. Only Primary Owners can create sub-organizations. Primary Owners can create sub-organizations with the following steps:

1. Click on Administration in the left menu
2. On the Administration page, click the Create button to the right of the "Secondary Organizations" heading
3. Fill out the information in the Create Organization pop-up (name, industry, website, IG, and Critical Controls Version) and click Save

Sub-organizations each have their own assessments, distinct from the assessments of their parent organization.  Once the sub-organization is created, you can navigate to that new sub-organization by selecting its name from the Organizations menu on the left.  With a sub-organization selected, you can add users to that sub-organization (see As an Org or Sub-Org Admin I'd like to add new users to CIS-Hosted CSAT. ), or create additional sub-organizations under it from the Administration page for that sub-organization.


![CSAT Suborg](https://github.com/user-attachments/assets/798c0544-f054-463b-8e5c-c2eb68fc2674)





## Assessments 
Admins can create assessments in the organizations that they administer. Each assessment will be open or closed. There can only be one open assessment per organization. Assessments begin “open” which means that users in that organization can work on those assessments based on their Organization Role. When an assessment is completed, an Admin can close the assessment. A “closed” assessment can still be viewed, but it cannot be edited. An Admin can re-open a closed assessment as needed. 


#### Creating a New Assessment 
To start a new assessment, select the green box with the assessment name: 


![new assessment](https://github.com/user-attachments/assets/98cbdcda-f57b-4ae3-884b-48ccdf502f47)



The three options are: 

**Start New Blank Assessment** - Starts a new blank assessment 

**Start New Assessment Using Current Data** - Starts a new assessment with the current assessments data

**Start New Assessment With File Upload** - Starts a new assessment using a .xlsx file of a previously exported assessment

The CIS Controls version can only be changed when starting a new assessment. 



**Assessment History** 
The Assessment History page displays all assessments that have completed for the organization. The Assessment Scores Graph displays the score for all previously completed assessments:


![assessment history](https://github.com/user-attachments/assets/ea89b5e3-c534-4452-ae04-49468443fae1)


To view an old assessment, click on the assessment box. This will bring you to the Dashboard page, and across the top of the screen the Assessment period will be displayed. The old assessment cannot be edited, it is view-only. 
Within the assessment block there are three icons. The green hourglass icon starts a new assessment using the data from this previous assessment. The green pen icon edits the name of the assessment. The red trashcan icon deletes the old assessment. 


### CSAT Scoring Categories Definitions
An organization can use the 4 scoring categories for whatever makes the most sense for your organization. In general, these categories refer to:

**Policy Defined** – to what degree is this Sub-Control covered by your organization’s policies?

**Control Implemented** – to what degree has your organization implemented this Sub-Control?  This can factor in coverage (such as what percentage of the machines in your organization have this Sub-Control implemented) and/or level of implementation (for instance, all machines in your organization could have the Sub-Control partially implemented).

**Control Automated** – to what degree does your organization enforce this Sub-Control through automated means vs. manual/procedural means?

**Control Reported** – to what degree is the state of this Sub-Control being reported within your organization, generally to leadership or management?  Are updates on the state of that Sub-Control's implementation getting to where they need to go (to the decision makers who can act on them, to those who can decide if the organization needs to invest more to improve that Sub-Control's implementation in order to reduce risk, to meet any reporting requirements the organization has including requirements from organizational policies or from regulatory requirements, etc.)?

### Score Color Legend

As the assessment is completed, the colors of the Controls will change based on the score: 
<br> 

![image](https://github.com/user-attachments/assets/77c992c5-0473-4ff1-b958-10ee51f01b04)


<br>


![image](https://github.com/user-attachments/assets/3c7f9d03-1ac6-4e65-835a-5097b0216e89)


<br> 

## CIS Controls

The CIS Controls are a prioritized set of actions that collectively form a defense-in-depth set of best practices that mitigate the most common attacks against systems and networks. The CIS Controls are developed by a community of IT experts who apply their first-hand experience as cyber defenders to create these globally accepted security best practices. The experts who develop the CIS Controls come from a wide range of sectors including retail, manufacturing, healthcare, education, government, defense, and others.

The CIS Controls v8.0 consists of 18 top-level Controls that serve as categories to house 153 Safeguards. Each CIS Safeguard is a specific action that can be implemented or activity that can be performed to improve an organization’s cyber defense program. The previous version of the CIS Controls, v7.1, consists of 20 top-level Controls that serve as categories to house 171 Safeguards.

To download the CIS Controls and see the other companion resources that are available, please visit the CIS Controls.

### Implementation Groups

In v7.1 of the CIS Controls, Implementation Groups (IGs) were introduced. Implementation Groups put the CIS Safeguards (known as CIS Sub-Controls prior to CIS Controls v8) into 3 groups to help organizations prioritize which Safeguards to implement first. CIS recommends that all organizations implement IG1, as the IG1 Safeguards represent essential cyber hygiene. Based on the resources available to the organization, as well the criticality of the data and services that the organization needs to protect, the organization can determine whether they should also implement additional Safeguards from IG2 and IG3. Each Implementation Group builds on the lower Implementation Groups; thus an organization implementing IG2 should also implement IG1, and an organization implementing IG3 should implement all three Implementation Groups.

The following are some general guidelines to help organizations determine which Implementation Groups are right for them:

#### IG1 

Organizations with limited resources where the sensitivity of data is low will need to implement the Safeguards that typically fall into the IG1 category.

#### IG2

Organizations with moderate resources and greater risk exposure for handling more sensitive assets and data will need to implement the IG2 controls along with IG1. These Safeguards focus on helping security teams manage sensitive client or company information.

#### IG3

Mature organizations with significant resources and high risk exposure for handling critical assets and data need to allocate the Safeguards under the IG3 category along with IG1 and IG2. The Safeguards that help reduce the impact targeted attacks from sophisticated adversaries typically fall into IG3.

A useful reference that lists all of the CIS Safeguards and which Implementation Group they belong to (for CIS Controls v7.1) can be found at: CIS Controls v7.1 Implementation Groups Reference.


