# Local Dev Environment Setup <!-- omit in toc -->

- [Mac Fix Home \& End Keys](#mac-fix-home--end-keys)
- [Setup VS Code](#setup-vs-code)
  - [Vs Code Extensions](#vs-code-extensions)
  - [Vs Code Settings](#vs-code-settings)
- [Windows Terminal](#windows-terminal)
  - [Add Git Bash to Windows Terminal](#add-git-bash-to-windows-terminal)
  - [Install Ubuntu Server or Debian Using WSL](#install-ubuntu-server-or-debian-using-wsl)
  - [Add Brogrammer Color Theme](#add-brogrammer-color-theme)
- [Mac Terminal](#mac-terminal)
  - [Add Brogrammer Color Theme](#add-brogrammer-color-theme-1)
- [Install Oh My Zsh](#install-oh-my-zsh)
  - [Install for Git Bash](#install-for-git-bash)
  - [Install for Linux/Mac](#install-for-linuxmac)
- [Fix Zsh Autocomplete](#fix-zsh-autocomplete)
- [Install Powerlevel10k Plugin](#install-powerlevel10k-plugin)

## Mac Fix Home & End Keys

1. Navigate to `~/Library` and creat a new folder called `KeyBindings`.
2. Navigate into the `~/Library/KeyBindings` folder and create a new file called `DefaultKeyBinding.dict`.
3. Add the following commands to that file:

   ```txt
   {
   /* Remap Home / End keys */
   /* Home Button*/
   "\UF729" = "moveToBeginningOfLine:";
   /* End Button */
   "\UF72B" = "moveToEndOfLine:";
   /* Shift + Home Button */
   "$\UF729" = "moveToBeginningOfLineAndModifySelection:";
   /* Shift + End Button */
   "$\UF72B" = "moveToEndOfLineAndModifySelection:";
   /* Ctrl + Home Button */
   "^\UF729" = "moveToBeginningOfDocument:";
   /* Ctrl + End Button */
   "^\UF72B" = "moveToEndOfDocument:";
    /* Shift + Ctrl + Home Button */
   "$^\UF729" = "moveToBeginningOfDocumentAndModifySelection:";
   /* Shift + Ctrl + End Button*/
   "$^\UF72B" = "moveToEndOfDocumentAndModifySelection:";
   }
   ```

4. Save the file and restart your mac. The home and end keys should now work as expected.

## Setup VS Code

### Vs Code Extensions

- Code Spell Checker
- C#
- ESLint
- Git Graph
- GitHub Pull Requests and Issues
- GitLens
- Jest
- Live Server (Microsoft)
- Live Share Extension Pack (Microsoft)
- Markdown All in One
- Markdown Preview Github Styling
- markdownlint
- open in browser
- Prettier
- Sonarlint
- Stylelint
- TODO Highlight
- WSL (Microsoft)
- YAML

### Vs Code Settings

```json
{
  "workbench.startupEditor": "newUntitledFile",
  "css.lint.unknownAtRules": "ignore",
  "editor.accessibilitySupport": "off",
  "editor.fontSize": 13,
  "editor.formatOnSave": true,
  "editor.guides.bracketPairs": true,
  "editor.quickSuggestionsDelay": 500,
  "editor.tabSize": 2,
  "editor.renderWhitespace": "boundary",
  "editor.rulers": [80, 100],
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "files.insertFinalNewline": true,
  "files.trimFinalNewlines": true,
  "files.trimTrailingWhitespace": true,
  "files.eol": "\n",
  "html.autoCreateQuotes": false,
  "diffEditor.renderSideBySide": true,
  "diffEditor.ignoreTrimWhitespace": false,
  "terminal.integrated.defaultProfile.windows": "Git Bash",
  "terminal.integrated.fontFamily": "MesloLGS NF",
  "git.autofetch": true,
  "gitlens.gitCommands.closeOnFocusOut": true,
  "gitlens.gitCommands.skipConfirmations": ["fetch:command", "switch:command"],
  "gitlens.menus": {
    "editor": {
      "blame": false,
      "clipboard": true,
      "compare": true,
      "details": false,
      "history": false,
      "remote": false
    },
    "editorGroup": false,
    "editorTab": false,
    "explorer": {
      "clipboard": true,
      "compare": true,
      "history": true,
      "remote": true
    },
    "scmGroup": {
      "compare": true,
      "openClose": true,
      "stash": true,
      "stashInline": true
    },
    "scmItem": {
      "clipboard": true,
      "compare": true,
      "history": true,
      "remote": true,
      "stash": true
    }
  },
  "security.workspace.trust.untrustedFiles": "open"
}
```

## Windows Terminal

### Add Git Bash to Windows Terminal

1. Open Windows Terminal. From the drop down menu (look for the `˅` symbol nex to the tabs) select `Settings`
2. In the left menu under Profiles select `Add new`
3. In the `name` field enter `Git Bash`
4. In the `Command line` field enter `C:\Program Files\Git\bin\bash.exe`
5. In the `Icon` field enter `C:\Program Files\Git\mingw64\share\git\git-for-windows.ico`
6. Click `Save`
7. In the left menu at the top select `Startup`
8. Update the `Default profile` field to `Git Bash`
9. In the left menu at the bottom select `Open JSON File`
10. Find the `Profile.list` array and change the ordering to your preference

### Install Ubuntu Server or Debian Using WSL

1. Follow instructions found here: <https://learn.microsoft.com/en-us/windows/wsl/install>
2. Once installed the following installation commands may need to be executed:

   ```bash
   sudo apt update
   sudo apt upgrade
   sudo apt install vim curl git
   ```

3. It may also be useful to add a windows home directory alias by executing a command simliar to this one:

   ```bash
   alias winhome="cd /mnt/c/Users/Samuel"
   ```

### Add Brogrammer Color Theme

1. Open Windows Terminal. From the drop down menu (look for the `˅` symbol nex to the tabs) select `Settings`
2. In the left menu at the bottom select `Open JSON File`
3. Find the `schemes` array and add the following object:

   ```json
   {
     "name": "Brogrammer",

     "cursorColor": "#B9B9B9",
     "selectionBackground": "#45A2D2",

     "background": "#131313",
     "foreground": "#D6DBE5",

     "black": "#1F1F1F",
     "blue": "#2A84D2",
     "cyan": "#1081D6",
     "green": "#2DC55E",
     "purple": "#4E5AB7",
     "red": "#F81118",
     "white": "#D6DBE5",
     "yellow": "#ECBA0F",
     "brightBlack": "#D6DBE5",
     "brightBlue": "#1081D6",
     "brightCyan": "#0F7DDB",
     "brightGreen": "#1DD361",
     "brightPurple": "#5350B9",
     "brightRed": "#DE352E",
     "brightWhite": "#FFFFFF",
     "brightYellow": "#F3BD09"
   }
   ```

4. Find the `Profiles.list array` and add the following properties to the profile objects that you wan the `Borgrammer` theme applied to:

   ```json
   "colorScheme" : "Brogrammer"
   "cursorShape" : "filledBox"
   ```

   The profile should look similar to this:

   ```json
   {
     "colorScheme": "Brogrammer",
     "cursorShape": "filledBox",
     "commandline": "C:\\Program Files\\Git\\bin\\bash.exe",
     "guid": "{575851b6-d773-46a1-9a47-6ef3249e1942}",
     "hidden": false,
     "icon": "C:\\Program Files\\Git\\mingw64\\share\\git\\git-for-windows.ico",
     "name": "Git Bash"
   },
   ```

## Mac Terminal

### Add Brogrammer Color Theme

1. Go to _Apple Terminal → Preferences → Profiles → Gear Icon → Import_. Import the file located at [./brogrammer.terminal](./brogrammer.terminal)
2. Update the selection color for the profile to #45A2D2

## Install Oh My Zsh

### Install for Git Bash

1. Download the latest MSYS2 zsh package from the MSYS2 package repository https://packages.msys2.org/package/zsh?repo=msys&variant=x86_64. The file will be named something along the lines of `zsh-5.8-5-x86_64.pkg.tar.zst`
2. Extract the contents of the archive (which should include etc and usr folders) into your Git Bash installation directory. This is likely to be under `C:\Program Files\Git`. Merge the contents of the folder if asked (no files should be getting overridden).
3. In Git Bash run the follow to verify the installation:

   ```bash
   zsh --version
   ```

4. Configure Zsh as the default shell by appending the following to your `~/.bashrc` file:

   ```bash
   if [ -t 1 ]; then
     exec zsh
   fi
   ```

### Install for Linux/Mac

Follow this guide: <https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#how-to-install-zsh-on-many-platforms>

## Fix Zsh Autocomplete

By default, Zsh "Tab Completion" may be case sensitive. Open your `~/.zshrc` file in an editor and add the following lines:

```bash
autoload -Uz compinit && compinit
zstyle ':completion:*' matcher-list 'm:{a-z}={A-Za-z}'
```

This tells Zsh that small letters will match small and capital letters. (i.e. capital letters match only capital letters.)

## Install Powerlevel10k Plugin

**TODO: does this guide still checkout?**

Follow the guide at <https://github.com/romkatv/powerlevel10k>

> ⚠️ NOTE: Read instructions in the above guide all the way through for each step. It is easy to skip the updating of the terminal's profile font, and setting ZSH_THEME="powerlevel10k/powerlevel10k" in `~/.zshrc`.
>
> ⚠️ NOTE: For Windows Terminal go to settings -> { profile } -> Appearance and change the the font face to the the powerlevel10k instructions said to download.

When running the Powerlevel10k config use the following styles:

```txt
Prompt Style = Rainbow
Character Set = Unicode
Show Current Time = 12-hour format
Prompt Separators = Angled
Prompt Heads = Sharp
Prompt Tail = Flat
Prompt Height = Two lines
Prompt Connection = Dotted
Prompt Frame = No frame
Connection Color = Lightest
Prompt Spacing = Sparse
Icons = Many Icons
Prompt Flow = Concise
Enable Transient Prompt = No
Instant Prompt Mode = Verbose
```
