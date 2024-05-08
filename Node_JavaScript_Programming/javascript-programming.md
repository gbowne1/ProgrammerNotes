# Introduction to JavaScript Programming

JavaScript is a versatile and widely-used programming language that is essential for web development. It allows developers to create interactive and dynamic content on websites. Whether you are using a Mac, Linux, or Windows computer, JavaScript is a fundamental skill for anyone interested in programming.

## Understanding JavaScript

JavaScript, often abbreviated as JS, is a high-level, interpreted programming language that conforms to the ECMAScript specification. It is known for its flexibility and is primarily used to enhance the interactivity of web pages. JavaScript can be used on both the client-side and server-side of web development. The filename extension is `.js`.

One should be using the latest version of the ES standard for JavaScript, however there are 3 more common ones used in most projects and they are:
ES5, ES6 and ES7.

It's also very important to stick to one version of the syntax, unless you are trying to introduce backwards compatibility into your project.
This will make it maintainable. For instance, If you are going to use ES6 syntax in a JavaScript project, I would suggest sticking with ES6 syntax in each .js file instead of using snippits of, say, ES5, ES6 and ES7 code splattered all over a file you've created.

## JavaScript Standards, References and Styleguides

While not specifically important to being able to program in JavaScript, there are some styleguides issued for instance by Google.

The Google Styleguide is here <https://google.github.io/styleguide/jsguide.html> and is also published in other formats like XML.

The Standards are documented by ECMA International in a few places:

<https://262.ecma-international.org/5.1/>
<https://tc39.es/ecma262/>
<https://ecma-international.org/publications-and-standards/standards/ecma-262/>
<https://tc39.es/ecma262/multipage/>

There are JavaScript reference information at <https://developer.mozilla.org/en-US/docs/Web/JavaScript>.

They have a GitHub page at: <https://github.com/tc39> and <https://github.com/tc39/ecma262>

This post is really old but it has some good stuff in there: <https://stackoverflow.com/questions/912479/what-is-the-difference-between-javascript-and-ecmascript>

## ES5, ES6, and ES7

ECMAScript 5 (ES5) was the fifth edition of the ECMAScript standard, which JavaScript is based on. It introduced many new features and improvements to the language. ES6, also known as ECMAScript 2015, brought significant enhancements to JavaScript, including arrow functions, classes, and template literals. ES7, or ECMAScript 2016, and subsequent versions continued to add new features and improvements to the language

The differences between ES5, ES6, and ES7 in JavaScript can be summarized as follows:

ES5, Also known as ECMAScript 2009, released in 2009.

- Variables: Only one way to define variables using the var keyword.
- Performance: Lower performance compared to ES6.
- Object Manipulation: Time-consuming compared to ES6.
- Function Definition: Both function and return keywords are used to define a function.
- Support: Supports primitive data types such as string, number, boolean, null, and undefined.

ES6, Also known as ECMAScript 2015, released in 2015.

- Variables: Introduces two new ways to define variables: let and const.
- Performance: Higher performance than ES5.
- Object Manipulation: Less time-consuming compared to ES5.
- Function Definition: Introduces arrow functions, eliminating the need for the function keyword in some cases.
- Data Types: Adds a new primitive data type, symbol, for supporting unique values.

ES7, Also known as ECMAScript 2016.

- Features: Builds upon ES6 and introduces new features such as async/await, exponentiation operator, and more.
- Transpilation: Requires transpilation to convert ES7 code to ES5 for compatibility with browsers.
- Spread Operator: Introduces the spread operator (...) for merging arrays and objects.
- Template Literal: Introduces template literals using backticks (`) for easy string interpolation.

## Learning JavaScript

To start learning JavaScript, it's important to understand the basic syntax and concepts of the language. Once you have a good grasp of the fundamentals, you can explore the new features introduced in ES6 and ES7.

These include:

- Arrow functions
- Classes
- Template literals
- Async/await
- Spread and rest operators
- Destructuring assignments
- Promises
- Modules
- Operators
- Control Flow
- Arrays
- Functions
- Objects
- Prototypes

## JavaScript program / application entrypoint

The typical filenames for JavaScript program entry points are "index.js," "app.js," and "main.js".

These names are commonly used, but the choice is ultimately up to the developer. According to the
Google JavaScript Style Guide, file names for JavaScript must be all lowercase and may include
underscores or dashes, but no additional punctuation, and the filename extension must be .js.

Some JavaScript frameworks will require certain entrypoint filenames.  This is also common in
JavaScript frameworks, especially NodeJS and React.

## JavaScript file structure

The first few lines of a .js file, usually are a few lines of comment basically documenting in short
form what the file is, who created it, possibly a timestamp, filename and any other useful metadata

If you're going to use the `use strict` it will go next.  If you haven't used any comments above the 'use strict`
it can go as the first line of code. We will discuss `use strict` later on in this document.

This is my understanding of the order of how things are implemented in the `.js` files you create. In this top down
order:

1. Import statements
2. Variable declarations
3. Function declarations
4. Event listeners or other callbacks
5. Execution code

## Commenting your JavaScript Code

There are a couple different types of comments used in JavaScript

- `//` is a single line comment

- `/*  Comment */` is a multi line comment and can be spread over a few lines.

It's a great idea to comment the top of your file as well as the code you've written.  Code should be self-documenting which at least
for beginners may be not as easy as it seems.  It should usually be apparent to anyone reading your code, regaurdless of experience,
what your JavaScript code is doing.

There are things to help you out however, including JSDoc.

JSDoc is a markup language used to annotate JavaScript source code files. Programmers use comments containing JSDoc to add documentation describing the application programming interface of the code they're creating. This documentation is then processed by various tools to produce accessible formats like HTML and Rich Text Format. JSDoc's syntax and semantics are similar to those of the Javadoc scheme, which is used for documenting code written in Java. It is an open format and is widely used in the JavaScript community for documenting code and providing type information

## Filenames and Variable casing

What are the various filename case are used in javascript?

Well, in JavaScript, the common naming conventions for file names are all lowercase with the option to use underscores (_) or dashes (-)

This means that file names must be all lowercase and may include underscores or dashes, but no additional punctuation. For example, "my_file_name.js" or "my-file-name.js" are both valid file names in JavaScript. It is important to follow the convention that your project uses

There is no official, universal convention for naming JavaScript files, but it is crucial to be consistent in the convention you choose.

In JavaScript, there are several naming conventions used for variables, functions, classes, and file names. The two most common naming conventions for file names are PascalCase and kebab-case. PascalCase uses capital letters at the beginning of each word, without spaces or punctuation, while kebab-case uses all lowercase letters and hyphens between words. For example, "MyFile.js" is in PascalCase, and "my-file.js" is in kebab-case

For variables and functions, the most common convention is camelCase, which uses a lowercase letter at the beginning of the name and capital letters for each new word, without spaces or punctuation. For example, "myVariable" and "myFunction" are in camelCase.

It is important to be consistent and follow the convention that your project uses. It is also a good practice to use descriptive and meaningful names for variables, functions, classes, and files to improve code readability and maintainability

## A newer class and standard of JavaScript to note

There are a few revisions to the JavaScript standard post ES7.  To this writer, they are still not as common as ES5, ES6 and ES7.

ES2017 (ES8): Introduced string padding, Object.values/Object.entries, async functions, and shared memory

ES2018 (ES9): Added rest/spread properties, asynchronous iteration, Promise.finally(), and additions to RegExp

ES2019 (ES10): Included features like Array.prototype.flat(), Object.fromEntries, String.prototype.trimStart/trimEnd, and optional catch binding

ES2020 (ES11): Introduced the Nullish Coalescing Operator (??) and the Optional Chaining Operator (?.)

ES2021 (ES12): Added features like String.prototype.replaceAll, Promise.any, Logical Assignment Operators, and more.

ES2022 (ES13): This version introduced features such as class fields, import(), and extended numeric separators

## Functions and Classes

Here are examples of JavaScript functions and classes in ES5, ES6, and ES7:

ES5

    // Function in ES5
    var myFunction = function() {
    // function body
    };

    // Class in ES5 (using constructor function)
    function MyClass() {
      this.property = value;
      this.method = function() {
    // method body
     };
    }

ES6

    // Function in ES6 (using arrow function)
    const myFunction = () => {
    // function body
    };

    // Class in ES6
    class MyClass {
        constructor() {
        this.property = value;
    }
    method() {
    // method body
      }
    }

ES7

    // Function in ES7 (using async/await)
    const myFunction = async () => {
    // function body
    };

    // Class in ES7 (using class properties)
    class MyClass {
        property = value;
    method = () => {
    // method body
      };
    }

A function in JavaScript is a block of reusable code designed to perform a specific task. It is similar to a procedure and can take input and return an output. Functions are first-class objects in JavaScript, which means they can be passed to other functions, returned from functions, and assigned to variables and properties. There are several ways to define a function in JavaScript, including function declaration and function expression. JavaScript also has special syntaxes for defining arrow functions and methods. Functions can be invoked when an event occurs, called from JavaScript code, or automatically invoked. When a function reaches a return statement, it stops executing and returns a value. Functions are essential for writing concise, modular, reusable, and maintainable code in JavaScript

## JavaScript classes

Classes in JavaScript are a way to create objects using a template. They were introduced in ECMAScript 2015 (ES6) to provide a cleaner way to follow object-oriented programming patterns. JavaScript is a prototype-based language, and classes are built on prototypes but also have some syntax and semantics that are unique to classes. Here are some key points about classes in JavaScript:

Definition: Classes are defined using the class keyword, and they can be defined in two ways: a class expression or a class declaration.

- Constructor: The constructor method is a special method that is executed automatically when a new object is created from a class. It is used to initialize object properties.

- Methods: Class methods are created with the same syntax as object methods. They are defined within the class and can be called on objects created from the class.

- Static Methods and Fields: Classes can also have static methods and static fields, which are shared by all instances of the class.

- Private Properties: Private fields can be used to define private properties within a class, which are not accessible from outside the class.

Classes in JavaScript provide a more structured way to create and work with objects, and they are especially useful for implementing object-oriented programming concepts.

To use JavaScript classes, you can follow these steps:

Declaring a Class: Use the class keyword followed by the class name. Always add a constructor() method, which is used to initialize object properties.

Adding Methods: You can add any number of methods to the class using the same syntax as object methods.

Creating Objects: Once you have a class, you can use it to create objects by using the new keyword followed by the class name and any necessary arguments for the constructor.

Here's an example of a simple class in JavaScript:

    class Car {
      constructor(name, year) {
        this.name = name;
        this.year = year;
      }
      age() {
        const date = new Date();
        return date.getFullYear() - this.year;
      }
    }

    const myCar = new Car("Ford", 2014);console.log(myCar.age());

Classes in JavaScript were introduced in ECMAScript 2015 (ES6) to provide a cleaner way to follow object-oriented programming patterns. They are mainly an abstraction over the existing prototypical inheritance mechanism, and all patterns are convertible to prototype-based inheritance

It is widely accepted to use classes in JavaScript, and they are not deprecated

## Tabs, spaces, brackets, semicolons: JavaScript formatting

Usage of tabs and spaces in Javascript is talked about a lot.

The debate between using tabs and spaces in JavaScript (and other programming languages) has been ongoing for some time. Here are some key points from the search results

- Tabs: Tabs are considered by some to be the democratic way to handle white space, as anyone can set them up how they like them. They are also descriptive, telling the editor the amount of indentation that should be added

- Spaces: Spaces are displayed visually the same across any system, ensuring consistency. Different platforms and editors may display tabs with varying sizes, leading to potential issues with code alignment and readability

- Debate: The debate between tabs and spaces is not just about personal preference, but also about consistency, readability, and potential issues with code alignment and display across different platforms and editors

The choice between tabs and spaces is ultimately a matter of personal or team preference, as both can be used effectively. Consistency within a codebase is key, regardless of whether tabs or spaces are chosen for indentation

In JavaScript, particularly in ES5, ES6, and ES7, developers have the option to use tabs or spaces for indenting. The choice between tabs and spaces is a matter of personal preference and team conventions. Here are the options you can use:

    Tabs for indentation, spaces for alignment: This approach is considered flexible and allows for proper alignment. It involves using tabs for the indentation of code blocks and spaces for aligning elements within the code. This method is seen as a superior approach by some developers

    Spaces for both indentation and alignment: While using spaces for both indentation and alignment is acceptable, some developers find it less flexible compared to the tabs for indentation, spaces for alignment approach

    Tabs for both indentation and alignment: This approach is generally considered unacceptable as it can lead to issues and is not recommended

The choice between tabs and spaces is often influenced by the coding style guide of the organization or the project. For example, some style guides recommend two spaces for indentation, while others recommend using tabs or four spaces

It's important to maintain consistency within a codebase, and tools like ESLint can be used to enforce consistent indentation

Ultimately, the decision of whether to use tabs or spaces for indenting in JavaScript code should be based on the specific needs and conventions of the project or team.

## Linting JavaScript

The most common linter used for JavaScript is ESLint. A linter will help you keep your JavaScript code at least partially consistent.  Configuring the linter is beyond the scope of this text.

Linting JavaScript and TypeScript applications offers several benefits, including:

- Fewer Errors: Linters help identify and fix potential issues, such as code smells, before they manifest as critical problems in a production environment.

- Consistent and Readable Code: Linting encourages adherence to coding standards and best practices, leading to more maintainable and consistent code

- Early Error Detection: Linters catch errors early in the development process, making them easier and less costly to fix

- Promotion of Best Practices: They promote the use of coding standards and best practices within a development team, ensuring that the codebase is of high quality and follows established guidelines

- Identifying Security Vulnerabilities: Linting can help identify potential security vulnerabilities in the code, reducing the risk of a breach

While it may seem that the applications you are working on function without any problems despite the linting errors, using a linter is still recommended due to the aforementioned benefits. It not only helps in maintaining code quality but also fosters a culture of best practices and consistency.

Linting JavaScript code offers several benefits, including:

- Error Prevention: Linting helps identify and eliminate common errors and problematic code patterns, such as the use of undeclared variables, calls to undefined or deprecated functions, and potential syntax issues. This proactive approach reduces the likelihood of bugs and errors before the code is executed, leading to more reliable and stable applications

- Code Quality: By enforcing coding standards and best practices, linting contributes to the overall quality and readability of the code. It helps maintain a consistent coding style across the codebase, making the code easier to understand and maintain for the entire development team

- Improved Code Review: Linting facilitates more productive code review discussions by automatically flagging potential issues, allowing developers to focus on higher-level design and architecture considerations rather than getting bogged down in trivial, easily preventable error

- Enhanced Developer Experience: Linting encourages the writing of clean and well-structured code, which can lead to a more enjoyable and efficient development experience. Developers can benefit from immediate feedback on their code, leading to faster identification and resolution of issues

## Inline scripting

You can do JavaScript inline in a HTML file by using the `<script>` tag and it needs a closing `</script>` tag to be valid at the end of the script.

You can place this script tag at any point in the HTML, however, for some performance gains the script tag should be placed at the end of the html file, just before the closing `</body>` tag.

Other than this, it is a lot more maintainable to just include the JavaScript code in a separate file, with the extension `.js` and call it from the HTML file.

## Try and Catch

To use try...catch in different versions of JavaScript, you can follow these guidelines:

In ES5, you can use the traditional try...catch syntax to handle exceptions.

    try {
    // Code that may throw an exception
    } catch (error) {
    // Handling the exception
    }

In ES6 and later versions, the try...catch syntax remains the same. However, new features have been added to the language, but the basic try...catch functionality remains consistent across these versions

For example, in ES2019, optional catch binding was introduced, allowing you to omit the binding if you don't need to use the error object:

    try {
    // Code that may throw an exception
    } catch {
    // Handling the exception
    }

In summary, the try...catch syntax is consistent across ES5, ES6, and later versions of JavaScript, with some additional features introduced in the later versions

## Debugging JavaScript

The `console.log` statement should be used for debugging in the browser console for JavaScript by sending logged and logged error output to the console.

ESLint is also a good tool to be used for debugging JavaScript.

Chrome has built in DevTools for debugging

Node.js has its own debugger and debugger port for it's JavaScript. See the note about Node.js development

## JavaScript Arrays

In JavaScript, an array is a single variable used to store multiple elements of different data types. It is a special type of object that allows for the storage of a collection of items under a single variable name. Arrays in JavaScript are zero-indexed, resizable, and can contain a mix of different data types. They are not associative arrays, so their elements are accessed using nonnegative integers as indexes. Arrays in JavaScript use numbered indexes, and their elements can be accessed by referring to an index number. Here are some key points about JavaScript arrays:

JavaScript arrays are best described as arrays, although the typeof operator in JavaScript returns "object" for arrays

They are zero-indexed, meaning the first element of an array is at index 0, the second at index 1, and so on, with the last element at the value of the array's length property minus 12.

Arrays can be created using array literals or the JavaScript new keyword.

They are not associative in nature, and their elements are accessed using nonnegative integers as indexes.

JavaScript arrays can hold different types of data and are used to store multiple values under a single variable name

You can add elements to an array in JavaScript using the push(), unshift(), splice(), and concat() methods. Here's a brief overview of each method:

- push(): This method adds one or more elements to the end of an array.

    let array = [1, 2, 3];
    array.push(4, 5);
    // Output: [1, 2, 3, 4, 5]

- unshift(): It adds one or more elements to the beginning of an array.

    let array = [1, 2, 3];
    array.unshift(0);
    // Output: [0, 1, 2, 3]

- splice(): This method can add elements at any specified position in the array.

     let array = [1, 2, 3];
     array.splice(1, 0, 4, 5);
     // Output: [1, 4, 5, 2, 3]

- concat(): It creates a new array by merging existing arrays.

    let array1 = [1, 2, 3];
    let array2 = [4, 5];
    let newArray = array1.concat(array2);
    // Output: [1, 2, 3, 4, 5]

Removing Elements from an Array in JavaScript

To remove elements from an array in JavaScript, you can use the pop(), shift(), splice(), or filter() methods. Here's a brief overview of each method:

- pop(): This method removes the last element from an array.
- shift(): It removes the first element from an array.
- splice(): This method can remove elements from any specified position in the array.
- filter(): It creates a new array with elements that pass the test implemented by the provided function.

Looping Through an Array in JavaScript

You can loop through an array in JavaScript using various methods such as for loop, forEach(), for...of loop, and map() method. Here's a brief overview of each method:

`for` loop:

    for (let i = 0; i < array.length; i++) {
        // Access each element using array[i]
    }

`forEach()`:

    array.forEach(function(element) {
    // Access each element using element
    });

`for...of` loop:

    for (let element of array) {
    // Access each element using element
    }

`map()`:

    let newArray = array.map(function(element) {
    // Perform operations on each element and return the result
    });

These methods provide flexibility in adding, removing, and iterating through elements in JavaScript arrays

To remove all elements from an array in JavaScript, you can set the array's length to 0 or use the splice() method. Here's how to do it:

- Setting the Array's Length to 0:

    let array = [1, 2, 3, 4, 5];
    array.length = 0;
    // Output: []

- splice() Method:

    let array = [1, 2, 3, 4, 5];
    array.splice(0, array.length);
    // Output: []

You can check if an element exists in an array in JavaScript using the includes() method or the indexOf() method. Here's how to do it:

- includes() Method:

    let array = [1, 2, 3, 4, 5];
    array.includes(3);
    // Output: true

- indexOf() Method:

    let array = [1, 2, 3, 4, 5];
    array.indexOf(3) !== -1;
    // Output: true

You can sort an array in JavaScript using the sort() method. By default, the sort() method sorts the elements as strings in alphabetical and ascending order. Here's how to use it:

    const array = [3, 1, 4, 1, 5];
    array.sort((a, b) => a - b);
    // Output: [1, 1, 3, 4, 5]

The sort() method can be customized to sort elements in a different order, such as descending order, by providing a compare function

These methods provide a way to remove elements, check for the existence of elements, and sort arrays in JavaScript.

To remove duplicates from an array in JavaScript, you can use the filter() method in combination with the indexOf() method. Here's how to do it:

    let array = [1, 2, 2, 3, 4, 4, 5];
      let uniqueArray = array.filter((value, index, self) => {
      return self.indexOf(value) === index;
    });
    // Output: [1, 2, 3, 4, 5]

This code creates a new array by filtering out duplicate elements from the original array.

You can reverse the elements of an array in JavaScript using the reverse() method. Here's an example:

    let array = [1, 2, 3, 4, 5];
    array.reverse();
    // Output: [5, 4, 3, 2, 1]

The reverse() method changes the original array by reversing its elements in place.

There are multiple ways to shuffle an array in JavaScript. One common approach is to use the Fisher-Yates algorithm. Here's an example of shuffling an array using this algorithm:

    function shuffleArray(array) {
      for (let i = array.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [array[i], array[j]] = [array[j], array[i]];
      }
      return array;
    }

    let array = [1, 2, 3, 4, 5];
    let shuffledArray = shuffleArray(array);
    // Output: A shuffled version of the original array

The Fisher-Yates algorithm provides a truly random shuffle of the array elements

These methods offer effective ways to remove duplicates, reverse, and shuffle arrays in JavaScript.

Here are the various methods to remove duplicates from an array in JavaScript:

Using Set Object

You can use the Set object to remove duplicates from an array in JavaScript. Here's an example:

    let array = [1, 2, 2, 3, 4, 4, 5];
    let uniqueArray = [...new Set(array)];
    // Output: [1, 2, 3, 4, 5]

The Set object automatically removes duplicate values, providing a simple and efficient way to obtain the unique elements of an array.

Using Filter Method

The filter() method can also be used to remove duplicates from an array. Here's an example:

    let array = [1, 2, 2, 3, 4, 4, 5];
    let uniqueArray = array.filter((value, index) => array.indexOf(value) === index);
    // Output: [1, 2, 3, 4, 5]

The filter() method creates a new array of elements that pass the condition provided, effectively removing duplicates.
Using Reduce Method

The reduce() method can be employed to remove duplicates from an array. Here's an example:

    let array = [1, 2, 2, 3, 4, 4, 5];
    let uniqueArray = array.reduce((accumulator, currentValue) => {
      if (!accumulator.includes(currentValue)) {
        accumulator.push(currentValue);
      }
      return accumulator;
    }, []);
    // Output: [1, 2, 3, 4, 5]

The reduce() method is used to reduce the elements of the array and combine them into a final array based on a reducer function. These methods provide different approaches to removing duplicates from an array in JavaScript

The main difference between using Set and Filter to remove duplicates from an array in JavaScript lies in the approach and the resulting output. Here's a brief comparison:

    Using Set:
        The Set object automatically removes duplicate values from an array, providing a simple and efficient way to obtain the unique elements of the array.
        The output is a Set, which needs to be converted back to an array using the spread operator or the Array.from method.
        The Set approach is concise and directly handles the removal of duplicates without the need for additional conditions.
    Using Filter:
        The filter() method creates a new array of elements that pass the condition provided, effectively removing duplicates.
        The output is an array containing the unique elements that satisfy the condition specified in the filter() method.
        The filter() approach requires the explicit definition of the condition for removing duplicates, which involves comparing the index of the current element with the index of its first occurrence in the array.

    The Set approach provides a more direct and concise method for removing duplicates, while the Filter approach offers more flexibility in defining the condition for removing duplicates.

Removing Duplicates from an Array of Objects in JavaScript Using Set Object

You can remove duplicates from an array of objects in JavaScript using the Set object. Here's an example:

    let arrayOfObjects = [{id: 1, name: 'John'}, {id: 2, name: 'Jane'}, {id: 1, name: 'John'}];
    let uniqueArray = Array.from(new Set(arrayOfObjects.map(obj => JSON.stringify(obj)))).map(str => JSON.parse(str));
    // Output: [{id: 1, name: 'John'}, {id: 2, name: 'Jane'}]

This code uses the JSON.stringify method to convert each object to a string, then leverages the Set object to remove duplicates based on the string representation, and finally converts the unique strings back to objects.

Removing Duplicates from an Array of Objects in JavaScript Using Filter Method

You can also remove duplicates from an array of objects in JavaScript using the filter() method. Here's an example:

    let arrayOfObjects = [{id: 1, name: 'John'}, {id: 2, name: 'Jane'}, {id: 1, name: 'John'}];
    let uniqueArray = arrayOfObjects.filter((obj, index, self) =>
       index === self.findIndex((t) => (t.id === obj.id && t.name === obj.name))
    );
    // Output: [{id: 1, name: 'John'}, {id: 2, name: 'Jane'}]

This code uses the filter() method in combination with the findIndex() method to create a new array containing only the first occurrence of each unique object. The Set object and the filter() method provide effective ways to remove duplicates from an array of objects in JavaScript, each with its own advantages and considerations

## Using Async and Await

To use async and await in JavaScript, you can follow these steps:

Declare an Async Function: Use the async keyword before a function to declare it as an async function. This means the function always returns a promise

For example:

    async function myFunction() {
      return "Hello";
    }

Use the Await Keyword: Inside an async function, you can use the await keyword before a call to a function that returns a promise. This makes the code wait until the promise is resolved before continuing. For example:

    let result = await myPromise;

Error Handling: You can use try...catch blocks to handle errors when using async and await.

To handle errors when using async and await in JavaScript, you can use the try...catch block. Here's how you can do it:

    async function myFunction() {
      try {
        let result = await someAsyncTask();
        // Code to handle the result
      } catch (error) {
        // Code to handle the error
      }
    }

This allows you to catch and handle any errors that occur during the execution of the await-ed promise. As for the second part of your question, yes, async and await can be used with promises in JavaScript. The await keyword is used to wait for a promise to resolve, and it can only be used inside an async function. When used together, they provide a more readable and maintainable way to work with promises.

## Other different types of JavaScript files

Note: Please see the included note about NodeJS Development </ProgrammerNotes/Node_JavaScript_Programming/nodejs-development.md>

- `.cjs` file extension

  This is for CommonJS. CommonJS is a project that aims to standardize the module ecosystem for JavaScript outside of web browsers, such as on web servers or native desktop applications. It provides a specification for how modules should work and is widely used for server-side JavaScript with Node.js. CommonJS can be recognized by the use of the require() function and module.exports, while ES modules use import and export statements for similar functionality. The .cjs file extension is associated with CommonJS code, which is intended to allow JavaScript to be used in environments beyond a frontend web browser. It also allows JavaScript to be used in environments beyond a frontend web browser
  CommonJS is a module system for JavaScript used in server-side environments like Node.js.

- `.mjs` file extension

  The .mjs file extension is used to indicate that a JavaScript file uses the ECMAScript module format, providing a standardized way to organize and share JavaScript code across multiple files and projects. ES6 modules, which are denoted by the .mjs extension, offer several advantages over traditional .js files, including native support for ES6 modules, a clear distinction between modules and regular scripts, and improved compatibility with bundlers and build tools

  The .mjs file extension is commonly used in Node.js for ECMAScript modules, providing a standardized way to organize and share JavaScript code across multiple files and projects. Some common use cases for .mjs files in Node.js include:

  Native Support for ES6 Modules: The .mjs file extension leverages the native support for ES6 modules in modern JavaScript runtimes, allowing the use of the import and export keywords to define and use modules without the need for additional tools or transpilation

  Clear Distinction Between Modules and Scripts: The use of .mjs file extension helps differentiate between modules and regular scripts, enabling developers to quickly identify and work with modules in their projects

  Improved Compatibility with Bundlers and Build Tools: As the new module system gains popularity, bundlers and build tools have started to adopt native ES6 module support. Using the .mjs file extension ensures better compatibility with these tools, allowing for seamless integration into existing development workflows

- `.ejs` file extension

  EJS, or Embedded JavaScript, is a simple templating language that allows the generation of HTML markup with plain JavaScript. It is commonly used as a template engine in Node.js to create HTML templates with minimal code and to inject data into an HTML template on the client side, producing the final HTML. EJS enables the embedding of JavaScript into HTML pages, and it is often used with Express, a web application framework for Node.js. EJS files typically use the .ejs file extension. To use EJS in a Node.js project, the EJS package can be installed via npm, and the templating engine can be set up with Express. EJS is known for its ease of use, as it allows the direct use of JavaScript to generate the desired HTML output. It also provides features such as partials and the ability to pass variables to views, making it a powerful tool for building web applications

## JavaScript Promises

JavaScript promises are objects that represent the eventual completion or failure of an asynchronous operation. They were introduced as part of ES6 to simplify working with callbacks and make the syntax more manageable. A promise can be in one of three states: pending, fulfilled, or rejected. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason, enabling asynchronous methods to return values like synchronous methods. Promises are created using the new Promise syntax, and they provide a robust way to wrap the result of asynchronous work, overcoming the problem of deeply nested callbacks

To create a promise, you can use the following syntax:

    let promise = new Promise(function(resolve, reject) {
      // Perform an asynchronous operation and then either resolve or reject the promise
    });

Promises also support chaining, which allows you to synchronize multiple asynchronous calls. Additionally, the Promise API provides static methods such as Promise.resolve, Promise.reject, Promise.all, and Promise.race to work with promises more effectively.

## Destructuring in JavaScript

Destructuring in JavaScript allows you to extract values from arrays or properties from objects into distinct variables. It's available in ES6 and later versions. Here's a summary of how to do destructuring in ES6, and ES7, as well as the types of things that can be destructured:

In ES5, there is no direct way to destructure objects or arrays.

In ES6, you can destructure arrays and objects using the following syntax:
Array Destructuring

    const [x, y] = [1, 2];

Object Destructuring

    const { a, b } = { a: 1, b: 2 };

ES7 doesn't introduce any new features related to destructuring.

Types of Things that Can be Destructured

- Arrays
- Objects
- Computed object property names
- Invalid JavaScript identifier as a property name
- Destructuring primitive values, which will be wrapped into the corresponding wrapper object

## JavaScript Keywords

I believe this list of JavaScript keywords is complete.

await, break, case, catch, class, const, continue, debugger, default, delete, do, else, enum, export
extends. false, finally, for, function, if, implements, import, in, instanceof, interface, let, new
null, package, private, protected, public. return, super, switch, static, this, throw, try, true
typeof, var, void, while, with, yield, abstract, arguments, boolean, byte, char, double, enum, eval,
export, final, float, goto, implements, import, int, interface, long, native, package, private, protected
public, short, static, synchronized, throws, transient, volatile

## JavaScript Identifiers

Here is a list of rules for JavaScript identifiers:

- An identifier must start with a letter, underscore (_), or dollar sign ($).
- Subsequent characters can be letters, digits, underscores, or dollar signs.
- Identifiers are case-sensitive.
- Identifiers cannot be the same as JavaScript keywords or reserved words.

For example, valid identifiers include myVar, _test, and $result. Invalid identifiers include break, 1test, and new

These rules define the naming conventions for variables, functions, classes, and other entities in JavaScript.

Some examples of JavaScript identifiers include:

- Variable names: myVar, count, totalAmount
- Function names: calculateTotal, validateInput
- Constant names: PI, MAX_SIZE
- Property names: user.name, order.totalAmount

How JavaScript Identifiers Are Used in Code:

JavaScript identifiers are used to name variables, functions, constants, properties, and other elements in a program. They help in identifying and referencing these program entities throughout the code. For example, in the statement let myVar = 10;, myVar is an identifier for a variable

Difference Between a Variable and an Identifier in JavaScript:

In JavaScript, an identifier is the name given to a variable, function, or other program entity, while a variable is a storage location associated with an identifier. For example, in the statement let myVar = 10;, myVar is the identifier, and it is associated with the variable that stores the value 10

Best Practices for Naming JavaScript Identifiers:

When naming JavaScript identifiers, it's important to follow these best practices:

- Use descriptive names that indicate the purpose of the identifier, such as totalPrice or calculateArea.
- Start with a letter, underscore (_), or dollar sign ($).
- Use camelCase for variable and function names, and PascalCase for class names.
- Avoid using single character names, except for simple loop counters.
- Be consistent with naming conventions throughout your codebase

Declaration and Initialization of JavaScript Identifiers
JavaScript identifiers are declared and initialized as follows:

- Declaration: Use the let, const, or var keyword to declare a variable, followed by the identifier name. For example, let myVar;.

- Initialization: Assign a value to the variable using the assignment operator (=). For example, myVar = 10; or let myVar = 10;
  for declaration  and initialization in a single step

Scope of a JavaScript Identifier:

The scope of a JavaScript identifier refers to the region of the code where the identifier is accessible. In JavaScript, the scope of an identifier is determined by where it is declared. There are three types of scope:

- Global scope: Identifiers declared outside of any function or block have global scope and are accessible throughout the code.
- Local scope: Identifiers declared within a function or block have local scope and are only accessible within that function or block.
- Block scope: Identifiers declared with let and const have block scope, meaning they are only accessible within the block where they are defined
