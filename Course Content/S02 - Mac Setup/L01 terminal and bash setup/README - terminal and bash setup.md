# Setup

There are separate sections for Mac and Windows setup.

These are the only sections in the course which differ : once this setup is complete, the remainder of the course videos should work on both platforms.

This the Mac setup section.

In this section we start with a factory reset machine and we'll install all the tools necessary  prior to starting development.

The only changes made to this machine are

- cosmetic : wallpaper, dock, finder
- video recording software + backup

# Mac / Windows compatibility

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
  - profiles-homebrew-font-size:14





# Change the default terminal to bash

Open a new terminal window and issue the following command

```bash
chsh -s /bin/bash
```

( To revert to the zsh just issue the command, but we will be assuming the bash shell for this course setup. )

```bash
chsh -s /bin/zsh
```


## .bash_profile

- Runs every time you open a new Terminal window
- Where you put things like
  - PATH
  - terminal prompt settings


Open **Terminal**, then run:

```bash
nano ~/.bash_profile
```

and add

```bash
export PS1="$ "
export BASH_SILENCE_DEPRECATION_WARNING=1

```

This does the following

- sets the terminal prompt to $ (we are going to use several split terminals and need the prompt small)
- removes unwanted messages when opening terminals

Open a new terminal window to see the results.

## .bashrc

- We won't be using it
