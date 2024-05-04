# Spellchecking your code

Especially for C and C++, you should try using cSpell.

Install cSpell by `sudo apt install cspell`

In the project you are working on, `cspell init` will create the `cspell.json` configuration file.

For a system/user wide configuration file, use `~/.cspell.json` and/or `~/.cspeignore`

The cspell.json will look like

{
  "version": 1,
  "language": "en-US",
  "words": ["customword1", "customword2"],
  "ignorePatterns": ["node_modules/", "public/"]
}

## VSCode Extension

Go to extensions and search for `Code Spell Checker` by `streetsidesoftware`. This extension can use cspell.json

## using cSpell

to check spelling, do a `cspell` in your console/terminal/shell/tty/bash or whatever shell you use.

The github is at <https://github.com/streetsidesoftware/cspell>
