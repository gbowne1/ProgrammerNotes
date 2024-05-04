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
 "tasks": [
 {
 "type": "process",
 "label": "",
 "command": "",
 "args": [],
 "options": {},
 "problemMatcher": "",
 "group": "",
 "presentation": {},
 "dependsOn": "",
 "isBackground": true,
 }
 ],
 }
 ```

In `type`: The type of task to be executed.

These supported `types` are `"shell"`, `"process"`, `"npm"`, `"grunt"`, `"gulp"`, `"jake"`, `"msbuild"`, `"xcodebuild"`, `"ant"`, `"gradle"`, `"lein"`, `"make"`, `"pdflatex"`, `"python"`, `"ruby"`, `"gcc"`, `"clang"`, `"tsc"`, `"dotnet"`, `"docker-build"`, `"docker-run"`, `"docker-push"`, `"docker-compose"`, `"dart"`, `"dart-analyze"`, `"dart-test"`, `"dart-run"`, `"flutter"`, `"flutter-analyze"`, `"flutter-test"`, and `"flutter-run"`.

In `group`: A string or an object that specifies the group to which the task belongs.

The supported groups are `"build"`, `"test"`, `"deploy"`, `"clean"`, `"rebuildAll"`, `"buildAll"`, `"testAll"`, `"run"`, `"preview"`, `"install"`, `"uninstall"`, `"configure"`, `"update"`, `"watch"`, `"lint"`, `"format"`, `"extensionDevelopment"`, `"docker"`, `"docker-compose"`, `"remote-ssh"`, `"remote-containers"`, `"remote-wsl"`, `"remote-ssh-edit"`, `"remote-containers-edit"`, and `"remote-wsl-edit"`.

The order of properties in `tasks.json` does not matter. You can define the properties in any order you like, as long as they are valid JSON syntax
