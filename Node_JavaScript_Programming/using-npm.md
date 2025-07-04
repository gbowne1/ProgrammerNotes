# Using npm

`npm outdated` -- Returns list of the outdated installed packages from your package.json file
`npm list` --
`npm ls` -- shows a list of installed packages.
`npm update` -- Updates the packages listed in package.json
`npm init` -- Initializes a new node.js project
`npm run <script_name>` -- runs whatever script is in 'scripts` in package.json
`npm cache clean --force` forces npm to clear its cache.
`npm ci` -- Installs dependencies directly from package-lock.json or npm-shrinkwrap.json, ignoring package.json
`npm audit` scans your project for known security vulnerabilities in your dependencies but no changes applied.
`npm audit fix`
`npm audit fix --force`
`npm version <new_version>` -- updates the semver version listing in your package.json to whatever <new_version> you specify.
`npm i <package_name` -- short version of npm install.
`npm install <package_name>` installs the package specified.
`npm install -D <package_name>` installs the package as a `devDependency` same as `--save-dev`
`npm install -g <package_name>` Installs a package globally, making it available across all your Node.js projects on your system
`npm uninstall <package_name>` removes a ppackage and its update from package.json
`npm view <package_name>`
`npm prune <package_name>`
`npm show` -- similar to npm view
`npm init -y` 
`npm publish`
`npm pack`
`npm dedupe`