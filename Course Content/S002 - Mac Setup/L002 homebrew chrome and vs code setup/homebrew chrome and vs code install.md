# Install Homebrew

Open Terminal and run:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo >> /Users/richardbray/.bash_profile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/richardbray/.bash_profile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

# Install Google Chrome

```bash
brew install --cask google-chrome
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
