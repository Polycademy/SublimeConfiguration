Sublime Text 3 Configuration
============================

Polycademy's preferred Sublime Configuration.

Theme
-----

Place Notepad++.tmTheme into the Packages location. This can be accessed via `Preferences -> Browse Packages`

Font
----

Acquire the Source Code Pro font and install this into your computer (https://github.com/adobe/source-code-pro)

Settings
--------

Copy paste the contents of Preferences.sublime-settings into your user settings. This can be accessed via `Preferences -> Settings - User`

Client Side Template Syntax Highlighting
----------------------------------------

Sublime Text Editor does not normally highlight the syntax of HTML that inside client side template script tags. For example AngularJS and Handlebars.

In order to make Sublime run syntax highlighting, first find the HTML.sublime-package zip archive. This is usually located where Sublime was installed. Copy this archive somewhere else and unzip. Open up HTML.tmLanguage file. On line 286 change:

```
<string>(?:^\s+)?(&lt;)((?i:script))\b(?![^&gt;]*/&gt;)</string>
```

into

```
<string>(?:^\s+)?(&lt;)((?i:script))\b(?![^&gt;]*/&gt;)(?!.*type=["']text/(template|html|ng-template)['"])</string>
```

This makes Sublime support text/template, text/html and text/ng-template.

You can also download the HTML.sublime-package file and replace the one found inside your installation. Make sure to backup the old one before doing so.

Packages
--------

Install Sublime Text 3 Package Control (https://sublime.wbond.net/installation)

Hit `Ctrl + Shift + P` and use Package Control to install these packages:

BracketHighlighter  
Notepad++.tmtheme  
AngularJS  
DocBlockr  
Emmet  
LESS  
Stylus  
Phoenix Theme  
Sublime-Github
SublimeLinter3
Floobits

Fin
---

Restart Sublime Text Editor!
