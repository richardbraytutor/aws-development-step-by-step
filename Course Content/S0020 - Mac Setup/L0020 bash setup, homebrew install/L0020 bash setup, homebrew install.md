# Setup .bash_profile

## .bash_profile

- is where you put things like your PATH

- It runs every time you open a new Terminal window

## .bashrc

- is where you typically put aliases and functions

- it runs when you start a bash shell inside an existing terminal

## Update .bash_profile

Edit the ~/.bash_profile file:
Open **Terminal**, then run:

```bash
nano ~/.bash_profile
```

and add the following

```bash
# In .bash_profile
export PS1="$ "
export BASH_SILENCE_DEPRECATION_WARNING=1
if [ -f ~/.bashrc ]; then
    source ~/.bashrc
fi

```

By adding this code to .bash_profile, you're telling it to also load .bashrc automatically whenever a new terminal is opened.

- this way, you can organize your settings
- keep PATH and environment variables in .bash_profile, and
- keep aliases and shortcuts in .bashrc
- and everything will load together when you open Terminal.

# Install Homebrew

Open Terminal and run:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo >> /Users/richardbray/.bash_profile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/richardbray/.bash_profile
eval "$(/opt/homebrew/bin/brew shellenv)"
```
