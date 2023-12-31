# Create a jsconfig.json

The `jsconfig.json` file is used with Visual Studio Code. It is used to configure JavaScript projects in Visual Studio Code. The `jsconfig.json` file specifies the root files and options for the features provided by the JavaScript language service. The presence of a `jsconfig.json` file in a directory indicates that the directory is the root of a JavaScript project. The file itself lists the files belonging to the project as well as compiler options. . It specifies the root files and the options for the language features provided by the JavaScript language service. This file is specific to Visual Studio Code and JavaScript projects. It is primarily used to define a JavaScript project in VS Code and to exclude some files from showing up in IntelliSense.  This file essentially configures IntelliSense for JavaScript.

```json
{
  "compilerOptions": {
  "target": "es6",
  "module": "es6",
  "allowSyntheticDefaultImports": true,
  "baseUrl": ".",
  "paths": {
    "@/*": ["src/*"]
    }
  },
  "exclude":["node_modules"]
}
```

If you want to improve your developer experience when working in JavaScript with VS Code, adding a jsconfig.json file to your projects can significantly aid the JavaScript language service and improve the auto-complete and file browsing support in the VS Code IDE.

There is also a `tsconfig.json` file that configures Typescript in Visual Studio Code and it's structure is similar and does similar things, except for TypeScript

There is more documentation about this here: <https://code.visualstudio.com/docs/languages/jsconfig>

The tsconfig.json file is used to specify the root files and compiler options required to compile a TypeScript project. It is placed in the root of the project and is used to configure the TypeScript compiler. The presence of this file indicates that the directory is the root of a TypeScript project. The tsconfig.json file can include various options such as "compilerOptions" and "include" to customize the behavior of the TypeScript compiler. The "compilerOptions" property can be omitted, in which case the compiler’s defaults are used. This property contains the rules for the TypeScript compiler to enforce, such as "target" for specifying the ECMAScript version, "module" for specifying the module code generation, and "strictNullChecks" for enabling strict null checks. The "include" property specifies an array of filenames or patterns to include in the program, and these filenames are resolved relative to the directory containing the tsconfig.json file. This property is useful for specifying the files to be included in the program. The tsconfig.json file is useful for both individual work and team projects because it allows everyone to be on the same page about how to write their code. By including a tsconfig.json file, you can use the tsc command without any arguments in the terminal, making it easier to compile the TypeScript code.
