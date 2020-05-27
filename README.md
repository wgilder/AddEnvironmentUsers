# AddEnvironmentUsers
Allows a UiPath Process Mining super admin to add multiple users to a particular environment

# Requirements
* Attended Automation
* Built using UiPath Studio 20.4.1
* Performs operations using Internet Explorer
* Uses Microsoft Excel
* Optionally sends emails via local Outlook account

## Usage
* Click "Run"
* Enter server details (input screen)
  * Enter the URL of the server hosting the Bootcamp, plus the credentials for the super admin user. 
* Select Excel new-users Excel sheet
  * Excel sheet is expected to have a header row, plus at least a column with the individual users' names and emails
* Specify creation details
  * Specify the column (by name) in the Excel containing the users' common name and email address.
  * Specify the environment in which to create the users. The list of environments is determined by querying the PM server
  * Specify how the password needs to be handled. The options are a) to replace the temporary password with a permanent one, sending the user the result; b) have the system generate an email informing the user of the temporary generated password; or c) do nothing
  * (Optional) Enter the Subject and Body of the email, and whether it's HTML-based or not. The body replaces three placeholds: {url} the URL of the server; {username} the name the user needs to log into their account on the server; and {password}, the password for the account.
* Robot then creates the indicated users in the environment specified.

## Note: 
Individual modules are not currently activated or deactivated following user creation. This shouldn't be a problem for single-module installations, though for multiple-module ones, a super-admin may need to manually activate or deactivate users.
