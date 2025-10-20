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

# Install Extensions as required

```
cat extensions-list.txt | xargs -L 1 code --install-extension
```
