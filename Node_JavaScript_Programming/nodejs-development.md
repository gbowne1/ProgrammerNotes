# Node.js development notes

Node.js uses JavaScript.

Node.js is a JavaScript runtime environment that allows the execution of JavaScript on the server side and the handling of concurrent requests. It is used for managing the back-end of web applications, enabling a JavaScript stack. The Node.js ecosystem consists of a collection of libraries, frameworks, tools, and resources that support the Node.js runtime. This ecosystem provides essential components for building and running various types of applications. To use Node.js, developers can take advantage of its extensive package manager, npm, which allows them to install, share, and manage dependencies for their projects. Additionally, the Node.js ecosystem offers online resources for finding help, collaborating on development, and sharing contributions with the community

Node.js and JavaScript are related but serve different purposes. JavaScript is a scripting language
used for writing scripts on websites and is mostly used on the client-side. On the other hand,
Node.js is a JavaScript runtime environment that allows JavaScript code to run outside the browser,
primarily on the server-side. Here are the key differences between Node.js and JavaScript:

- JavaScript is a programming language used for writing scripts on websites, mostly on the client-side,
  while Node.js is a JavaScript runtime environment primarily used on the server-side

- JavaScript can only be run in the browsers, while Node.js allows JavaScript code to run outside the browser.

- JavaScript is capable of adding HTML and playing with the DOM, while Node.js does not have the capability to add HTML tags

- JavaScript is used in frontend development, while Node.js is used in server-side development

- JavaScript can run in any browser engine, while Node.js uses the V8 engine to parse and run JavaScript

- JavaScript is used with frameworks like RamdaJS and TypedJS, while Node.js uses modules like Lodash and Express, which are imported from npm.

Node.js is a JavaScript runtime environment for server-side development, allowing you to write JavaScript code that runs on the server instead of in the browser. It is popular for creating web applications, APIs, and microservices, and has several libraries that can't be found in JavaScript, making certain operations easier.

## Node.js ecosystem

Node.js has packages available for download by using a Node.js package manager like Yarn, NPM, PNPM and there may be others, but it is typical to use Yarn or NPM.  NPM is a Node.js Package Manager.

Node versions can be managed by using `nvm` package and calling it with the command line.  I would reccomend using the latest LTS (Long Term Support) version but also use the current version, if not installing it so it can be used.  It's easy to use nvm to switch versions.

Node.js can be used to build libraries, packages or applications for the browser. This can be done by importing and exporting modules using JavaScript.

Packages and libraries are usually published to NPM, Yarn or PNPM.

While there are some great tutorials, it can still be a bit confusing.  Many of these were published a number of years ago.

## Obtaining Node.js

Node.js can be downloaded from <https://nodejs.org>.  It's a fairly big ecosystem used by Web Developers.  Especially in a `full-stack` development environment.

## Node.js import and export of modules

There are several things going on here and should be considered.  ES5 and other Pre-ES6 JavaScript module imports used const and require();

To import modules in Node.js, you can use ES5 syntax, Here's how to do it:

    `var myModule = require('./myModule');`

it can also be done with a const

    `const myModule = require('')`

Modules need to be exported, so you do it like this:

ES5 syntax:

    // ES5 function
    function myFunction() {
      // function logic
    }

    module.exports = myFunction;
    // or
    // exports.myFunction = myFunction;

ES6/ES7 syntax:

    // ES6 function
    function myFunction() {
    // function logic
    }

    export default myFunction;
    // or
    // export { myFunction };

You also have the ability to use the function keyword in an export:

    export function myFunction(a, b) {
    return `${a} ${b}`;
    }

In both cases, the ./myModule does not have to explicitly export itself. Instead, it's the content of the module that is exported using the appropriate syntax.

In Node.js, both module.exports and exports are used to export values from a module. They essentially serve the same purpose, with exports being a reference to module.exports

However, it's generally recommended to use module.exports to avoid potential issues. When using both exports and module.exports in the same module file, it's best to stick to one convention for consistency.

The main difference between the two is that whatever you assign module.exports to is what's exported from your module. If you use both exports and module.exports in the same module, be cautious as it can lead to unexpected behavior

To import values from a module in Node.js, you can use the require function. For example, to import a module named mymodule, you would use const mymodule = require('./mymodule').

When working with ES modules in JavaScript, it's important to follow best practices to ensure smooth and efficient code. Here are some best practices:

    Avoid Mixing ES Modules and CommonJS: It's recommended to avoid mixing ES modules syntax and CommonJS syntax in your codebase. Stick to one syntax consistently throughout your project to prevent conflicts and compatibility issues

    Use Strict Mode: JavaScript modules operate in strict mode by default. Ensure that you abide by JavaScript's strict syntax rules to avoid potential issues

    Organize Code in Small, Reusable Units: ES modules are designed to organize code in small, reusable units that can be imported or exported in other modules. Follow this modular approach to keep your codebase clean and maintainable

Debugging Issues with Importing ES Modules in JavaScript

When debugging issues with importing ES modules in JavaScript, you can use the following approaches:

    Check for Syntax Errors: Ensure that your import and export statements are correctly written and that the file paths are accurate.

    Verify Module Type: Confirm that the module you are trying to import is indeed an ES module and is being treated as such by the environment.

    Use Browser Developer Tools: If you are working in a browser environment, utilize the developer tools to inspect network requests and console errors related to module imports.

Dynamic import is a feature introduced in ES2020, also known as ES11, which allows you to import ES modules dynamically. This feature is useful for loading modules on demand, potentially saving bandwidth. The syntax for dynamic import is as follows:

    async function loadMyModule() {
      const myModule = await import('./myModule.js');
      // ... use myModule
    }

    loadMyModule();

The import() function returns a promise for the module namespace object of the requested module, and the imported module can be assigned to a variable using async/await

Benefits of Using Dynamic Import in JavaScript

The benefits of using dynamic import in JavaScript include:

    On-demand module loading, which reduces the initial load time and improves application performance.

    Code splitting, allowing the browser to load only the necessary code for the current view, with the rest being loaded in the background or when needed.

    Greater syntactic flexibility as dynamic imports allow modules to be loaded conditionally or on demand, circumventing the syntactic rigidity of static import declarations

Dynamic import is a powerful feature that can significantly improve the performance and efficiency of JavaScript applications, especially in scenarios where on-demand loading of modules is required

Static imports, introduced in ES6, are used to import modules at the beginning of a program. The imported modules are loaded immediately, increasing the initial load time. On the other hand, dynamic imports, introduced in ES2020 (ES11), allow modules to be imported conditionally or on demand, reducing the initial load time and improving application performance. Dynamic imports are useful for code splitting, as they allow the browser to load only the necessary code for the current view, with the rest being loaded in the background or when needed

It also allows you to import read-only live bindings, which are exported by another module. The imported bindings are called live bindings because they are updated by the module that exported the binding, but cannot be re-assigned by the importing module. The static import declaration is used to import modules at the beginning of a program, and the imported modules are loaded immediately. The syntax for static import includes various forms such as importing default exports, importing all exports, and importing specific exports from a module

Common Mistakes to Avoid When Using ES Modules in JavaScript

Some common mistakes to avoid when using ES modules in JavaScript include:

    Mixing Module Formats: Avoid mixing ES modules with other module formats like CommonJS, AMD, or UMD to prevent confusion and compatibility issues

    Ignoring Strict Mode: Since ES modules operate in strict mode by default, failing to adhere to strict syntax rules can lead to unexpected behavior.

    Incorrect File Extensions: Ensure that ES modules use the .mjs file extension or are explicitly marked as modules to be properly recognized by the environment

By following these best practices and being mindful of common mistakes, you can effectively work with ES modules in JavaScript.

To use JavaScript strict mode, you can include the directive "use strict"; at the beginning of a script or a function. Here's an overview of what strict mode does and how to use it:

    Global Strict Mode:
        To enable strict mode globally, add "use strict"; at the beginning of a script. This applies strict mode to all code within the script.

    javascript
    "use strict";
    // Your JavaScript code here

Function-Level Strict Mode:

    You can also enable strict mode within a specific function by adding "use strict"; at the beginning of the function.

    function myFunction() {
        "use strict";
        // Strict mode is enabled for this function
    }

    Benefits of Strict Mode:
        Strict mode enforces stricter parsing and error handling, helping to write cleaner code and catch errors that might otherwise go unnoticed. It prevents the accidental creation of global variables and disallows certain potentially error-prone features of JavaScript.

By using strict mode, you can make your JavaScript code more resilient, secure, and maintainable.

By including the "use strict"; directive, you can opt in to the restricted variant of JavaScript, thereby implicitly opting out of "sloppy mode" and ensuring that your code is executed in strict mode, which offers various benefits in terms of code quality and error prevention

Common Errors When Using Strict Mode in JavaScript

Some common errors that can occur when using strict mode in JavaScript include:

    Accidental Global Variables: In strict mode, attempting to assign a value to an undeclared variable will result in a ReferenceError, preventing accidental creation of global variables

    Restricted Syntax: Strict mode prohibits the use of certain syntax that is likely to be defined in future versions of ECMAScript, which can lead to errors if that syntax is used

Availability of Strict Mode

Strict mode is not limited to Node.js and can be used in regular JavaScript. It is a feature of the JavaScript language itself, available in modern browsers and other JavaScript environments. By including the "use strict"; directive, you can opt in to the restricted variant of JavaScript, ensuring that your code is executed in strict mode

## Using Localhost with Node.js

Node.js can be used with localhost ports, and Node.js usually expexts port 3000 to be used. However, there are no strict port number requirements.

The localhost ports typically used with Node.js are commonly in the range of 3000 to 9000. However, the specific port number used is often based on developer preference and application requirements. For example, ports such as 3000, 5000, 8000, and 8080 are frequently used for local development. When deploying Node.js applications to the internet, they are often mapped to standard HTTP ports 80 and 443. Additionally, the use of environment variables, such as process.env.PORT, allows for dynamic port assignment, catering to both local and server environment

## Node.js environement and environement variables

Using the Node.js environment especially within a web application or framework typcially requires installing the npm package `dotenv` so that you can use a `.env` or `variable.env` file to pass certain things along like ports