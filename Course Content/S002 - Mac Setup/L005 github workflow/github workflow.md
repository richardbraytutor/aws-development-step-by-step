# GitHub website

- run chrome

- create and signin to a GitHub desktop account

# New Repo : VS Code Initiated

- use finder to create folder ~/<github-account-name>/repo-one
- put VS Code in the dock and drag the folder on top of it
- got to Source Control in Activity Bar

# Create a new repo and save it to GitHub

## Create new folder and file

- Open application terminal

```bash
cd ~
mkdir repo-one
cd repo-one
git init -b main -q
touch README.md
```

### Create Repo with GitHub Desktop

- Open GitHub desktop
- File->AddLocalRepository (to Add an Existing Repository from your Local Drive)
- choose the "repo-one" folder and hit "Add Repository"

### Clone a repo in GitHub Desktop:

File → Clone Repository → pick one from your GitHub account.

It saves locally on your Mac.

### Open in VS Code:

In GitHub Desktop → Right-click the repo → “Open in Visual Studio Code.”

### Make a change in VS Code:

Edit a file and save it.

### Commit in VS Code:

Open the Source Control panel (Ctrl+Shift+G or sidebar icon).

Enter a commit message → Click ✅ Commit.

### Push in VS Code:

Click the “Sync Changes” / “Push” button in the Source Control panel.

On first push, Git Credential Manager will launch a browser window.

Log in to GitHub → approve access.

Your token is securely stored in the macOS Keychain (local, not iCloud).

### Verify push succeeded:

Refresh your repo on GitHub.com and check your change is there.

## Switch to second Github Account

This workflow shows how to switch to a second GitHub account, if needed.

### GitHub Desktop Signin to new, alternative GitHub account

In GitHub Desktop settings, sign in to your second GitHub account (this replaces the login to the first account).

### Clone a repo in GitHub Desktop

File → Clone Repository → pick one from the second GitHub account.

### Remove git credentials for the first GitHub account

- Open a terminal and enter this command:

```bash
git credential-manager github list
```

This will return the account you are git is configured to pull/push from.

Lets assume it returns

```
rjbtutor
```

- Clear these credentials with this command

```bash
git credential-manager github logout rjbtutor

```

### Attempt to push to the second GitHub account

Edit the cloned repo above with VS code and try to push the changes

it will re-prompt you to authenticate the new GitHub account you want to push to.

You can now continue to pull/push from repos in the second GitHub account.
