# Whitespace

Sublime Text has options `trim_trailing_white_space_on_save` and `ensure_newline_at_eof_on_save` to handle whitespace.
In some situations, these options do not give satisfactory result. While similar packages exist, e.g., [TrailSpaces](https://github.com/SublimeText/TrailingSpaces), they do not allow easier syntax specific settings.
Whitespace helps in keeping your code clean by providing more features in removing trailing spaces.

- remove trailing whitespace
- ensure single trailing newline
- ignore whitespace only lines
- ignore whitespace on current line


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
    wait few seconds until the installation finishes up
1. Now,
    Go to the menu **`Preferences -> Package Control`**
1. Type **`Add Channel`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    input the following address and press <kbd>Enter</kbd>
    ```
    https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
    ```
1. Go to the menu **`Tools -> Command Palette...
    (Ctrl+Shift+P)`**
1. Type **`Preferences:
    Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    find the following setting on your **`Package Control.sublime-settings`** file:
    ```js
    "channels":
    [
        "https://packagecontrol.io/channel_v3.json",
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
    ],
    ```
1. And,
    change it to the following, i.e.,
    put the **`https://raw.githubusercontent...`** line as first:
    ```js
    "channels":
    [
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
        "https://packagecontrol.io/channel_v3.json",
    ],
    ```
    * The **`https://raw.githubusercontent...`** line must to be added before the **`https://packagecontrol.io...`** one, otherwise,
      you will not install this forked version of the package,
      but the original available on the Package Control default channel **`https://packagecontrol.io...`**
    > [!WARNING]
    > Placing this custom channel before the default channel changes Package Control's resolution globally.
    > Packages from this channel with the same name will override versions from the default channel.
    >
    > You can review the channel contents here:
    > https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
1. Now,
    go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    search for **`Whitespace`** and press <kbd>Enter</kbd>

See also:

1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


### Options
- The easiest way to apply "remove trailing whitespace" is by Command Palette `C+Shift+P`.

- To activate "remove trailing whitespace on save", click the menu items in `Edit -> Whitespace`.

- To enable Whitespace at startup, modify your preference setting file. If you want to enable Whitespace for a specific syntax,
edit `Preferences -> Settings - More -> Syntax Specific`:

```
{
    "remove_trailing_whitespace_on_save": true,
    "ensure_single_trailing_newline": true,
    "ignore_whitespace_only_lines": false,
    "ignore_whitespace_on_current_line": true
}
```

The options explain themselves. Their default values are `false`. You can also make use of [Syntax Manager](https://github.com/randy3k/SyntaxMgr) to enable Whitespace for multiple syntaxes.
