# Configuring Prettier

Prettier is an opinionated code formatter that supports various languages. It enforces a consistent code style by parsing the code and reprinting it from scratch, taking the line length into account. It supports languages such as JavaScript (including experimental features), JSX, Angular, Vue, Flow, TypeScript, CSS, Less, SCSS, HTML, Ember/Handlebars, JSON, GraphQL, Markdown (including GFM and MDX v1), and YAML

To configure Prettier, you can use a "prettier" key in your package.json file, a .prettierrc file written in JSON or YAML, a .prettierrc, .prettierrc.js or prettier.config.js file, or a .prettierrc.toml file, among other options.

Prettier intentionally doesn’t support any kind of global configuration to ensure consistent behavior across different environments

Prettier also supports the use of plugins to add new languages or formatting rules. Official plugins include @prettier/plugin-php, @prettier/plugin-pug, @prettier/plugin-ruby, and many more. Community plugins are also available for a wide range of languages
