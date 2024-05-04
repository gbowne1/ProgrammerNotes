# VSCode workspaces

You can open workspaces in several ways

Double-clicking the .code-workspace file
Using the "File > Open Workspace" command in VS Code and selecting the workspace file
Choosing the workspace from the "File > Open Recent" list (if you've previously opened it)

Configuration file is typically `yourprojectworkspacenamehere.code-workspace` and is typically also written in JSON format.

{
  // Folders to be included in the workspace
  "folders": [
    {
      "path": "src"
    },
    {
      "path": "tests"
    }
  ],
  // Optional: Workspace-specific settings (example: code formatting)
  "settings": {
    "javascript.format.enable": true,
    "javascript.format.insertSpaces": false
  }
}
