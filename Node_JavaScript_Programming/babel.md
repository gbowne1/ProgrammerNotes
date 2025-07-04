I never quite figure out how to use Babel so here it goes as best as I am able to describe.
From what I understand, Babel is basically a JavaScript Compiler/Transpiler.  It's basically so that 
the code you wrote runs in older browsers.

Babel 5 prior to 2015, required `babel-core` and packages were not namespaced like `@babel`
It also used preset packages like babel-preset-*.

Babel 6 in 2015, started to change things and needed `.babelrc`

Babel 7 you can use `.babelrc.js` or `babel.config.js` and packages are namespaced/scoped as @babel.
This now uses `@babel/preset-env`

.babelrc is json only and only used with Babel 5

.babelrc.js and babel.config.js need to have `module.exports = { . . . };` syntax.