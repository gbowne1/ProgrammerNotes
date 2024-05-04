# Introduction to C++ Programming

C++ is a powerful and versatile programming language widely used for developing system software, game engines, and applications. It can seem confusing to many beginners.

To get started with C++, you need to understand its syntax and features. A simple "hello, world" program is often the first step. Here's a basic example:

```cpp
#include <iostream>

int main() {
    std::cout << "Hello World";
    return 0;
}
```

In this program, `#include <iostream>` allows input/output operations. Including a `<iostream>` header file

The cout statement outputs "hello, world" to the console.

Learning C++ involves grasping concepts like variables, conditional statements, loops, functions, pointers, and classes. Text-based courses can be more efficient than video tutorials, allowing you to learn at your own pace.

## Compiling C++

To compile and run a C++ program on Linux, Windows, Darwin/Apple/Macintosh, and BSD, you can use various compilers such as GCC by using g++, Clang, and Visual C++ aka MSVC++. Here's a brief overview of how to compile and run a C++ program on these platforms:

- Windows
  - Clang
  - Microsoft Visual C++ aka MSVC++
  - MinGW?

- Linux
  - GCC using g++
  - Clang using clang++

- Darwin/Mac/MacOS/Apple
  - GCC
  - Clang

- BSD's

## Structure of a C++ file

The structure of a C++ file typically consists of a header file and a closely related implementation file. The header file, usually ending in ".h", contains class declarations and function prototypes, while the implementation file, often ending in ".cpp", contains the definitions of the methods declared in the header file. This separation helps split the interface from the implementation, resulting in declarations of member functions in the header file and their details inside the implementation file. Additionally, a C++ project may contain directories such as "bin" for the final executables, "build" for building files, "example" for example code, and "include" for header files. However, the specific project structure can vary based on the organization's coding conventions and requirements.

## C++ Program Entrypoint

n C++, the entry point of a program is where the execution of the program begins, and in C++, it is the main() function. When the program is executed, the control is passed to the main() function, and from there, the program's execution starts. The main() function can also accept command line arguments, allowing for flexibility in program execution. It is important to note that the main() function is the standard entry point for C++ programs, and changing it to another function is not a standard practice and may not be supported by all compilers or linkers. This is normally place in a file named `main.cpp`.

If you use any other program name, or do not need any other file you can use `int main()` after you include the headers, defines

## C++ Header Files and C++ classes

Creating a C++ class involves defining the class in a header file, which typically has a `.h` file extension, although could have a `.hpp` extension.  Traditionally, C++ header files use the `.h` file extension instead of `.hpp`.

In C++, each class is usually defined in its own header file, which contains the class declaration. The header file also includes any necessary function prototypes, member variables, and other declarations

Here's a basic example of a header file for a C++ class:

```cpp
// MyClass.h
#ifndef MYCLASS_H
#define MYCLASS_H

class MyClass {
public:
    MyClass();  // Constructor
    void myMethod();  // Member function
private:
    int myVariable;  // Member variable
};

#endif
```

In this example:

The #ifndef, #define, and #endif directives are used to prevent multiple inclusions of the same header file. The class MyClass is declared with its member functions and variables.

Header files are essential in C++ for several reasons:

- They allow for the separation of interface and implementation, making the code more modular and maintainable.

- They enable code reuse by allowing other parts of the program to access the class's interface without needing
  to know its implementation details.

- They facilitate the organization of large projects by providing a clear structure for the code.

Header files play a crucial role in organizing and maintaining C++ code. They contain function and data type
definitions and are imported into C++ programs using the #include preprocessor directive.

## Constructors

A constructor in C++ is a special method that is automatically called when an object of a class is created. It is used to initialize the data members of the object. The constructor has the same name as the class and does not have a return type. It can be used to set initial values for attributes and can take parameters like regular functions. There are different types of constructors in C++, including default constructors, parameterized constructors, and copy constructors. Constructors can be overloaded, and a class can have multiple constructors. They are mostly declared in the public section of the class, and they do not return values. Constructors can also be defined outside the class by specifying the name of the class followed by the scope resolution operator and the name of the constructor.

Constructors are essential for ensuring that an object is always in a valid state.

The primary purpose of constructors is to initialize the object's data members. They ensure that the object is in a valid state when it is created. Constructors eliminate the need for separate set methods to initialize the object's attributes, making the code more concise and readable.

An example C++ constructor

```cpp
class Car {
public:
    string brand;
    string model;
    int year;
    // Parameterized Constructor
    Car(string x, string y, int z) {
        brand = x;
        model = y;
        year = z;
    }
};

int main() {
    // Create Car objects and call the constructor with different values
    Car carObj1("BMW", "X5", 1999);
    Car carObj2("Ford", "Mustang", 1969);
}
```

## C++ Includes

In C++, files typically start with the first few lines including header files from the standard library.

Standard Header Files and Their Uses:

C++ provides standard libraries with header files that offer valuable functionalities to ease programming. For example:

- `<iostream>`: For input/output operations using cin and cout.
- `<fstream>`: For file creation and read/write operations.
- `<cmath.h>`: For common mathematical operations like sqrt() and pow()

## C++ Code quality

C++ code quality directly impacts readability, maintainability, and efficiency. High-quality code is well-formatted, easy to read, properly tested, and well-documented. It's free of bugs and supports future expansion of the codebase.

To produce quality C++ code, you can follow several best practices and guidelines. Some of the key recommendations I have include:

Follow a coding standard: Maintaining and following a set of standards is important in producing high-quality code. There are several common C++ code standards. Adhering to a coding standard, such as Google's C++ Style Guide or the C++ Core Guidelines, can help maintain consistency and readability in your code

Write readable code: Use proper indentation, whitespace, and comments to make your code easier to read.  This will help with maintainablilty.

Use descriptive and meaningful variable names: This makes your code easier to read and understand.

Write unit tests: Learning and using testing frameworks like GTest and GMock can help ensure the quality of your code. I would suggest using CTest from CMake.  GTest and GMock are from Google.

Use sanitizers and static analysis tools: These tools can help identify and prevent bugs and other issues in your code.

Embrace modern idioms: Familiarize yourself with modern C++ idioms and design patterns to write high-quality code

Utilize the standard library: C++ provides a rich set of standard libraries that can simplify your code and improve performance
By following these best practices, you can write clean, efficient, and high-quality C++ code.

Use smart pointers: Smart pointers, such as std::unique_ptr and std::shared_ptr, can help manage memory automatically and avoid memory leaks

Always initialize variables: Automatic variables should always be initialized at the point of definition to avoid using uninitialized memory

Check array bounds: Always ensure that you perform bounds checking when working with arrays to prevent buffer overflows and other security issues

Avoid raw pointers: Instead of using raw pointers, prefer smart pointers or other RAII (Resource Acquisition Is Initialization) techniques to manage resources and avoid memory leaks

## C++ Keywords and Operators

In C++, the keywords "for," "while," "if," "new," "else," "switch," "case," "delete," "continue," "break," "default," and "return" are used for various control flow and memory management purposes.

- "for" keyword is used to create a loop that consists of three optional parts: initialization, condition, and increment/decrement.

- "while" keyword is used to create a loop that executes a block of code as long as the specified condition is true.

- "if" keyword is used to execute a block of code if a specified condition is true.

- "new" keyword is used to dynamically allocate memory for a variable of a given type.

- "else" keyword is used to execute a block of code if the same condition is false.

- "switch" keyword is used to select one of many code blocks to be executed.

- "case" keyword is used within a "switch" statement to specify a block of code to be executed.

- "delete" keyword is used to deallocate memory that was previously allocated using "new."

- "continue" keyword is is used to skip the rest of the code inside a loop for the current iteration and continue to the next iteration.

- "break" keyword is used to terminate the loop or switch statement and transfer control to the statement immediately following the loop or      switch.

- "default" keyword is used within a "switch" statement to specify the code to be executed if no case matches.

- "return" keyword is used to exit a function and return a value to the caller.

Notes:

1. 'switch`,`case`,`break` and `default` are typically used together.
2. `while` sets up a loop condition.
3. `if` and `else` is typically used together in a if-else statement to do conditional checking

## C++ String literals

In C++, a string literal is a sequence of characters enclosed in double quotation marks. It has the type "array of n const char," where n is the size of the string, including the terminating null byte. This means that a string literal has the type const char[n] and has static storage duration

For example, "Hello" has the type "array of 6 const char" because it consists of 6 characters, including the null terminator. When used in a program, a string literal can be accessed as a const char* due to array-to-pointer conversion.

In C++, a string literal is a sequence of characters enclosed in double quotation marks. Here's an example:

```cpp
const char* greeting = "Hello, World!";
```

In this example, "Hello, World!" is a string literal enclosed in double quotation marks, and it is assigned to a pointer to const char.

## C++ Struct

A C++ struct is a user-defined data type that allows the grouping of several related variables into one place. It is similar to a class, but with different default visibility: struct members are public by default, whereas class members are private by default1

Here's a summary of the key points about C++ structs:

- Definition: A C++ struct is defined using the struct keyword, and its members are declared inside curly braces

- Members: Each variable in the structure is known as a member of the struct. Unlike arrays, a struct can contain
  many different data types such as int, string, bool, etc.

- Accessing Members: Members of a struct can be accessed using the dot syntax ( . )

- Comparison with Class: In C++, the only difference between a struct and a class is that the members and base
  classes of a struct are public by default, while a class has private members and base classes by default

Usage: Structs are commonly used for creating pure data structures, where the focus is on grouping related variables rather than implementing behavior

In object-oriented programming, using structs for pure data structures is not a bad idea, as it provides a convenient way to work with related variables. However, it's important to consider the design and purpose of the data structure when deciding whether to use a struct or a class.

Here is an example of a C++ struct:

```cpp
struct MyStruct {
  int myInt;  // Member variable of type int
  char myChar;  // Member variable of type char
  float myFloat;  // Member variable of type float
};
```

From here, in the int main(), one should:

- Create an instance of the struct
- Access and assign values to the members of the struct
- Access members of the struct

In C++, the only difference between a struct and a class is the default visibility of members. Struct members are public by default, while class members are private by default

## C++ `void`

In C++, "void" is used to indicate that a function doesn't return a value or that it has no parameters or both. When used as a function return type, it specifies that the function doesn't return a value. When used for a function's parameter list, it specifies that the function takes no parameters. Additionally, when used in the declaration of a pointer, "void" specifies that the pointer is "universal" and can point to any variable that's not declared with the const or volatile keyword. A void pointer can be converted into any other type of data pointer, but it can't be dereferenced unless it's cast to another type.

It is also used to declare universal pointers that can point to any type of data. The void data type has no values and no operations, representing the lack of a data type. When used as a pointer, "void" specifies that the pointer is "universal" and can point to any variable that's not declared with the const or volatile keyword. A void pointer can hold the address of any type and can be typecasted to any type.

In C++, void is used in different contexts. When used as a function return type, it specifies that the function does not return a value. When used for a function's parameter list, it specifies that the function takes no parameters. When used in the declaration of a pointer, void specifies that the pointer is "universal," and a void* pointer can point to any variable. Here's an example of a void function:

```cpp
#include <iostream>

// A void function that doesn't return anything
void sayHello() {
    std::cout << "Hello, World!" << std::endl;
}

int main() {
    // Call the void function
    sayHello();
    return 0;
}
```

This example defines a void function sayHello that simply prints "Hello, World!" when called from the main function. This demonstrates the use of void as a function return type.

A void function is one that does not return a value, while a non-void function returns a value. The void keyword is used in a function's parameter list to specify that the function takes no parameters. It is also used in the declaration of a pointer to create a "universal" pointer, void*, which can point to any variable. Here are some common use cases for void pointers in C++:

- Memory allocation: Void pointers are often used in memory allocation functions like malloc and calloc to allocate memory of any data type.

- Callback functions: Void pointers are used to pass a reference to any type of data to a callback function.

- Generic data structures: Void pointers are used to create generic data structures that can store any type of data.

## C++ enum

n C++, an enum, or enumeration, is a user-defined data type that allows you to create a new data type with a fixed range of possible values. It provides a way to define and group integral constants, making the code easy to maintain and less complex. Enums are generally used when you expect a variable to select one value from a set of possible values, increasing abstraction and enabling you to focus more on values rather than worrying about how to store them. They are helpful for code documentation and readability purposes

Here's an example of how to declare an enum in C++:

```cpp
enum season { spring, summer, autumn, winter };
```

It might also be used like this:

```cpp
enum MyEnum {
     ENUM1,
     ENUM2
};
```

In this first example, "season" is the name of the enumeration, and "spring," "summer," "autumn," and "winter" are the values of type "season." By default, "spring" is 0, "summer" is 1, and so on. You can also change the default value of an enum element during declaration if necessary

Enums are used to restrict data to certain values and provide it in a human-readable format. They are vital for any project where you need to work with a fixed set of values, such as game development or managing states of objects

An enum consists of named integral constants. It provides a way to define and group integral constants, making the code easy to maintain and less complex. Enums are generally used when you expect the variable to select one value from a possible set of values, increasing abstraction and enabling you to focus more on values rather than worrying about how to store them. To structure an enum in C++, you can use the following syntax

```cpp
enum EnumName {
    EnumValue1,
    EnumValue2,
    //...
};
```

For example:

```cpp
enum Color {
    Red,
    Green,
    Blue
};
```

This defines an enum type called "Color" with the values "Red", "Green", and "Blue"

Additionally, C++ 11 introduces enum class (or enum struct) to address some limitations of the traditional enum. Enum class (or enum struct) provides type safety, scope, and the ability to specify the underlying type. Here's an example of how to define an enum class

```cpp
enum class EnumName : underlyingType {
    EnumValue1,
    EnumValue2,
    //...
};
```

For example:

```cpp
enum class Status : char {
    Active,
    Inactive
};
```

This defines an enum class type called "Status" with the values "Active" and "Inactive", and the underlying type is specified as "char".

## Compiled C++ code

In C++, when you compile a source file, it is converted into an object file. The object files resulting from the compilation of multiple source files are then linked into an executable, a shared library, or a static library. Here are the differences between the common compiled object files in C++:

- `a.out` file: This is the default name of the executable file produced by the compiler if no other name is specified. It is the final output of the linking step when compiling C++ source files

- `.bin` file: In C++, there is no standard file format for binary files. The .bin extension is often used for generic binary files, but it is not specific to C++ object files

- `.obj` file: This is the standard extension for object files in the Windows environment. Object files contain machine code and are the result of compiling C++ source files. They are later linked to produce an executable or a library

- `.o` file: Also an object file.

- `.s` file: Assembly output of the compiler's compilation phase and have a ".s" extension. They contain the assembly code generated from source, this is typically used by MASM or GAS (GNU Assembler or `as`)

Other common compiled object files: In addition to the above, C++ also uses shared libraries (.so files in Unix-based systems, .dll files in Windows) and static libraries (.a files in Unix-based systems, .lib files in Windows) for modularizing code and reusing it across different programs also .exe files.

It's important to note that object files created with different compilers are generally not binary-compatible due to differences in implementation-defined details such as the size and alignment of data types.

Therefore, when distributing precompiled C++ libraries, it is often expected that the same compiler will be used for linking to ensure binary compatibility

Understanding the compilation and linking steps in C++ is crucial for efficient code development and debugging

Each C++ source file needs to be compiled into an object file, and the resulting object files are then linked into an executable, a shared library, or a static library

Additionally, C++ also uses shared libraries (.so files in Unix-based systems, .dll files in Windows) and static libraries (.a files in Unix-based systems, .lib files in Windows) for modularizing code and reusing it across different programs.

In C or C++, .o files are object files that are created when a non-header file is compiled. They contain binary code that is "almost" executable. These files are the output of the compiler and input to the linker/librarian. On the other hand, .so files are shared object files that are created when you want to share code between different executables. They are essentially shared libraries and are used for dynamic linking. In C or C++, both .o and .so files exist. The .o files are used during the construction of the executable, while the .so files are used for dynamic linking and sharing code between different executables

Compiling C++ code involves converting each source file into an object file, and then linking the object files together to create an executable. Here's a summary of the process:

Compilation: Each C++ source file is compiled into an object file. This involves several stages, including preprocessing, compiling, and assembling. The result is a collection of object files, one for each source file.

Linking: The linker takes the object files and combines them into a single executable. It resolves references between the files, links in any necessary libraries, and produces the final output.

Here are some key points to note:

C++ source code is split into header and source files and each part is seen by the compiler in a different way, which affects the compilation and linking process

The compilation process involves preprocessing, which deals with directives like #include, and the result is a pure C++ program file

The linker's job is to link together the object files into a binary executable.

For example, to compile a C++ program consisting of multiple source files, you would first compile each source file into an object file, and then link the object files together to create the executable. Here's a simple illustration of the commands involved:

 ```bash
  g++ -c file1.cpp
  g++ -c file2.cpp
  g++ -o myprog.exe file1.o file2.o
 ```

This sequence compiles each source file into an object file and then links the object files together to produce the executable myprog.exe

There are two methods for liking. Static linking and dynamic linking are the two methods used to combine external libraries with a C++ program.

Here are the key differences between the two:

Static Linking:

In static linking, all the necessary library code is copied into the final executable file during the compilation process

This results in a larger executable file, but it allows the program to run independently without relying on external libraries at runtime

Static linking offers faster execution because the entire library content is copied at compile time, and there is no need to query for unresolved symbols at runtime

Dynamic Linking:

    In dynamic linking, the names of the external libraries are copied into the final executable as unresolved symbols. The actual linking of these unresolved symbols occurs at runtime.
    This leads to smaller executable files, as the code of linked libraries does not need to be shipped with the executable file.
    Dynamic linking allows for easier updating and deployment, as the external libraries can be updated and recompiled to offer the latest changes to the programs

## Compiler flags are useful

There are a number of useful compiler flags and options to set when compiling C++. Here are some of them:

-Wall, -Werror, -Wextra, -Wpedantic and -pedantic are compiler flags.

There is also -O which enables compiler optimimization and -g which enables debugging symbols.

-march, -mtune and -mcpu and also -melf_i386 sets the architecture.

-m32 sets 32 bit but does not work in g++, it only works in gcc.  I have never tested it out in g++ or c++, or cc.

Valid values for the -march flag in GCC depend on the target architecture. For example, for x86-based systems, valid values include i386, i486, i586, i686, and x86-64.

## The linking process

The linker is a crucial part of the C++ compilation process, responsible for creating executable files by resolving linkage issues and combining object files. There are several linkers typically used in C++, including:

- GNU Linker (ld): This is the default linker for most C and C++ programs on Linux and other Unix-like systems. It is typically invoked indirectly by the compiler driver (e.g., gcc or g++).

- Microsoft Visual C++ Linker (link): This is the linker used with the Microsoft Visual C++ compiler on Windows. It takes object files and libraries as input and produces an executable or a DLL.

- Intel C++ Compiler Linker (xild): This is the linker used with the Intel C++ Compiler. It performs a similar function to other linkers, combining object files into an executable.

These linkers perform the essential task of combining object files and libraries to produce the final executable or library. They also handle tasks such as resolving external symbols, including debugging information, and supporting features like incremental linking and versioning

## Mistakes and common things to avoid doing in C++

Here are some common mistakes to avoid when writing C++ code:

- Incorrect use of "new" and "delete": Improper use of dynamic memory allocation and deallocation can lead to memory leaks and other issues

- Not understanding STL: Lack of understanding of the Standard Template Library (STL) can lead to errors, especially regarding iterator invalidation and thread safety

- Manual memory management: Manual memory management can result in memory leaks, dangling pointers, and other memory-related issues

- Not writing readable, maintainable code: Failing to use proper indentation, meaningful variable names, and comments can make the code difficult to understand and maintain

Ignoring best practices: Not following best practices such as writing unit tests, using static analysis tools, and embracing modern idioms can lead to lower quality code can quickly lead to technical debt you may not be able to escape from.

By being aware of these common mistakes and following best practices, you can write cleaner and more reliable C++ code.

## Overflows, overflows, overflows

In C++, an overflow occurs when a number exceeds the maximum value that the data type can hold. This can lead to unexpected behavior and errors in the program. For signed integers, overflow is undefined behavior, while for unsigned integers, it is well-defined and the value wraps around. One way to avoid integer overflows is to use larger data types, such as long long or int64_t, to accommodate larger values. Another approach is to write adequate unit tests to check for overflows and to avoid putting the code in a situation prone to overflows. Using 64-bit integers can also help prevent overflows. However, detecting and preventing overflows can be challenging, and integer overflow bugs in C and C++ programs are difficult to track down and may lead to fatal errors or exploitable vulnerabilities.

## Debugging C++

Debugging in C++ is a critical skill for identifying and fixing errors in code. There are several tools and techniques available
for debugging C++ code

Here are some tips and techniques for debugging C++ code:

GDB:

GDB is a command-line debugger for C and C++ programs. It allows you to run your program and stop it at any line, examine the contents of variables, and track down program crashes. To use GDB, you need to compile your program with the debug flag, which tells the compiler to insert debugging information the debugger will use.

Tips for Debugging C++:

 Use conditional breakpoints to suspend code execution when specific conditions are met.
 Use watchpoints to stop the program when a particular variable is modified.
 Pretty-print structures to make complex data structures easier to read.
 Time travel debugging allows you to step backward and forward in your program's execution to understand how a bug occurred
