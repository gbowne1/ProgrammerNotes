# Configuring ESLint to lint your JavaScript

Are you looking to maintain the quality of your JavaScript code with ease? ESLint is here to help!

This pluggable and configurable linter tool is designed to identify and report on patterns in JavaScript,
allowing you to catch potential issues and enforce coding standards. In this guide, we'll walk you through
the process of configuring ESLint for your project, so you can start writing cleaner and more consistent code.

What is ESLint? ESLint is an open source JavaScript linting utility that was originally created by
Nicholas C. Zakas in June 2013. It's a type of static analysis tool that is commonly used to find
problematic patterns or code that doesn’t adhere to certain style guidelines. With ESLint, you can
discover errors and enforce coding conventions without having to execute your JavaScript code, making
it an invaluable tool for maintaining code quality. Configuring ESLint To configure ESLint for your
project, you can start by creating a configuration file.

ESLint supports various file formats for configuration, including JavaScript, JSON, YAML, and even the
eslintConfig property in your package.json file.

For example, you can use a .eslintrc.js file to export an object containing your configuration, or a
 .eslintrc.json file to define the configuration structure.

ESLint is primarily designed for linting JavaScript. However, it can also be configured to support other
languages through parser options. By default, ESLint expects ECMAScript 5 syntax, but you can override
this setting to enable support for other ECMAScript versions and JSX using parser options

Besides the .eslintrc file, ESLint also recognizes the following files as configuration files:

- .eslintrc.js: This is a JavaScript file that exports an object containing your configuration.

- .eslintrc.cjs: Use this when running ESLint in JavaScript packages that specify "type":"module" in their package.json. Note that ESLint does not support ESM configuration at this time.

- .eslintrc.yaml or .eslintrc.yml: These are YAML files to define the configuration structure.

- .eslintrc.json: This is a JSON file to define the configuration structure. ESLint’s JSON files also allow JavaScript-style comments.

- package.json: You can create an eslintConfig property in your package.json file and define your configuration there. If there are multiple configuration files in the same directory, ESLint only uses one.

The priority order is as follows: .eslintrc.js, .eslintrc.cjs, .eslintrc.yaml, .eslintrc.yml, .eslintrc.json, package.json

These files provide flexibility in how you can define and manage your ESLint configurations.

As you gain familiarity with ESLint, You should build a baseline configuration and store the rather than just
rely on the defaults so that you can get to work easily on your project and store it somewhere handy so that
you can copy and paste it into your project.  If you work on various types of JavaScript projects and frameworks,
 you might even have several configurations you can rely on.

## Installing ESLint

Install the ESLint package in your project `npm install --save-dev eslint`

It should be available via Yarn or other npm-like package managers

## JavaScript example of configuration

Here's a quick example of a configuration file in JavaScript format:

```js
module.exports = {
  "extends": "eslint:recommended",
  "rules": {
    "indent": ["error", 2],
    "quotes": ["error", "single"],
    "semi": ["error", "always"],
  },
  "root": true,
  "parserOptions": {

  }
};
```

The docs for configuration are: [Config]<https://eslint.org/docs/latest/use/configure/rules>

## ESLint configuration keys and properties

"extends" - The "extends" key in an ESLint configuration file is used to extend the base configuration by adding additional rules or overriding the existing one

"rules" is the place where you will be adding the lint rules to your configuration.

"env": the "env" key is used to specify the environments for which the ESLint configuration is intended, like the "browser", "node", "commonjs" and "es6".

"plugins" are configurations for the plugins you have installed

"proccessor" - Specifies a preprocessor for the code, such as "prettier/recommended" to enable Prettier integration

"overrides" - The "overrides" key in an ESLint configuration file allows you to define configuration overrides for specific files, paths, or glob patterns

"parser" are configurations for the parser and choosing the parser you will be using.  "babel" is probably the most common parser.

"parserOptions" are options to configure the parser.

"globals" - Specifies additional global variables that are predefined. This can be useful for defining global variables that are not defined in the current file but are used elsewhere

"ignorePatterns" - Allows you to specify files and directories to ignore during the linting process.

"root" - Indicates that the current configuration file is the root configuration, and ESLint should stop looking for further configurations in parent directories

"workspaces" - This configuration is used in a monorepo setup to specify the workspaces to apply the ESLint configuration to.

"ecmaFeatures" - This is an object. This specifies support for ECMAScript (JavaScript) features like jsx and classes.

"ecmaVersion" - number value: A number representing the ECMAScript version to parse the code against (e.g., 2023)

"codeFrame" - This is a boolean value, true to include code frames, false to omit them

"settings" - Provides settings for ESLint to interpret code in specific contexts.

"react" - An object or a boolean, depending on where used in the configuration, enables ESLint's built-in rules for React applications.

"version" - This is a string and an optional property that can be used to specify an ESLint shareable config version.

"jest"- An object or a boolean, depending on where used in the configuration, enables rules specific to Jest testing environments.

"browser" - A boolean value, this enables rules for code running in a browser environment

"commonjs" - A boolean value, this nables rules for code using the CommonJS module system

"amd" -  Enables rules for code using the Asynchronous Module Definition (AMD) format.

"es6" - An object or boolean, Enables or configures rules for ECMAScript 6 (ES6) features.

"allowImportExportEverywhere" - This is a boolean value to allow imports and exports anywhere, false to restrict them to module top-level.

## Configurations

Common configurations in "rules" are, and they should be:

curly - Requires the use of curly braces for all control statements

quotes - Enforces the consistent use of either single, double, or backticks for string literals. It can be set to "single", "double", or "backtick" to enforce the corresponding style

semi - Enforces the use of semicolons at the end of statements. It can be set to "always" or "never" to require or disallow semicolons, respectively

indent - Enforces consistent indentation. It specifies the number of spaces for indentation and whether to use spaces or tabs

There are more configurations in "rules" that you can set.  Tailor these to your liking.  Add others when you need them.

## ESLint Plugins

There are plugins for ESLint. An ESLint plugin is an npm module that can contain a set of ESLint rules, configurations,
processors, and environments. These plugins often include custom rules and can be used to enforce a style guide and support
JavaScript extensions, libraries, and frameworks such as TypeScript, React, and Angular

Each plugin is an npm module with a name in the format of eslint-plugin-<plugin-name>, such as eslint-plugin-react and there
 are a number of others. Plugins can also provide additional environments, custom processors, and configurations.

You should be able to easily find a list of awesome ESLint plugins, configs, etc. on GitHub and the npmjs site.

If you are going to be using ESLint, I would suggest that you should install these packages:

- eslint-plugin-prettier
- eslint-plugin-react
- eslint-plugin-jest
- eslint-plugin-jsdoc
- eslint-plugin-mocha
- eslint-plugin-cypress
- eslint-plugin-babel
- eslint-webpack-plugin
- eslint-plugin-filenames
- eslint-plugin-markdown
- eslint-plugin-jsonc
- eslint-plugin-jsx-a11y
- eslint-plugin-safe-jsx

As for config.. install these packages:

- eslint-config-prettier (The config plugin for Prettier)
- eslint-config-airbnb-base
- eslint-config-airbnb
- eslint-config-standard (for standard JavaScript)
- eslint-config-react-app (the Create React App config) # Not Needed if you are not using Create React App
- eslint-config-google
- eslint-config-standard-react
- eslint-config-standard-jsx
- eslint-config-react

If you are doing React development, I would suggest installing both the plugin and config for React.  You can look up each one of these on
npmjs.com and find out what they do.  I would suggest only installing eslint-plugin-prettier, eslint-plugin-react, eslint-config-react and eslint-config-prettier when you are first starting out as a beginner.  You can add more.  The others may not be helpful to you, but you should be aware of them.

## Ignoring files

You can tell ESLint to ignore file parsing of any file you do not want ESLint to parse by using .eslintignore which has a format similar to a .gitignore file.
It has been suggested that you should ignore parsing of node_modules.

## Disabling ESLint rules

You can inline disable ESLint's rules when necessary.

use the // eslint-disable-rulename or /*eslint-disable-rulename*/

## ESLint in the Command Line

To run ESLint in the command line, two things can happen but most of the time all you will need to do is run `eslint --fix .` in whatever directory you are in.
