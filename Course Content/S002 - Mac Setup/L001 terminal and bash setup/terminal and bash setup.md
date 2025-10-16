# Setup

My aim is for this course to provide complete instructions on how to develop a substantial AWS project from scratch, with nothing missing.

For that reason we are starting with a factory reset machine.

The only changes I have made are:

- cosmetic : wallpaper, dock, finder
- video recording software + backup

# Mac / Windows compatibility

There are separate sections for Mac and Windows setup.

You are currently in the Mac setup section.

These are the only sections in the course which differ : once this setup is complete, the remainder of the course videos should work on both platforms.

If there are any differences I will point them out as we go along and show you what to do on each platform.

In order to maintain this compatibility I am going to assume that we are using the same terminal shell on both platforms.

We will therefore be using the bash shell thoughout the course.

A Mac, by default, is configured to use zsh, so the first thing we are going to do is change this to the bash shell.

Don't worry : I will point out how it can be changed back !

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
