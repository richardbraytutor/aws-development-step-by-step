# Install Git

```bash
brew install git
```

Verify:

```bash
git --version
```

# Install Git Credential Manager (GCM)

We are going to be using three similar terms frequently :

- git - which is a command line application (CLI) installed on your local machine and can be used to manage "source code repositories" or "repos" both local and remote

- github - which is a website for storing repositories

- github desktop - which is a desktop application with a UI which can be used as an alternative to the git CLI

Visual Studio code uses **git** under the hood for source code management.

In order to be able to push to GitHub repos, we need to configure git security correctly.

git can communicate with its remote host using two protocols

- ssh
- https

The github website supports both of these.

However, the GitHub desktop application only uses **https** to communicate with the GitHub website.

We are therefore going to configure git to use **https** as well.

When your local git talks to the github server **via https** it uses the git credential manager to manage the security, so we will install that next.

Once we have done that both of these applications will be able to talk to GitHub

- git
- visual studio code

(Note that GitHub desktop does not use git credentials and its security is managed completely independently)

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
