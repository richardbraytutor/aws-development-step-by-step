# FIRST GitHub account

## Account login / create

- run chrome

- create / signin to a GitHub desktop account

# New Repo : Created in VS Code

- use finder to create folder ~/github/`your-github-account-name`/repo-one
- put VS Code in the dock and drag the folder on top of it
- in Finder, look at the account icon in the bottom of the activity bar and sign out of any accounts - just to establish a reference point
- create a new file called README.md
- got to Source Control in Activity Bar
- Click on "Initialize Repository" or select View->CommandPalette->Git:Initialize Repository
- type "first commit" into the Message box and hit Commit
- press Publish Branch or select View->CommandPalette->Git:Publish Branch
- "The extension GitHub wants to sign in using GitHub" ... allow
- use the browser to authorize Visual Studio Code to access the GitHub account where you want to publish to repo
- you may be asked to sign in with your browser again ... just sign in to the same GitHub account
- go to github.com and you will see the repository there

# New Repo : Created on github.com website

- login to github.com and
- navigate your browser to www.github.com/`your-github-account-name`
- hit "+" button then "create a new repository"
- name = "repo-two"
- visibility = private
- run github desktop
- go to settings
- sign into GitHub.com as `your-github-account-name` using the browser
- run GitHub Desktop
- File->Clone Repository
- On the "Github.com" tab you should see repo-two - select it
- Clone it to ~/github/`your-github-account-name`/repo-two
- Select "Open in Visual Studio Code" button
- Add a README.md file
- got to Source Control in Activity Bar
- type "first commit" into the Message box
- in the dropdown choose Commit and Sync
- return to Github.com/`your-github-account-name`/repo-two and you should see the commit

# Switching to a SECOND GitHub Account

This is an **optional** section which shows how to switch to a second GitHub account if you have one.

## Create new Repo in second, different GitHub Account (VS Code Initiated)

- use finder to create folder ~/github/`A-DIFFERENT-account-name`/repo-three
- put VS Code in the dock and drag the folder on top of it

## Prepare for using another github account do the following

1. go to github.com and logout of all accounts
2. Clear the credential manager login

```bash
git credential-manager github list
```

- it should reply with something like `your-github-account-name`
- now ask Git Credential Manager to logout of that github account like this

```bash
git credential-manager github logout `your-github-account-name`
```

3. logout the github extension in vs code

- find the account icon in the activity bar and sign out of any github accounts `your-github-account-name`

## Publish the new repo to a new account

- create a new file called README.md
- got to Source Control in Activity Bar
- Click on "Initialize Repository" or select View->CommandPalette->Git:Initialize Repository
- type "first commit" into the Message box
- click on "Publish"
- use your browser to authentical login to `A-DIFFERENT-account-name`
