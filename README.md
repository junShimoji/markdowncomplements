# Markdown complements
Easy indenting of Markdown lists.

* This plugin provides functions to complement a markdown list item making/changing or indent up/down.
* Need to set Key Bindings only.
* No need to care extensions(.md,.mdown,.txt or something like that).
* Can change list items manually not connected with indent levels.
* Can prevent conflicting with Japanese Input method that selected characters are disappearing.

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

There are 5 plug-ins.

1. markdown_indent_down

If the focus line has a list item(\*,+ or -), then you can indent down.
If the focus line has no list item(\*,+ or -), you can add a list item automatically.

2. markdown_indent_up

If the line has a list item(\*,+ or -), it indent up.

3. markdown_new_line

It provides new line with a list item.

4. markdown_rotate_list_item

If a list item(\*,+ or -) exists, the list item lotates like \* -> + -> - * ....

Use as follows.

Open Preferences > Key Bindings and add as follows:

    { 
        "keys": ["ctrl+enter"], "command": "markdown_indent_down",
        "context": [{ "key": "selector", "operator": "equal", "operand": "text.html.markdown" }]
    },
    { "keys": ["ctrl+shift+enter"], "command": "markdown_indent_up" },
    { "keys": ["command+enter"], "command": "markdown_new_line" },
    { "keys": ["shift+enter"], "command": "markdown_rotate_list_item" }

Above "context" should be added if neceesary.

5. outline to table

It provides outline to markdown table.

* To make table header, use list item ```+```.
* To make table contents, use list item ```-```.
* Select texts which include headers and contents.
* Open palette and input 'outline to table.'

#### example

before)

```
+ header1
    + header2
        + header3

- content1
    - content2
- content3
    - content4
```

after)

```
|header1|header2|header3|
|-|-|-|
|content1|content2|
|content3|content4|
```