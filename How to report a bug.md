Let's say that in your application under test you want to create a new user with user information. To do that you need to login into the application and navigate to USERS menu > New User, then enter all the details in the ‘User form’ like, First Name, Last Name, Age, Address, Phone etc. Once you enter all this information, you need to click on the ‘SAVE’ button to save the user. Now you expect to see a success message saying, “New User has been created successfully” as per the requirement/user story.

But when you entered into your application by logging in and navigated to USERS menu > New user, entered all the required information to create the new user and clicked on SAVE button. Instead of success message, your application crashed and you got an error page on the screen. 
In order to give the developers the best chance at fixing the bug, you should capture this error message window (and preferably highlight the error space) using Greenshot/SnippingTool/PrintScreen and save it as an image file (*.png/*.jpg/xxx).

Now, this is the bug scenario and you would need to report this as a BUG in JIRA or your bug-tracking tool (Azure DevOps/Trello/xxx).

A sample bug report:

Issue Type: Bug

Bug Title/Summary: Application crash on clicking the SAVE button while creating a new user.

Description: 
Steps To Reproduce:
1) Login into the application
2) Navigate to the Users Menu > New User
3) Filled all the user information fields
4) Clicked on the ‘Save’ button

Actual Result:
An error page is displayed. Refer attached screenshot for error details.

Expected Result:
On clicking SAVE button, should be prompted to a success message “New User has been created successfully”.

Attachment: Browse the error message that was saved as an image file.

Tips: 
1. Choose appropriate Severity and Priority for the bug. 
2. Including Browser version, Build version and any other relevant system information in the bug would be useful to reproduce it. 
3. Attaching logs (optional only) where necessary would be useful.
4. Be sure to provide information that might be useful for the developer, but don't fill the report with useless information that will slow the developer down while they explore the bug.

Read more about defect fields and their purpose here https://www.softwaretestinghelp.com/how-to-write-good-bug-report/.