# Making a devcontainer

A `.devcontainer` is a configuration file used by the Visual Studio Code Dev Containers extension to create a development environment inside a container. This allows developers to work in a consistent and isolated environment regardless of the host operating system or dependencies installed on the host machine

To use a `.devcontainer` in Visual Studio Code, you need to have the Dev Containers extension installed. Once installed, you can open a folder in a container by running the `Dev Containers: Open Folder in Container...` command from the Command Palette or quick actions Status bar item. This will create a container based on the configuration specified in the `.devcontainer` file and mount the project folder inside the container. The container will then be used as the development environment for the project

The `.devcontainer` file is a JSON file that specifies the container image to use, the environment variables to set, the extensions to install, and other configuration options for the container. The file is similar to the `launch.json` file used for debugging configurations

It is worth noting that running the full Visual Studio Code in Windows/Linux containers is not supported, but running with the Dev Containers extension is supported. When using the Dev Containers extension, the Visual Studio Code server is running in the container while the Visual Studio Code client is on the desktop.

The `.devcontainer` configuration file is a JSON file that specifies the container image to use, the environment variables to set, the extensions to install, and other configuration options for the container

It is typically stored in a `.devcontainer` directory or folder in the root of a project

The `.devcontainer` configuration file can be placed inside a `.devcontainer` folder or directory in the root of a project and it is not recommended to place it inside the `.vscode` folder.

Here is the documentation for .devcontainer for more reading:
<https://code.visualstudio.com/docs/devcontainers/containers>

This is the extension to install: `ms-vscode-remote.remote-containers`
