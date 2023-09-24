# package.json file

You can create your own `package.json` file.  Yes, running `npm init -y` or `npm init` will do it for you but it might be missing some fields, keys, properties and other things you might find useful.

You can use this template.

Some things were meant to be only used for when you are publishing a package to npm (when you set private to "false").

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
 2. "exports" must be a file path pattern that will match the pattern of "^\./".
 3. "funding" must be a URI for the fund

You really won't need most of these for most projects unless you are going to publish to yarn, npm or pnpm
