# Visual Studio Code

## User Settings

Copy `settings.json` into the `User` directory which location depends on the OS platform.

- **Windows**: `%APPDATA%\Code\User\settings.json`
- **Linux**: `$HOME/.config/Code/User/settings.json`
- **MacOS**: `$HOME/Library/Application Support/Code/User/settings.json`

## Extensions

Search the following extensions in the Extension Marketplace with prefix `@id:`. For example, `@id:ms-python.python`. Note that there is no space after colon symbol `:`.

```
13xforever.language-x86-64-assembly
aaron-bond.better-comments
alefragnani.Bookmarks
CoenraadS.bracket-pair-colorizer
Equinusocio.vsc-community-material-theme
Equinusocio.vsc-material-theme
equinusocio.vsc-material-theme-icons
Gruntfuggly.todo-tree
mhutchie.git-graph
ms-toolsai.jupyter
ms-vscode.cpptools
ms-vscode.cpptools-extension-pack
PKief.material-icon-theme
shd101wyy.markdown-preview-enhanced
streetsidesoftware.code-spell-checker
tchayen.markdown-links
tomoki1207.pdf
torn4dom4n.latex-support
vscode-icons-team.vscode-icons
vscodevim.vim
zhuangtongfa.material-theme
```

### Show Installed Extensions

```sh
$ code --list-extensions
```

> MacOS must install `code` command before running it in the shell. Launch VSCode and open the Command Palette (`Shift+Cmd+P`). Type `Shell Command: Install 'code' command in PATH command` and hit Enter button. Restart the terminal and now we can run the command below to show installed extensions.
