# Webpack and Babel.js

There are a few things that you should know about

## Babel.js

What is Babel?

Babel, also known as Babel.js, is a free and open-source JavaScript transcompiler that is primarily used to convert ECMAScript 2015+ code into a backward-compatible version of JavaScript that can be run by current and older browsers or environments

It allows developers to take advantage of the newest features of the language and to use new JavaScript language features by converting their source code into versions of JavaScript that a web browser can process

Babel can also be used to compile TypeScript into JavaScript, but in this case you really should just write TypeScript.

The toolchain can transform syntax, polyfill features missing in the target environment, perform source code transformations, and more

Babel has support for the latest version of JavaScript through syntax transformers, allowing developers to use new syntax without waiting for browser support

It is widely used in the industry and has a large community of contributors and sponsors

The Babel toolchain includes various tools such as @babel/cli, @babel/core, and @babel/preset-env, which make it easy to use Babel for transforming and polyfilling JavaScript code

Babel is particularly useful for ensuring that modern JavaScript code can run on older browsers and environments, making it an essential tool for web developers who need to support a wide range of platforms

## Webpack

Webpack is a highly extensible and configurable static module bundler for JavaScript applications. It goes through your application from a root entry point, builds a dependency graph, and produces optimized bundles of the combined modules.

Webpack's configuration file is a JavaScript file that exports a webpack configuration, which is then processed by webpack based on its defined properties

It is used to bundle JavaScript files for usage in a browser and can also transform, bundle, or package any resource or asset

Some of its use cases include separate builds per page, creating a components library as a container, and dynamic dependency graphs in a multi-page application

Webpack configuration files are written in JavaScript and can be split into smaller files for loaders, plugins, and other options

The configuration file is a JavaScript object that configures one of Webpack's options

It is commonly defined in a top-level webpack.config.js file, but it can also be passed as a parameter to Webpack's Node.js API

If you need to create a configuration for production in a separate file, you can do so by specifying the config file to use
