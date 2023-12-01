# Create a nodemon.json file

Nodemon is a command-line interface (CLI) utility that helps in developing Node.js based applications by automatically restarting the node application when file changes in the directory are detected.

`nodemon.json` is used a configuration file used to customize the behavior of Nodemon, a utility for Node.js applications that monitors for changes and automatically restarts the server. It allows you to specify options such as which files to watch, which files to ignore, and the delay before restarting the server. The file is typically named nodemon.json and can be located in the current working directory or in your home directory. Command line arguments always override the settings in the nodemon.json file.

To install nodemon, you can use npm (Node Package Manager) by running the following command:

```bash
npm install -g nodemon
```

This will install nodemon globally on your system, allowing you to use it from the command line.
Some alternatives to nodemon include forever, gulp, Grunt, LiveReload, and PM2. These are popular
tools for managing Node.js applications and providing similar functionality to nodemon

If you are considering alternatives to nodemon, it's important to evaluate your specific requirements
and choose the tool that best fits your needs. Each tool has its own strengths and weaknesses, so it's
worth exploring and experimenting with different options to find the best fit for your project. For more
details, you can refer to the official documentation of nodemon and online resources that compare
different tools for managing Node.js applications.

To use nodemon, you need to install it either globally or locally on your project using npm or yarn.

Here is the `nodemon.json` File Structure:

```json
{
 "watch": ["src/client", "src/server"],
    "ext": "js,json",
    "exec": "node src/server/server.js",
    "restartDelay": "",
    "args": "",
    "nodeArgs": "",
    "verbose":  true,
    "watch": "",
    "watchOptions": "",
    "ignore": ["src/**/*.test.js"],
    "delay": 1000,
    "execMap": {
      "js": "node --inspect"
    },
}
```

This is all the information I could find out about the file.
