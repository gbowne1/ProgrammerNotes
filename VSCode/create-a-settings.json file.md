# Creating a settings.json file for VSCode

Ideally one should create a settings.json in a .vscode folder/directory in their project or project workspace
separated from the global settings.json file.

There are some things to remember here. IntelliSense if you have it set up, will show you

It is JSON Objects so it looks like

 ```json
 {
     "": ,
 }
 ```

It is helpful to add what VSCode allows language specific settings.  It's described by:

"[languagehere]": {
  "vscode.specificSetting": "value",
},
