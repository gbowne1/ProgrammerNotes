# Create a launch.json

You can create a `launch.json` file for Visual Studio Code.  The can be automatically created by the UI, but not too hard to create one of your own.

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
    "sourceMaps": "",
    "MIMode": "",
    "setupCommands": "",
    "externalConsole": "",
    "environment": [],
    "miDebuggerPath": "",
    "stopAtEntry": "",
    "processId": "",
    "remotePath": "",
    "showLog": "",
    "port": "",
    "host": "",
    "preLaunchTask": "",
    "envFile": "",
    "mode": "",
    "apiVersion": "",
    "logOutput": "",
    "trace": "",
    "logging": "",
    "skipFiles": "",
    "console": ""
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

- "name" needs to be a string and the "name" is purely descriptive and is used to identify the configuration in the VS Code UI.

- "type" The supported types are `node`,`php`,`go`,`cppvsdbg`,`cppdbg`,`msedge`,`python`,`python`,`clr` and it is used to
  specify the type of   debugger to use for the launch configuration

Here are uses for the supported types:

- node for Node.js debugging.
- php for PHP debugging.
- go for Go debugging.
- cppvsdbg for C++ debugging with Visual Studio Windows debugger.
- cppdbg for C++ debugging with GDB or LLDB.
- msedge for debugging with Microsoft Edge.
- python for Python debugging.
- java for Java debugging.
- coreclr or clr for C# debugging with .NET Core or .NET Framework.

- "request" values are either "launch" or "attach"

- "program" attribute specifies the path to the program that the debugger should launch or attach to, and is usually pointed to the entry point

- "args" this attribute is used to specify command-line arguments that will be passed to the program when it is launched. The accepted values for "args" are an array of strings, where each string represents an argument

- "cwd" this is the current working directory and usually is set to ${workspacFolder} and in Visual Studio Code refers to the path & directory from which the debugger launches or attaches to the program.

- "env" are environment variables passed to the debugger and the "env" attribute is used to define environment variables for the launched or attached program

- "sourceMaps" are a boolean.  true or false.  For transpiled languages like TypeScript, Babel, Webpack. is used to control whether source maps are used during debugging.

- "MIMode" accepts "gdb" and "lldb" and is used to specify the debugger that VS Code will connect to for C++ debugging.

- "setupCommands"  is used to specify an array of commands that are executed to set up the debugger environment before the debugging session starts. the array includes the properties "text", "description" and a boolean "ignoreFailures". and the array must start with [ and end with ] and contains parenthesis pairs {}. these commands are specific to GDB or LLDB.

- "externalConsole" is used to specify whether the program being debugged should run in an external console or use the
  integrated terminal within VS Code. this value is a boolean, true or false.

- "environment" is the same as "env", and the "environment" attribute is used to specify environment variables for the program being debugged.

- "miDebuggerPath"  is used to specify the path to the debugger executable (such as GDB or LLDB) when the "MIMode" is set to "gdb" or "lldb".

- "stopAtEntry" is a boolean value, true or false and used to control whether the debugger should pause execution at the
  entry point of the program when a debugging session starts.

- "processId"  is used to specify the process ID to which the debugger should attach and should be a integer
  process ID or ${command:pickProcess} which will prompt you for the ID.  The "request" field should be "attach".

- "remotePath"  is used to specify the path to the source code on the remote machine when remote debugging. the "host"
  and "port" should be set. use `null` if the path is the same on both machines.  It should be set to the path of the
  source code on the remote machine.

- "showLog" - is a boolean value true or false and is used to control whether the debug logs should be displayed in the Debug Console

- "port": mainly used for the remote debugging.

- "host": mainly used for the remote debugging.

- "preLaunchTask" is used to specify the name of a task defined in tasks.json that should be executed before the debugger starts.
  This should be the name of a task as defined in the tasks.json file. This should be a string that matches the "label" property
  of a task in your tasks.json file.  It can be also `null` if there is no tasks.json task. This task will run before debugging begins.

- "envFile" is used to specify the path to a file containing environment variables to be loaded into the debugging session. this is typically set to ${workspaceFolder}/.env and is used with the "node" type.

- "mode" is either set to "launch" or "attach" and might be used the same as "request", however this is not a standard setting and may be deprecated, use "request" instead.

In this case:

- "launch": This mode is used to start a new instance of the application for debugging. It's typically used when you want to debug your application from the start.

- "attach": This mode is used to attach the debugger to an already running instance of the application. It's useful for debugging applications that are already in a running state.

- "apiVersion" is only used to specify the "Delve" version and only using when debugging Go.

- "logOutput" particularly when debugging Go code, the "logOutput" attribute is used to specify which components of the debugger should log their output. can be a comma separated list of components. the accepted values are "debugger", "gdbwire", "lldbout", "debuglineerr", "rpc".

## Alternative launch.json configuration styles

launch.json configs can also be specified without the configuration array like:

```json
{
    "name": "Launch file",
    "type": "go",
    "trace": "verbose",
    "showLog": true,
    "logOutput": "debugger,gdbwire",
}
```
