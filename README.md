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
