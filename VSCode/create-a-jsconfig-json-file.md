# Create a jsconfig.json

The `jsconfig.json` file is used with Visual Studio Code. It is used to configure JavaScript projects in Visual Studio Code. The `jsconfig.json` file specifies the root files and options for the features provided by the JavaScript language service. The presence of a `jsconfig.json` file in a directory indicates that the directory is the root of a JavaScript project. The file itself lists the files belonging to the project as well as compiler options.

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

There is also a `tsconfig.json` file that configures Typescript in Visual Studio Code and it's structure is similar
