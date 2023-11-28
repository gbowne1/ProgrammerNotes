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

## C++ Keywords and Operators

In C++, the keywords "for," "while," "if," "new," "else," "switch," "case," "delete," "continue," "break," "default," and "return" are used for various control flow and memory management purposes.

"for" keyword is used to create a loop that consists of three optional parts: initialization, condition, and increment/decrement.
"while" keyword is used to create a loop that executes a block of code as long as the specified condition is true.
"if" keyword is used to execute a block of code if a specified condition is true.
"new" keyword is used to dynamically allocate memory for a variable of a given type.
"else" keyword is used to execute a block of code if the same condition is false.
"switch" keyword is used to select one of many code blocks to be executed.
"case" keyword is used within a "switch" statement to specify a block of code to be executed.
"delete" keyword is used to deallocate memory that was previously allocated using "new."
"continue" keyword is is used to skip the rest of the code inside a loop for the current iteration and continue to the next iteration.
"break" keyword is used to terminate the loop or switch statement and transfer control to the statement immediately following the loop or switch.
"default" keyword is used within a "switch" statement to specify the code to be executed if no case matches.
"return" keyword is used to exit a function and return a value to the caller

1. 'switch`, `case`, `break` and `default` are typically used together.
2. `while` sets up a loop condition.
3. `if` and `else` is typically used together in a if-else statement to do conditional checking
4.

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

Example void:

```cpp


```


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

In this first example, "season" is the name of the enumeration, and "spring," "summer," "autumn," and "winter" are the values of type "season." By default, "spring" is 0, "summer" is 1, and so on. You can also change the default value of an enum element during declaration if necessary2
. Enums are used to restrict data to certain values and provide it in a human-readable format. They are vital for any project where you need to work with a fixed set of values, such as game development or managing states of objects