# Configuring Prettier

Prettier is an opinionated code formatter that supports various languages. It enforces a consistent code style by parsing the code and reprinting it from scratch, taking the line length into account. It supports languages such as JavaScript (including experimental features), JSX, Angular, Vue, Flow, TypeScript, CSS, Less, SCSS, HTML, Ember/Handlebars, JSON, GraphQL, Markdown (including GFM and MDX v1).

To configure Prettier, you can use a "prettier" key in your package.json file, a .prettierrc file written in JSON or YAML, prettierrc.js or prettier.config.js file, or a .prettierrc.toml file, among other options.  According to recent Prettier documentation online, the current way to configure prettier is using a prettier.config.js file, but the other formats are still supported.

Prettier intentionally doesn’t support any kind of global configuration to ensure consistent behavior across different environments

Prettier also supports the use of plugins to add new languages or formatting rules. Official plugins include @prettier/plugin-php, @prettier/plugin-pug, @prettier/plugin-ruby, and many more. Community plugins are also available for a wide range of languages

If you're following along doing some Web Development, you will find this tool to help you format HTML, CSS, JavaScript.

## Installation

Prettier is a package installed to your project.  It's available on npmjs.com and can be installed to your project using `npm install prettier`

## Extensions, Plugins

There are some Prettier plugins and extensions for VSCode.

First of all, Open the VSCode settings and search for "Editor: Default Formatter" and set it to "esbenp.prettier-vscode". You can also do this to
your settings.json

There are two handy packages that are useful when using Prettier with ESLint. They are, `eslint-config-prettier` and `eslint-plugin-prettier`.

## Example configuration

Here is an example `.prettierrc` which you can code in JSON or YAML..

    {
      "singleQuote": true,
      "trailingComma": "all",
      "arrowParens": "always",
      "printWidth": 120,
      "tabWidth": 2,
      "semi": false,
      "endOfLine": "auto",
      "bracketSpacing": false,
      "jsxSingleQuote": true,
      "quoteProps": "as-needed",
      "htmlWhitespaceSensitivity": "css",
      "embeddedLanguageFormatting": "auto",
      "insertPragma": false,
      "proseWrap": "always",
      "ignorePath": ".prettierignore",
      "useTabs": false,
      "rangeStart": 0,
      "jsxBracketSameLine": true,    (using jsxBraketSameLine is deprecated)
      "requirePragma": true,
      "vueIndentScriptAndStyle": true,
      "parser": babel",
      "overrides": [
        {
          "files": "*.test.js",
          "options": {
            "printWidth": 80
          }
        }
      ],
      "plugins": ["prettier-plugin-foo"]
    }

I prefer JSON.  There could be more settings.  This covers most of them.  Most of the settings are or at least should be somewhat self-explanatory

Documentation on this file is here: <https://prettier.io/docs/en/configuration.html>

## Node.js configuration

Configuring Prettier for Node.js is slightly different however.
{
  "env": {
    "node": true,
    "es2021": true
  },
  "extends": "eslint:recommended"
}

## React configuration

Also, configuring Prettier for React is somewhat different from Node.js and setting up JavaScript linting.

{
  "env": {
    "browser": true,
    "es2021": true
  },
  "extends": [
    "eslint:recommended",
    "plugin:react/recommended"
  ]
}

## JavaScript configuration file

In order to make the file using JavaScript it needs to be wrapped in a module.exports like this example, and it needs to be name `.eslintrc.js`

     ```js
     module.exports = {
     // For JSON files
     overrides: [
      {
      files: '*.json',
      options: {
       tabWidth: 2,
       useTabs: false,
       trailingComma: 'none',
       arrowParens: 'avoid',
      },
      },
     ],
     // For JavaScript and JSX files
     semi: false,
     trailingComma: 'all',
     singleQuote: true,
     printWidth: 80,
     tabWidth: 2,
     useTabs: false,
     bracketSpacing: true,
     jsxBracketSameLine: false,
     arrowParens: 'avoid',
     parser: 'babel', // Use Babel parser for ES7 and JSX syntax
     };
     ```
