# Dotfiles

Classic with fries, please!

Jeez, why is it encrypted?! Well, every secret needs to hide `¯\_(ツ)_/¯`

## Encryption technologies

[Git-crypt](https://github.com/AGWA/git-crypt)

Cheat sheet:
```
git-crypt init
git-crypt status
git-crypt lock
git-crypt unlock
```

```
gpg --list-keys
gpg --list-secret-keys
```

## VSCode stuff

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

Copy extensions from local machine to this git repo (`vscode_extensions.json`):
```
./cp_vscode_extensions
```

Install extensions from this git repo (`vscode_extensions.json`) to local machine
```
./run_vscode_extensions
```

Useful config files:

- `keybindings.json`
- `settings.json`

## Bash stuff

Save `~/.bash_profile`: `./cp_bash_profile_driftrock`.
