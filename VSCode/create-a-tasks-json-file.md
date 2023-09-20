# Create a tasks.json

There are certain tasks that Visual Studio Code can do.  They will be made available in the `Terminal` menu.

You can create a file `tasks.json` that will accomplish this.  The current "version" of the file is `2.0.0` set in `version`.

You can use `IntelliSense` to help you create valid `tasks.json` files.

The official documentation for this is: <https://code.visualstudio.com/docs/editor/tasks> but you can see the link in the file comment.

Here is the file structure:

```json
{
 // See https://go.microsoft.com/fwlink/?LinkId=733558
 // for the documentation about the tasks.json format
 "version": "2.0.0",
    "tasks": [{
     "type": "",
     "label": "",
     "command": "",
     "args": "",
     "options": "",
     "problemMatcher": "",
     "group": "",
     "presentation": "",
     "dependsOn": "",
     "isBackground": "",
    ],
}
```
