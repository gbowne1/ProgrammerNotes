# Introduction to CMake

CMake is a powerful tool used in software development to manage the build process of C and C++ projects. It allows developers to write a single set of build instructions that can be used to generate native build files for different platforms and IDEs. This is particularly useful for developers working on multiple platforms or collaborating with others who use different development environments.

The tutorial aims to introduce the basics of CMake to an audience with some experience in development. By providing step-by-step guidance, the tutorial seeks to help learners understand how to use CMake to efficiently manage and build their projects, thereby enhancing their skills in software development and preparing them for more advanced topics in the future.

CMake is an open-source build system generator for software projects that allows developers to specify build parameters in a simple, portable, text file format.  The repository is at <https://github.com/Kitware/CMake> if eventually you would like to contribute to it.

It is used to manage the build process in an operating system and in a compiler-independent manner, generating standard build files from configuration files called CMakeLists.txt.

This makes CMake a powerful tool for simplifying the build and compilation process of software projects, especially for cross-platform development. One of the key reasons to use CMake is its ability to handle the difficult aspects of building software, such as cross-platform builds, system introspection, and user-customized builds, in a simple manner that allows users to easily tailor builds for complex hardware and software systems.

CMake generates project files for native build tools, including Integrated Development Environments (IDEs) such as Microsoft Visual Studio or Apple’s Xcode, as well as UNIX, Linux, NMake, and Ninja.

This simplifies the build process and provides a unified build system, which is particularly beneficial for cross-platform projects. In addition to its cross-platform capabilities, CMake provides the ability to create complex, custom commands for automatically generated files, select optional components at configuration time, and easily switch between static and shared builds

It also supports automatic generation of file dependencies and parallel builds on most platforms, making it a versatile and efficient build system generator for various software projects

Overall, CMake's simplicity, portability, and powerful features make it an essential tool for managing the build process of software projects, especially for developers working on cross-platform applications.

They have some documentation here: <https://cmake.org/> that is well beyond the scope of this tutorial and not recommended because it can generally be confusing to the new user, especially the included examples.

This document aims to fix that.  These are also some of the things I learned about CMake.

## Setting Up CMake

Setting up and configuring CMake for cross-compiling on Linux, Windows, or macOS involves creating a toolchain file that describes the target platform, adjusting the CMakeLists.txt file, and using system inspection tests for determining the properties of the target system. Here's a brief overview of how to set up and configure CMake on each system type:

- Linux
    To set up CMake for cross-compiling on Linux, you need to create a toolchain file that describes the target platform. This file tells CMake everything it needs to know about the target platform. After setting up the toolchain file, CMake will know how to handle the target platform and the cross-compiler. You can then build software for the target platform

- Windows
    For Windows, you can use CMake to build a C++ project by selecting the appropriate generator. After generating the project, you can build and install the executable file and library. When running the executable, you may need to add its bin folder to the PATH environment variable

- macOS
    On macOS, you can create a toolchain file that describes the target platform and use it to build the project. After setting up the toolchain file, you can build and install the executable file and library. When running the executable, you may need to add its bin folder to the PATH environment variable

### Installing CMake

CMake is a cross-platform, open-source software written in C++ that simplifies the build process for
software projects

Precompiled binaries are available for download from the official CMake website, making installation
straightforward for various platforms.

For Unix-based systems, ready-to-install packages can be obtained directly from the command line.

It's important to note that CMake doesn't come with compilers, so if they are not already installed on the system, they need to be provided and their paths added to the PATH environment variable for CMake to find them

Additionally, building from the source is an option, although it is relatively slow and requires more steps and may not be an optimal procoess for a begginer.

To install CMake on Linux, Mac, and Windows, you can follow these steps:

- Linux

    Using Package Manager: On Ubuntu/Debian, you can install CMake using the APT repository. Open a terminal and run:

    ```shell
    sudo apt update
    sudo apt install cmake
    ```

- Mac/OSX/Apple/Darwin:

    Using Homebrew: If you use Homebrew, you can install CMake by running the following command in the terminal:

    ```shell
    brew install cmake
    ```

- Windows:

    Using Official Installer: You can download CMake from KitWare's website. The official installer is a common way to get CMake on Windows. After downloading, run the installer and follow the installation instructions.

### Configuring CMake for Different Platforms

CMake supports various platforms, including Unix-based systems, Windows, and macOS. On Windows, a popular choice for finalizing the build process started by CMake is Visual Studio, which is available for free from Microsoft's website

For Linux, CMake can be installed using package managers such as apt-get for Debian/Ubuntu and yum for Red Hat, or by downloading and running the installation script

macOS is also strongly supported by CMake developers, with installation options available through MacPorts or Homebrew.

This makes CMake a versatile tool for configuring and building projects across different platforms and for various use cases. This example provides an overview of installing CMake and configuring it for different platforms, highlighting the availability of precompiled binaries, installation methods for specific platforms, and support for cross-compiling.

## Basic CMake Concepts

CMake uses CMakeLists.txt files to define how the project should be built.

These files contain commands and instructions for building the project, such as setting the project name,
specifying the source files, and declaring dependencies.

Below is an example of a CMake build system for a C++ project:

```cmake
     # Minimum version of CMake required to build this project
     cmake_minimum_required(VERSION 3.0)

     # Name of the project
     project(MyLibrary)

     # Add a library to this build. The name of the library is MyLibrary and it consists of only the MyLibrary.cpp file
     add_library(MyLibrary src/MyLibrary.cpp)
```

In this example, we set the minimum required CMake version, define the project name, and add a library to the build. The add_library command specifies the name of the library and the source file it consists of.

This is a required to be the first line or command in the CMakeLists.txt file.  This author suggests not to set the version to anything less than 3.0 because features were added after 2.8 that changed how things are.  Most developers choose to set this to the version to the one they have installed on their system.

This is a basic example to demonstrate the structure of a CMakeLists.txt file for a C++ project

Variables, functions, and control structures in CMake
Creating a simple "Hello World" C++ project using CMake

## Building C++ Projects with CMake

// TODO Finish this section

The command `cmake ..` is used to run CMake in the parent directory of the current working directory, while `cmake` without any arguments is used to run CMake in the current working directory. When you run `cmake ..`, CMake will look for the `CMakeLists.txt` file in the parent directory and use it to generate the necessary build files in the current directory. This is useful when you want to keep the source directory clean and separate from the build files.

This approach is known as an "out-of-source" or "shadow" build. It allows you to build the project in a directory that is different from the source directory, which helps to keep the source directory clean and prevents build artifacts from cluttering the source tree. When you run `cmake ..`, CMake will generate the build files in the parent directory of the source directory, effectively separating the build artifacts from the source code. This approach is recommended as it allows for multiple builds with different options but just one copy of the source code. It also makes it easier to clean up build artifacts by simply deleting the build directory. In summary, using `cmake ..` allows for an organized project structure where the source directory remains clean and separate from the build files, leading to easier maintenance and management of the projec

On the other hand, when you run cmake without any arguments, CMake will look for the `CMakeLists.txt` file in the current directory and use it to generate the build files in the same directory. This is useful when the `CMakeLists.txt` file is located in the current directory. Both `cmake ..` and cmake without arguments are commonly used to initiate the CMake configuration and generate the build files for a C or C++ project

Next we will talk some about using `cmake --build .` command

Another option to use in building projects with CMAke is `cmake -B build`. To use this, create a folder or directory called `build`.  This command will build the project inside the folder or directory named `build`.

## Generating Build files with CMake

The -G option is used to specify the generator, which determines the build system that CMake will generate.

`cmake -G "Unix Makefiles" path_to_source_directory`

The possible options for the -G flag in CMake are the various generators that can be used to generate the build system. Some of the common options include:

- Unix Makefiles: Generates standard makefiles.
- Ninja: Generates build.ninja files for use with the Ninja build system.
- Visual Studio [version]: Generates Visual Studio project files.
- Xcode: Generates Xcode project files.
- CodeBlocks: Generates CodeBlocks project files.
- Eclipse CDT4: Generates Eclipse CDT 4.0 project files.

These are just a few examples of the possible options for the -G flag. The full list of available generators can be obtained by running cmake --help or by referring to the CMake documentation

## Cross-Platform Development

Cross-compiling, which involves building software on one system for a different target platform, is fully supported by CMake, and it requires the use of a toolchain file to specify the target platform and cross-compiler settings

CMake supports cross-platform development by allowing the writing of platform-independent CMake code

It can handle different compilers and build tools, making it suitable for multi-platform development.

This capability is essential for scenarios where the build system and the target platform differ significantly, such as in embedded systems development or cross-platform application development

To enable cross-compiling with CMake, a toolchain file must be created to describe the target platform. This file, known as the "toolchain file," provides CMake with the necessary information about the target platform and cross-compiler settings

The toolchain file specifies details such as the target system's operating system, hardware architecture, and the location of the cross-compilation tools. This allows CMake to generate the appropriate build files tailored to the target platform, ensuring that the software is built correctly for the intended environment

CMake's support for cross-compiling is comprehensive, covering a wide range of scenarios, from cross-compiling from Linux to Windows, to cross-compiling for supercomputers and small embedded devices without an operating system

The toolchain file is crucial in informing CMake about the target platform, allowing it to handle the differences between the build platform and the target platform effectively. By separating the information about the build platform and the target platform, CMake provides mechanisms to address cross-compiling issues without additional requirements such as running virtual machines.

This flexibility makes CMake a versatile tool for configuring and building projects across different platforms and for various use cases.

In addition to the toolchain file, CMake provides built-in support for cross-compiling through the use of the CMAKE_TOOLCHAIN_FILE variable.

When CMake is invoked with the command line parameter --toolchain path/to/file or -DCMAKE_TOOLCHAIN_FILE=path/to/file, the specified toolchain file is loaded early to set values for the compilers, enabling seamless cross-compilation

This approach simplifies the process of configuring CMake for cross-compiling, making it easier for developers to manage the build process for diverse target platforms. Overall, CMake's robust support for cross-compiling, combined with its ability to handle different compilers and build tools, makes it an ideal choice for multi-platform development. By allowing the writing of platform-independent CMake code, developers can create projects that can be built and run on various platforms without the need for extensive platform-specific modifications

This capability streamlines the development process and ensures that projects can be efficiently deployed across different environments.

To name a CMake toolchain file, you can use any name you prefer, but it's common to use a name that reflects its purpose or the target platform. For example, you can name it `mytoolchain.cmake` or `crosscompile.cmake`.

The file extension used with a CMake toolchain file is .cmake.

When using the toolchain file, you can specify it using the -DCMAKE_TOOLCHAIN_FILE option followed by the path to the toolchain file. For example, if the toolchain file is named `mytoolchain.cmake` and is located in the current directory, you can use the following command to specify it:

```bash
cmake -DCMAKE_TOOLCHAIN_FILE=./mytoolchain.cmake path_to_source_directory
```

This will instruct CMake to use the specified toolchain file for the build.

## Advanced CMake

// TODO Add more advanced topics to this section

Conditional Compilation:

Conditional compilation in CMake allows developers to include or exclude certain parts of the code based on predefined conditions. This is often achieved using preprocessor directives, which are evaluated at compile time. CMake provides a powerful mechanism for conditional compilation through the use of compile feature requirements. These requirements can be specified with the target_compile_features command, allowing developers to specify the required language features for a target. For example, target_compile_features(my_target PRIVATE cxx_constexpr) specifies that the target my_target requires the constexpr feature. This ensures that the in-use C++ compiler is capable of the feature and adds any necessary flags to the compile lines of C++ files in the target. If the compiler is not capable of the feature, a FATAL_ERROR is issued. CMake computes the appropriate compile flags to use by considering the features specified for each target

Macros and Functions:

CMake supports the use of macros and functions to define reusable code snippets and perform repetitive tasks. Macros in CMake are defined using the macro command, and functions are defined using the function command. These macros and functions can be invoked with parameters, allowing for flexibility and reusability in CMake scripts. They are particularly useful for abstracting complex operations into simple, reusable components, thereby improving the maintainability and readability of CMake code. By encapsulating common operations within macros and functions, developers can streamline the development process and reduce code duplication. This approach aligns with the principles of modular and maintainable software development, enabling efficient management of CMake projects

CMake Variables and Properties:

CMake variables and properties play a crucial role in configuring and controlling the build process. Variables in CMake are used to store and manipulate data, while properties are used to define characteristics and behaviors of targets, source files, and directories. CMake provides a set of built-in variables and properties, and developers can also define custom variables and properties to suit their specific project requirements. Variables are typically used to store user input, configuration settings, and intermediate values, while properties are used to specify target-specific settings such as compile options, include directories, and dependencies. By leveraging variables and properties, developers can customize the build process, manage project settings, and ensure consistent behavior across different platforms and configurations. This flexibility and configurability make CMake variables and properties essential components for effectively managing CMake projects

The ability to conditionally compile code, define macros and functions, and utilize variables and properties in CMake scripts provides developers with powerful tools for customizing and controlling the build process. These features enable developers to create flexible, maintainable, and platform-independent build systems, aligning with the principles of modern software development. By leveraging these capabilities, developers can efficiently manage complex build configurations, streamline the development workflow, and ensure the portability and reliability of their CMake projects.

## Building with CMake

CMake can generate a native build environment that compiles source code, creates libraries,
generates wrappers, and builds executables in arbitrary combinations

It supports in-place and out-of-place builds, as well as static and dynamic library builds.

## Managing Dependencies

CMake allows for adding external libraries, linking libraries, and handling header files.
It provides commands to find and use libraries, include directories, and other dependencies required by the project.

## Adding External Libraries

In CMake, you can add external libraries using the find_library command to locate the library file and the target_link_libraries command to link the library to your project. For example, to add an external library named mirsdrapi-rsp, you can use the following commands in your CMakeLists.txt file:

```cmake
find_library(mirslocation NAMES mirsdrapi-rsp HINTS ${SDR_API_PATH} NO_CMAKE_FIND_ROOT_PATH)
add_library(mirs STATIC IMPORTED)
set_target_properties(mirs PROPERTIES IMPORTED_LOCATION ${mirslocation})
target_link_libraries(your_project_name mirs)
```

This code snippet demonstrates how to find the library, import it as a static library, and link it to your project.

## Linking Libraries

To link libraries in CMake, you can use the target_link_libraries command. This command specifies that the given target (e.g., your project) depends on libraries. For example, to link a library named mirs to your project, you can use the following command:

```cmake
target_link_libraries(your_project_name mirs)
```

Replace your_project_name with the actual name of your project. This command ensures that the specified library is linked to your project

`target_link_libraries` is a CMake command used to specify libraries or flags to use when linking a given target and/or its dependents. It has several signatures, all with the general form: `target_link_libraries(<target> ... <item>... ...)`. The named `<target>` must have been created by a command such as`add_executable` or `add_library` and must not be an INTERFACE library. When a library is linked to a target using `target_link_libraries`, the usage requirements from linked library targets will be propagated. The usage requirements of a target's dependencies affect the compilation of its own sources. The command has different scopes, including PRIVATE, INTERFACE, and PUBLIC, which define how dependencies of a library will affect consumers of that library. Using `target_link_libraries` to link a target to an internal target will not only add the linker flags required to link to the internal target, but also the definitions, include paths, and other settings, even transitively, if they are configured that way.

`target_link_libraries` is a crucial CMake command that is responsible for adding a library into the linker's command line. It is used to specify the libraries or flags to use when linking a given target and/or its dependents.  This command is essential for ensuring that the necessary libraries are linked to the target, and it allows for the propagation of usage requirements from linked library targets. If the `target_link_libraries` line is not added, it can hurt performance because the necessary libraries may not be linked correctly, leading to runtime errors or performance degradation. By using `target_link_libraries`, the required libraries are linked in a way that ensures the target and its dependents have access to the necessary components for optimal performance. In summary, the advantages of including `target_link_libraries` are:

- It ensures that the necessary libraries are linked to the target and its dependents.
- It allows for the propagation of usage requirements from linked library targets, ensuring that the target has
  access to the required components for optimal performance

Proper usage of the target_link_libraries command in CMake is essential for specifying the libraries or flags to use when linking a given target and its dependents. The command has different scopes, including PRIVATE, INTERFACE, and PUBLIC, which define how dependencies of a library will affect consumers of that library. Using `target_link_libraries` to link a target to an internal target will not only add the linker flags required to link to the internal target, but also the definitions, include paths, and other settings, even transitively, if they are configured that way. It is crucial for ensuring that the necessary libraries are linked to the target and its dependents, and it allows for the propagation of usage requirements from linked library targets, ensuring that the target has access to the required components for optimal performance

## Handling Header Files

To handle header files in CMake, you can use the include_directories command to specify the directories where the header files are located. For example, to include header files from an external library, you can use the following command:

```cmake
include_directories(${SDR_API_PATH})
```

Replace ${SDR_API_PATH} with the actual path to the directory containing the header files. This command ensures that the specified directory is included in the list of directories to search for header file(s).

## Integration with C/C++ and Web Development

// TODO Add this section

    Integrating CMake with C and C++ projects
    Using CMake for web development projects

## Using CMake to do testing
