# IntelliSense Configuration

Configuration for C/C++ Extension with the extension id of
`ms-vscode.cpptools`is done in Visual Studio Code with the `c_cpp_properties.json` file.

The `c_cpp_properties.json` file is usually kept in the workspace folder of a C/C++ project in Visual Studio Code. This is used to configure the `IntelliSense` in Visual Studio Code

Alternatively, you can create the file manually and configure it to your needs. If you want to set a global `c_cpp_properties.json` file for the entire workspace, you can create a single file and place it in the root of the workspace.

If the file is not present in the workspace folder, you can create it manually by running the `C/C++: Edit Configurations (UI)` command from the Command Palette (Ctrl+Shift+P) and saving the configuration.

The `c_cpp_properties.json` file can also be kept in the `.vscode` folder of a project.

It generally looks like this in Linux:

```json
{
 "env": "",
 "configurations": [
  {
   "name": "Linux",
   "includePath": [
    "${workspaceFolder}/**",
    "/usr/include",
    "${workspaceRoot}",
   ],
   "defines": [],
   "compilerPath": "/usr/bin/g++-8",
   "cStandard": "c11",
   "cppStandard": "c++17",
   "compilerArgs": "",
   "browse": {
        "path": [
        "${workspaceFolder}/**",
        "/usr/local/include",
        "/usr/include/x86_64-linux-gnu",
        "/usr/include"
        ]
   },
   "compileCommands": "",
   "forcedInclude": [],
   "limitSymbolsToIncludedHeaders": true,
   "intelliSenseMode": "linux-gcc-x86",
   "configurationProvider": "ms-vscode.cmake-tools",
   "databaseFilename": "${workspaceFolder}/.vscode/browse.vc.db",
   "enableConfigurationSquiggles": "",
   "mergeConfigurations": "",
   },
  ],
 "version": 4
}
```

I don't use this in Mac or Windows so this would be the best configuration for using the GNU compilers, debuggers and the linker.

The default value for the `intelliSenseMode` property in the `c_cpp_properties.json` file is `default`.

This means that the extension will try to automatically detect the correct IntelliSense engine to use based on your project configuration. If the extension is unable to detect the correct engine, it will fall back to using the Clang C++ compiler for x64 architectures.

Well, anyhow.. the attributes this configuration file uses are typically under the header "configuration".


name: 