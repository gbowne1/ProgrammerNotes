# Structuring a C++ program

There are indeed many possibilities of creating and structuring the files of a program with C++. In this text `folder` and `directcory` will be interchangeable and used as meaning the same thing, but will use the word `directory` to mean either one.

First of all, the structure of the program you've created should be maintainable by yourself and anyone involved in the project.

Why? It makes sense to not make so much work of yourself or anyone else, even if no one else may look at the code or the structure of your program and not just because it will save time.

There are some traditional C and C++ program structure conventions that will make this a bit easier for you and anyone else involved.

Here is a guide to creating a maintainable project in C++:

Create your project directory.

In that directory, create a directory called `src`.

Also in that directory, create a directory called `include`. All of your header files with the extension of `.h` will be placed. You also might choose to put the `include` directory inside the `src`. There is no distinct reasoning behind this, however this decision can be left up to the developer to choose which one. We will talk more about this in a bit.

In the main directory, create a main.cpp file. This will be the entrypoint to your program, and it will have a int main(); function. This entrypoint should stay in the root directory of the project.

From here you can and should try and modularize your program and its code.

This refers to the practice of dividing code into smaller, independent, and cohesive units that perform specific tasks or functions. These units, often called modules, components, or classes, allow for better organization, reusability, and maintainability of the code. Modular programming emphasizes separating the functionality of a program into independent, interchangeable modules, with each module containing everything necessary to execute only one aspect of the desired functionality.

When it comes to C++, modular programming involves dividing a computer program into separate sub-programs or modules, each containing the necessary code to execute a specific aspect of the program's functionality. This approach allows for better management of large programs, increased maintainability, readability of the code, and ease of making changes in the future or correcting errors

Modularizing a C++ project's code offers several benefits. It makes the code easier to read, understand, and maintain by separating it into functions or modules, with each dealing with a specific aspect of the overall functionality.

This approach also reduces the chances of conflicts when multiple developers are working on the same codebase, leading to improved collaboration and productivity. Additionally, modularization can enhance code reusability, which is beneficial for future projects. However, it's important to note that excessive modularization can lead to code that is overly complex and difficult to manage, so at minimum try to be consistent.

The program should be subdivided into separate sub-programs or modules, with clear limitations and communication among them.

In C and C++, this can be achieved by dividing the code into smaller modules called functions or procedures, each handling a specific responsibility.

To modularize header files versus implementation files in C or C++, the general practice is to declare the functions, classes, and data structures in the header files, while the implementation details are defined in the implementation files (typically with a .cpp extension for
C++).

This separation helps in organizing the code and allows for better reusability and maintainability. However, there are cases where the implementation is included in the header file, such as for small, simple functions or when using templates. The decision on how to modularize depends on factors such as code complexity, project size, and performance considerations.

The decision to use a /src/ and /src/include/ directory versus a /include and a separate /src/ directory can depend on various factors. One advantage of the former is that it reduces the maintenance overhead for clients of the library, as they only need to be aware of one include directory, which reduces the risk of header name collisions

It also benefits implementors, as they can change the layout of their src directory without worrying about breaking library clients.

Additionally, it may have a small influence on build times, as having a smaller size folder with includes could potentially make the build process slightly faster.

On the other hand, the decision may also depend on the size of the project. For smaller projects, keeping the files in one directory tends to be more convenient, while for larger applications with hundreds or thousands of files, separating them into different directories becomes more practical.

The decision to use a /src/ and /src/include/ directory versus a /include and a separate /src/ directory can have both advantages and disadvantages.

Disadvantages of using a /src/ and /src/include/ directory:

- Complexity: It can add complexity to the project structure, especially for smaller projects

- Build System Configuration: It may require additional configuration in the build system to specify the include paths

- Verbose Include Paths: It can lead to verbose include paths, especially when using fine-grained modularization

How it can improve code organization:

- Reduces Maintenance Overhead: It reduces the maintenance overhead for clients of the library, as they only need to be aware of one include directory, reducing the risk of header name collisions

- Easier Reorganization: It makes it easier to reorganize the layout of the src directory without affecting library clients

- Influence on Build Times: It may have a small influence on build times, as having a smaller size folder with includes could potentially make the build process slightly faster

In the end, the choice between the two approaches is often a matter of preference and depends on the specific needs of the project. Both methods are valid, and it ultimately depends on the coding style and organizational preferences of the development team.

If your project will have a bunch of class files and keep this in in a practical and maintainable fashion.  Becuause many projects have a lot of files witih:

    ```cpp
    // other C++ code here

    class MyClass {

    }
    ```

The best practices for class files can be considered:

- Separation of Declaration and Definition: It is a common practice to separate the declaration of a class (interface) in a header file (.h or .hpp) and the definition (implementation) in a corresponding source file (.cpp).

- Namespace and Directory Structure: Organize the classes into namespaces and use a clear directory structure to reflect the namespaces. This helps in avoiding naming conflicts and makes the codebase more maintainable.

- Dependency Management: Use forward declarations to minimize dependencies between header files. This can help reduce compilation times and minimize the impact of changes.

- Use of Modules: With the introduction of C++20, modules provide a new way to organize code and manage dependencies. Consider using modules for better organization and encapsulation of code.

- Consistent Coding Style: Adopt a consistent coding style and adhere to best practices such as naming conventions, code formatting, and documentation. clang-format and clang-tidy will help out here immensely and we will cover this in another topic file or section.

- Unit Testing: Implement unit tests for the classes to ensure their correctness and maintainability over time.

This will help you or anyone else working with your project maintain your project multiple class files in a practical and maintainable fashion, it is important to follow best practices such as separating declaration and definition, organizing code into namespaces, managing dependencies, adopting new language features like modules, maintaining a consistent coding style, and implementing unit tests.

If you are working with someone elses C++ project, do your best to try and follow the code style they have used. It is usually reasonably easy to spot how the project is laid out.

If you are developing a C++ program that will be compiled to run on different platforms like Windows and Linux and Mac.

