# Markdown complements

* This plugin provides functions to complement markdown a list item making/changing or indent up/down.
* No need to care extensions(.md,.mdown,.txt or like that).

![gif](https://immense-headland-55656.herokuapp.com/markdownComplements.gif)

## Sublime Text Version

The plugin requires Sublime Text 3.

## Installation

You can clone this repository into your Sublime Text "Packages" folder.

### MacOS: 

    cd ~/"Library/Application Support/Sublime Text 3/Packages"
    git clone https://github.com/junShimoji/markdowncomplements.git MarkDownComplements

### Windows:

    cd "%APPDATA%\"Sublime Text 3\Packages"
    git clone https://github.com/junShimoji/markdowncomplements.git MarkDownComplements

### Settings

There are 4 plug-ins.

#### markdown_indent_down

If the focus line has a list item(\*,+ or -), then you can indent down.
If the focus line has no list item(\*,+ or -), you can add a list item automatically.

#### markdown_indent_up

If the line has a list item(\*,+ or -), it indent up.

#### markdown_new_line

It provides new line with a list item.

#### markdown_rotate_list_item

If a list item(\*,+ or -) exists, the list item lotates like \* -> + -> - * ....

Use as follows.

Open Preferences > Key Bindings and add as follows

    { "keys": ["ctrl+enter"], "command": "markdown_indent_down" },
    { "keys": ["ctrl+shift+enter"], "command": "markdown_indent_up" },
    { "keys": ["command+enter"], "command": "markdown_new_line" },
    { "keys": ["shift+enter"], "command": "markdown_rotate_list_item" }


