# Create a launch.json

You can create a `launch.json` file for Visual Studio Code.

The file format is:

```json
{
 // Use IntelliSense to learn about possible attributes.
 // Hover to view descriptions of existing attributes.
 // For more information, visit: https://go.microsoft.com/fwlink/linkid=830387
 "version": "0.2.0",
 "configurations": [
  {
  "name": "",
  "type": "",
  "request": "",
  "program": "",
  "args": [],
  "cwd": "",
  "env": [],
  "sourcemap": "",
  "MIMode": "",
  "setupCommands": "",
  "externalConsole": "",
  "environment": [],
  "miDebuggerPAth": "",
  "stopAtEntry": "",
  "processId": ""
  }
 ]
}
```

To see the default configuration for a debugger, you can go to the Run and Debug view in Visual Studio Code and select the "create a launch.json file" link. This will create a `launch.json` file with a default configuration for the selected debugger, including a link to the official documentation for the attributes.

To run a launch.json configuration in Visual Studio Code 1.81 for Linux, you can follow the steps below:

1. Open your project in Visual Studio Code.
2. Press Ctrl+Shift+D to open the Run and Debug view.
3. Select the configuration you want to run from the drop-down menu in the top toolbar.
4. Click the green "Run" button to start the debugging session.

Once you have created a `launch.json` file, you can customize the configuration settings to match your debugging scenario. For example, if you want to configure `launch.json` for `cppdbg`, you can set the "type" field to `"cppdbg"` and the "request" field to "launch", and specify the path to the executable you want to debug in the "program" field.
