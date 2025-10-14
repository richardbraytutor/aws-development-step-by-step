## 3. Create a GitHub account if you don't already have one - use Passkey for easy login

- go to settings, password and authentication, add a passkey

## 4. Install and Configure Git and GitHub Desktop

Note that --cask means its a UI application

```bash
brew install git
brew install --cask github
```

### set git global defaults

Set your **Personal identity** as the global default:

```bash
git config --global user.name "personal"
git config --global user.email "personal@gmail.com"
git config --global init.defaultBranch main
git config --global core.editor "code --wait"
```

### Generate SSH Keys for Each Account

```bash
# personal account
ssh-keygen -t ed25519 -C "personal@gmail.com" -f ~/.ssh/id_ed25519_personal
```

This creates a key pair:

- `~/.ssh/id_ed25519_personal`
- `~/.ssh/id_ed25519_personal.pub`

### Configure SSH

Edit your SSH config file:

```bash
nano ~/.ssh/config
```

Paste in the following:

```ssh-config
# Personal GitHub
Host github.com-personal
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_personal
  IdentitiesOnly yes
```

Save and exit.

### Add Public Keys to GitHub

Copy the public key into the cut/paste buffer:

```bash
pbcopy < ~/.ssh/id_ed25519_personal.pub   # personal
```

Then paste it into the GitHub online correct account at:  
**GitHub → Settings → SSH and GPG keys → New SSH key**

### Test Connections

```bash
ssh -T git@github.com-personal
```

You should see:

```
Hi <username>! You've successfully authenticated, but GitHub does not provide shell access.
```

### Daily CoursePublicationflow Example

```bash
# Clone repo with correct alias
git clone git@github.com-personal:company/example-repo.git
cd example-repo
code .

# Create feature branch
git checkout -b feature/my-change

# Make edits in VS Code, then commit
git add -A
git commit -m "Add new feature"

# Push branch
git push -u origin feature/my-change
```

## 5. Install and Configure VS Code

Note that --cask means its a UI application

```bash
brew install --cask visual-studio-code
```

### Add VS Code to PATH

1. Open VS Code
2. Press `Cmd+Shift+P`
3. Type **Shell Command**
4. Select **Install 'code' command in PATH**
5. Restart Terminal → now you can run `code .`

### Run VS Code and add extensions

## docker desktop (with buildx)

## aws cli

## cdk cli

## pnpm

## npm

## jq

## psql (pgadmin)

## flyway

## cygpath (install on windows only)

```

```
