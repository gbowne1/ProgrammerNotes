# package.json file

You can create your own `package.json` file.  Yes, running `npm init -y` or `npm init` will do it for you but it might be missing some fields, keys, properties and other things you might find useful, and unless you are creating a package to be listed on npmjs, I would suggest just making the file manually.

You can use this template to start with

Some things were meant to be only used for when you are publishing a package to npm (when you set private to "false") so you can just remove those.

Here's a step-by-step guide to creating a package.json file:

```json
{
 "homepage":"",
 "name": "name-string-goes-here",
 "version": "",
 "description": "",
 "scripts": {},
 "author": "",
 "license": "",
 "dependencies": {},
 "bugs": "",
 "repository": "",
 "contributors": [],
 "funding": "uri-goes-here",
 "files":[],
 "browser": "",
 "bin": "",
 "man": "",
 "config": {},
 "devDependencies": {},
 "peerDependencies": {},
 "optionalDependencies": {},
 "engines": {},
 "private": "true",
 "keywords": [],
 "main": "",
 "publishConfig": {},
 "types": "",
 "typings": "",
 "exports": "",
 "module": "",
 "unpkg": "",
 "style": "",
 "stylelint": {},
 "eslintConfig": {},
 "browserslist": "",
 "os": [],
 "cpu": [],
 "jest": "",
 "directories": {},
 "stlyelintIgnore": "",
 "eslintIgnore": "",
 "prettier":"",
 "commitlint": "",
 "lintstaged": "",
 "husky": ""
}
```

Notes:

 1. "name" must be a string longer than 1 character
 2. "exports" must be a file path pattern that will match the pattern of `"^\./"`
 3. "funding" must be a URI for the fund

You really won't need most of these for most projects unless you are going to publish to yarn, npm or pnpm.

The package.json file is essential for managing and installing packages. It lists the packages your project depends on, specifies the versions of a package that your project can use using semantic versioning rules, and makes your build reproducible, and therefore easier to share with other developers

If you expect to create many package.json files, and intend to use `npm init`, you can customize the questions asked and fields created during the init process so all the package.json files contain a standard set of information. In your home directory, you can create a file called .npm-init.js to customize the npm init questionnaire.

There are a number of these keys and properties that should be used in all or most package.json files, and I believe some are required.  From the research I have done, there is no particular order required.

"name":  This is the name of your package and it must be a string longer that 1 character in the double quotes.

"keywords":  This is recommended, especially if you list your package on npmjs

"version": The "version" in the package.json file is the version of the package.
The "version" field in the package.json file must be in the form x.x.x and follow the semantic versioning guidelines

"main": This the entry point filename for your program, library or application, usually app.js, index.js

"license": This should contain the license you are using.

"devDependencies": This section should only include any packages and their version numbers which are needed for development.

"dependencies": This section should include all of the packages required for your application to run, not including development packages.

"engines": This should be the nodejs version(s) required for your application to run.

"description": You should provide a very short description of your package or application here, especially if you are publishing to npmjs, pnpm, yarn.

"private": You should set this to true, unless you intend on publishing your package to npmjs.

## Package Versioning

In "dependencies" and "devDependencies" the version numbers should be listed in SemVer.
