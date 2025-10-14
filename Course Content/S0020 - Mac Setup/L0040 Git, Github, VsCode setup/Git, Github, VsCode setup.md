# 1 Install Git

```bash
brew install git
```

Verify:

```bash
git --version
```

# 2 Install Git Credential Manager (GCM)

```bash
brew install --cask git-credential-manager
git-credential-manager configure
```

Check it’s configured:

```bash
git config --global credential.helper
```

It should say:

manager

# 3 Install GitHub Desktop

```bash
brew install --cask github
```

Open GitHub Desktop.

Sign in with your GitHub account (this makes cloning super simple).

# 4 Install Visual Studio Code

```bash
brew install --cask visual-studio-code
```

# 5 First-time test workflow

## Clone a repo in GitHub Desktop:

File → Clone Repository → pick one from your GitHub account.

It saves locally on your Mac.

## Open in VS Code:

In GitHub Desktop → Right-click the repo → “Open in Visual Studio Code.”

## Make a change in VS Code:

Edit a file and save it.

## Commit in VS Code:

Open the Source Control panel (Ctrl+Shift+G or sidebar icon).

Enter a commit message → Click ✅ Commit.

## Push in VS Code:

Click the “Sync Changes” / “Push” button in the Source Control panel.

On first push, Git Credential Manager will launch a browser window.

Log in to GitHub → approve access.

Your token is securely stored in the macOS Keychain (local, not iCloud).

## Verify push succeeded:

Refresh your repo on GitHub.com and check your change is there.

# 6 If, at some time in the future you want to work with a different GitHub account :

- In GitHub desktop, sign in to the new GitHub account in "settings"

- Clone a repo from the new account

- Open a terminal and enter this command:

```bash
git credential-manager github list
```

This will return the account you are git is configured to pull/push from.

lets assume it returns

```
myaccount
```

- Clear these credentials with this command

```bash
git credential-manager github logout myaccount

```

- Edit the cloned repo above with VS code and try to push the changes

it will re-prompt you to authenticate the new GitHub account you want to push to.
