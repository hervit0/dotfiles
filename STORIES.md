## Funny stories

[The Vim disaster](https://github.com/VSCodeVim/Vim/issues/2322):

```
If you're in a hurry and can't wait for the fix : downgrade to vscode-vim 0.10.11

set "extensions.autoUpdate" to false in your user settings
uninstall vscode-vim 0.10.12
download vscode-vim 0.10.11 VSIX file : https://github.com/VSCodeVim/Vim/releases
in vscode, ctrl+shift+p > Install from VSIX > Choose vscode-vim 0.10.11 VSIX file
restart vscode
This worked for me.
```
