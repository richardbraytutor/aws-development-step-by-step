# Setup

These are the setup instructions if you are working on a Mac.

The windows instructions are in another section.

I am starting with a Mac which has been fully reset.

The only changes I have made are:

- cosmetic : wallpaper, dock, finder
- video recording software + backup

# Terminal setup

- run mac terminal application

- in the menu bar select Terminal → settings

- Set "shells open with" to Command (complete path) and set this to

```
/bin/bash
```

- you may wish to change the display settings, I am going to use
  - profile = homebrew
  - profiles-homebrew-font-size:18

# Change the default terminal to bash

Open a new terminal window and issue the following command

```bash
chsh -s /bin/bash
```

( To revert to the zsh just issue the command, but we will be assuming the bash shell for this course setup. )

```bash
chsh -s /bin/zsh
```

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

Edit the ~/.bash_profile file

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
