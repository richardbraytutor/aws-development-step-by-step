# login as new IAM user
- run chrome - we are going to save passkeys later on in the chrome password manager

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

# select a chrome profile
- click "your chrome" at top right of browser
- select "sign in to chrome"
- choose either your personal google account if you have one or the gmail account you used to setup the aws account with
- sign in

This way, the passkey will be stored by chrome in the password manager for your profile

# setup MFA with a passkey

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





