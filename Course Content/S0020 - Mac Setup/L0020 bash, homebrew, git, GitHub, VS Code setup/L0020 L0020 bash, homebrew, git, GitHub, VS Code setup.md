# Setup .bash_profile

We need to distinguish .bash_profile from .bashrc

## .bash_profile

- Runs every time you open a new Terminal window
- Where you put things like
  - PATH
  - terminal prompt settings

## .bashrc

- Runs when you start a bash shell inside an existing terminal
- Where you typically put
  - aliases
  - functions

## Update .bash_profile

Edit the ~/.bash_profile file:
Open **Terminal**, then run:

```bash
nano ~/.bash_profile
```

and add

```bash
# In .bash_profile
export PS1="$ "
export BASH_SILENCE_DEPRECATION_WARNING=1
if [ -f ~/.bashrc ]; then
    source ~/.bashrc
fi

```

This does the following

- sets the terminal prompt to $ (we are going to use several split terminals and need the prompt small)
- removes unwanted messages when opening terminals
- loads .bashrc automatically whenever a new terminal is opened, thereby setting required aliases (we will be using some shortly)

# Install Homebrew

Open Terminal and run:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo >> /Users/richardbray/.bash_profile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/richardbray/.bash_profile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

# Install Git

```bash
brew install git
```

Verify:

```bash
git --version
```

# Install Git Credential Manager (GCM)

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

# Install GitHub Desktop

```bash
brew install --cask github
```

# Install Visual Studio Code

```bash
brew install --cask visual-studio-code
```

# VS Code : set default terminal

Run Visual Studio Code

Select View → Command Palette

Terminal: Select Default Profile

choose "bash"

# VS code : disable GPU acceleration in terminal

In the VS Code menu bar select "Code -> Settings"

Search for "features terminal gpu"

Under Terminal › Integrated: Gpu Acceleration

set to Off

# Workflow : first Github Account

## GitHub Desktop Signin

In GitHub Desktop settings, sign in with your GitHub account (this makes cloning super simple).

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

# Workflow : Second Github Account

This workflow shows how to switch to a second GitHub account, if needed.

## GitHub Desktop Signin to new, alternative GitHub account

In GitHub Desktop settings, sign in to your second GitHub account (this replaces the login to the first account).

## Clone a repo in GitHub Desktop

File → Clone Repository → pick one from the second GitHub account.

## Remove git credentials for the first GitHub account

- Open a terminal and enter this command:

```bash
git credential-manager github list
```

This will return the account you are git is configured to pull/push from.

Lets assume it returns

```
myaccount
```

- Clear these credentials with this command

```bash
git credential-manager github logout myaccount

```

## Attempt to push to the second GitHub account

Edit the cloned repo above with VS code and try to push the changes

it will re-prompt you to authenticate the new GitHub account you want to push to.

You can now continue to pull/push from repos in the second GitHub account.
