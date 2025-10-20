# Git : Working with multiple accounts simultanously

## Don't use GitHub Desktop

GitHub desktop doesn't support connecting to multiple GitHub accounts simultaneoulsy so we won't use it.

## Enable Multiple account support in git

Open a terminal and enter this command

```bash
git config --global credential.https://github.com.useHttpPath true
```

This command is essential for multi-account support.

# Repo in First Account

## Get HTTPS URL of the first repo you want to clone

First visit the github website, signin if necessary (for private repos) and locate the repo you require.

Find the URL on the github website using the green Clone button and select the HTTPS URL and copy it, eg

https://github.com/rjbtutor/000-Course-Planning.git

## Clone the repo using an **adjusted URL**

Open a terminal in the folder where you want to clone the repo.

Issue a git clone command in the terminal but change github.com to youraccount@github.com like this

```bash
git clone https://rjbtutor@github.com/rjbtutor/000-Course-Planning.git
```

## Use the first repo from within VS Code

you can now make changes and push those changes from within VS Code

# Repo in Second Account

## Get HTTPS URL of the first repo you want to clone

First visit the github website for the second repo, signin if necessary (for private repos) and locate the repo you require.

Again, find the URL on the github website using the green Clone button and select the HTTPS URL and copy it, eg

https://github.com/rjbtutor/000-Course-Planning.git

## Clone the repo using an **adjusted URL**

Open a terminal in the folder where you want to clone the repo.

Issue a git clone command in the terminal but change github.com to youraccount@github.com like this

```bash
git clone https://rjbtutor@github.com/rjbtutor/000-Course-Planning.git
```

## Use the second repo from within VS Code

you can now make changes and push those changes from within VS Code

# Retest pushing the first repo from VS Code

Reopen the first repo in VS Code, make another change and push : it should all work.
