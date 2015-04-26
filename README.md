Sublime Text 3 Configuration
============================

Polycademy's preferred Sublime Configuration.

Theme
-----

Place Notepad++.tmTheme into the Packages location. This can be accessed via `Preferences -> Browse Packages`

Actually I've changed:

1. For day time - iPlastic
2. For night time - Cobalt

Font
----

Acquire the Source Code Pro font and install it into your computer: (https://github.com/adobe-fonts/source-code-pro)

Acquire the Anonymous Pro font and install it into your computer: (http://www.marksimonson.com/fonts/view/anonymous-pro)

Anonymous Pro Font is better.

Packages
--------

Install Sublime Text 3 Package Control (https://sublime.wbond.net/installation)

Hit `Ctrl + Shift + P` and use Package Control to install these packages:

```
BracketHighlighter  
DocBlockr
Emmet
Phoenix Theme  
SublimeLinter3
Floobits
MarkdownEditing
SublimeTableEditor
Open-Url
GitSavvy
SublimeREPL
```

### Language/Framework Specific Packages

```
Nginx
Elm
Elixir
GoSublime
LESS  
AngularJS
Nix
Rust
Toml
```

Settings
--------

Copy paste the contents of Preferences.sublime-settings into your user settings. This can be accessed via `Preferences -> Settings - User`

Client Side Template Syntax Highlighting
----------------------------------------

Sublime Text Editor does not normally highlight the syntax of HTML that inside client side template script tags. For example AngularJS and Handlebars.

In order to make Sublime run syntax highlighting, first find the HTML.sublime-package zip archive. This is usually located where Sublime was installed. Copy this archive somewhere else and unzip. Open up HTML.tmLanguage file. On line 286 change:

```xml
<string>(?:^\s+)?(&lt;)((?i:script))\b(?![^&gt;]*/&gt;)</string>
```

into

```xml
<string>(?:^\s+)?(&lt;)((?i:script))\b(?![^&gt;]*/&gt;)(?!.*type=["']text/(template|html|ng-template)['"])</string>
```

This makes Sublime support text/template, text/html and text/ng-template.

You can also download the HTML.sublime-package file and replace the one found inside your installation. Make sure to backup the old one before doing so.

MarkdownEditing Theme Settings
------------------------------

This is for Github Flavored Markdown:

```json
{
    "extensions": [
        "mdown",
        "txt",
        "md"
    ],
    "font_options": [
        "subpixel_antialias",
        "directwrite"
    ],
    "color_scheme": "Packages/MarkdownEditing/MarkdownEditor.tmTheme",
    "draw_centered": false,
    "word_wrap": true,
    "wrap_width": false,
    "line_numbers": true,
    "highlight_line": true
}
```

Fin
---

Restart Sublime Text Editor!
