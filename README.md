# synthwave-x-fluoromachine
This is a fork of a fork of @robbowen's [Synthwave '84 theme](https://marketplace.visualstudio.com/items?itemName=RobbOwen.synthwave-vscode), merged with @fullerenedream's [Fluoromachine](https://colorsublime.github.io/themes/FluoroMachine/) theme, and these additional tweaks:

* Debugging squiggles not quite popping out enough:

```
"editorError.foreground": "#fc199a",
"editorWarning.foreground": "#fc199a",
```

* Inadequate selection highlighting :

```
"editor.selectionBackground": "#ffaa007a",
```

![Theme screenshot](https://repository-images.githubusercontent.com/184457193/69dcff00-14d2-11ea-90e1-4bdf6fef80ca)

## Installation

1. Install Synthwave ’84/[Synthwave + Fluoromachine](https://marketplace.visualstudio.com/items?itemName=webrender.synthwave-x-fluoromachine) theme on VS Code

2. Install [Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css)

3. Command + Shift + P to open command palette > "Preferences: Open settings (JSON)"

4. Add to the settings object this key, and the value is an array containing the path to the CSS file for your extension. On a Mac it should be the following:

```
{
    "vscode_custom_css.imports": [
    "file:///Users/${username}/.vscode/extensions/${extension folder name}/${extensions css file name}.css"
    ]
}
```

On Linux, the home directory is `/home` instead of `/Users`.

Windows:

```
{
  "vscode_custom_css.imports": [
    "file:///C:/Users/{your username}/.vscode/extensions/webrender.synthwave-x-fluoromachine-0.0.12/synthwave-x-fluoromachine.css"
    ]
}
```


5. Quit VS Code and go to terminal so we can restart it with proper Permissions
6. Type `sudo chown -R $(whoami) PATH TO CODE` where PATH TO CODE is actually the file path, and you actually type `${whoami}` as well. On Linux, the command is `sudo chown -R $(whoami) /usr/share/code`.

So I typed exactly:

`sudo chown -R $(whoami) /Applications/Visual\ Studio\ Code.app/Contents/MacOS/Electron` - the back slashes in front of the space are important

6a. According to Custom CSS and JS Loader, if you are using 'Insiders Branch' then the VS Code file path might be: `/Applications/Visual Studio Code - Insiders.app/Contents/MacOS/Electron` but idk what that means

7. Should prompt you for your password

8. Reopen VS Code

9. Command + Shift + P > "Reload Custom CSS and JS"

10. Restart VS Code one more time and hopefully you'll see the glow!

## Notes to keep in mind:

* SPECIAL NOTE: If Code complains about that it is corrupted, simply click “Don't show again”.
* NOTE: Every time after Code is updated, please repeat step 6 and re-enable Custom CSS.
* NOTE: Every time you change the configuration, please re-enable Custom CSS.
