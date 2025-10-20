# Install Extensions as required

```bash
#!/bin/bash

# Write the extensions into the file
cat > extensions-list.txt <<EOL
albert.tabout
bradlc.vscode-tailwindcss
christian-kohler.path-intellisense
dbaeumer.vscode-eslint
dsznajder.es7-react-js-snippets
esbenp.prettier-vscode
formulahendry.auto-rename-tag
inferrinizzard.prettier-sql-vscode
mhutchie.git-graph
ms-vscode-remote.remote-wsl
ms-vscode.vscode-typescript-next
peakchen90.open-html-in-browser
redhat.vscode-yaml
ritwickdey.liveserver
vincaslt.highlight-matching-tag
yoavbls.pretty-ts-errors
EOL

# Install all extensions listed
cat extensions-list.txt | xargs -L 1 code --install-extension
```
