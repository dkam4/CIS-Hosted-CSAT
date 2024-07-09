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

### Users and Privileges

There are 3 types of users in CIS-Hosted CSAT: 

| User Type   | Permissions |
| ----------- | ----------- |
| Primary Owner      | Access to full functionality for the organization and all sub-organizations       |
| Admin   | Access to all the functionality and dashboard for the organization, but does not have access to sub-organizations        |
| Basic User/Member  |  Access to Sub-Controls that are assigned to the user

Here are some use case examples;

- Admin user would have access to the full assessment and assessment history of the organization in question, but not of the sub-organizations.  The Admin would be able to create/delete assessments for their organization, and would be able to add/delete users to that organization, not for any of the sub-organizations.

- If you do not want a user to have access to add/delete users, or create/delete assessments in that organization, you could go with a basic user/member, and assign that basic user to all Sub-Controls or a subset of the Sub-Controls.  With the new bulk assignment ability in CIS CSAT v1.3.0 it is easier to assign a large number of Sub-Controls to a single user.

  
