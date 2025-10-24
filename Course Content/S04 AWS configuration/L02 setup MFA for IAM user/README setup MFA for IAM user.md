# login as new IAM user

- go to the AWS login screen (you can find this using Google - search for "AWS sign in")
- Account alias - as chosen previous lesson - eg "awsstepbystep-xxx"
- IAM username = dev
- password = as per previous lesson

# setup MFA with an Authenticator

if you haven't already installed an authenticator on your phone install one ... 

At the time of writing I use both Google and Microsoft authenticators - I find Microsoft slightly more polished but they both work fine. 

- open the IAM service
- select (in the Access Management section) Users
- click on "dev"
- Select the "security credentials" tabbed section
- press "Assign MFA device" button
- select a name eg. awsstepbystep-dev-auth
- select Authenticator app
- the authenticator will provide a new number every 30 seconds ... type two successive numbers into the MFA 1 and MFA 2 boxes

# logout and log back in again

- click on the username at the top right "dev" 
- press the signout button
- login again - you will be prompted for an MFA code from your authenticator

# setup MFA with a passkey

This assumes you are on your personal machine 

It also assumes that you are using a browser such as Chrome with a profile setup for you personally

This way, the passkey will be stored by chrome in the password manager for your profile

- open the IAM service
- select (in the Access Management section) Users
- click on "dev"
- Select the "security credentials" tabbed section
- press "Assign MFA device" button
- select a name e.g awsstepbystep-dev-passkey
- select Passkey
- use default passkey name = true

at this point chrome should jump in and ask you to confirm the passkey creation

- hit next

the passkey will now be saved

# logout and log back in again

- click on the username at the top right "dev" 
- press the signout button
- login again - this time you should be able to use a passkey





