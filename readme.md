# Ubuntu Linux

`sudo apt update`

`sudo apt list --upgradable`

`sudo apt update`

| Command          | Description          |
| ---------------- | -------------------- |
| Ctrl + W         | close window         |
| Super (Win) + D  | hide window          |
| Super + Space    | change input source  |
| Ctrl + Alt + T   | open terminal window |
| Ctrl + Shift + T | open terminal tab    |

PrintScreen - utility to make screen shots and record videos

PrintScreen + Ctrl - make quick screenshot (full page screenshot)

### Git

Visit [official website](https://git-scm.com/install/linux) to install the latest version of Git on Linux:

`sudo apt-get install git`

`sudo add-apt-repository ppa:git-core/ppa`

`sudo apt update; sudo apt install git`

### NVM

Visit [NVM Github page](https://github.com/nvm-sh/nvm) for install script:

`nvm install stable / latest / carbon / 18`

`nvm ls`

`nvm use stable / latest / carbon / 18`

### Software

Download .deb package from the [Google](https://www.google.com/chrome/?platform=linux), [VSCode](https://code.visualstudio.com/download) official websites and install them using dpkg:

`sudo dpkg -i path-to-deb-package.deb`

Install Chromium:

`sudo apt update; sudo apt install chromium-browser`

Install VLC player:

`sudo apt install vlc -y`

_Built-in screen recorder does not record sound; need to install Kazam or Vokoscreen_

### System Settings

Settings -> Appearence: AutoHide Dock + Bottom + Theme

Keyboard -> Add new input source + Change keyboard shortcut to change input source

# Git

`git config --local user.name itgrad07`

`git config --local user.email itgrad07@gmail.com`

Delete all local branches except:

`git branch | grep -v "develop" | xargs git branch -D`

Create alias for `git status`:

`git config --global alias.st status`

| Text                        | Description           |
| --------------------------- | --------------------- |
| git branch                  | show branches         |
| git branch -r               | show remote branches  |
| git branch -D branch        | delete local branch   |
| git cherry-pick commit-hash | delete local branch   |
| git reset --soft HEAD~N     | squash last N commits |

### SSH

Public SSH key is stored in .pub file in ~/.ssh folder:

`ssh-keygen`

`cat ~/.ssh/id_rsa.pub`

# VSCode

Set the following settings:

- format: onSave
- save: onFocusChange

Extensions:

- Prettier - Code formatter + edit settings.json
- ESLint (Microsoft)
- Live Server (Ritwick Dey)
- Simple React Snippets (Burke Holland)

Simple React Snippets:

- sfc (stateless functional component with default export)
- usf (declare a new state variable using State Hook)

Fonts:

_'Cascadia Code', 'Fira Code', Inconsolata, Consolas, 'Courier New', monospace_

**settings.json** should look like:

```
{
  "editor.formatOnSave": true,
  "files.autoSave": "onFocusChange",

  "editor.codeActionsOnSave": {
    // remove and reorder unused imports
    "source.organizeImports": true,
  },

  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
  },

  "git.autofetch": true,
}
```

# Other

#### VPN Chrome Extensions

Free VPN Proxy - VPNLY

windscribe
