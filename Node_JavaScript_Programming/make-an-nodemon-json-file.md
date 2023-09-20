# Create a nodemon.json file

Nodemon is a command-line interface (CLI) utility that helps in developing Node.js based applications by automatically restarting the node application when file changes in the directory are detected.

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
    "watchOptions": "",
    "ignore": ["src/**/*.test.js"],
    "delay": 1000,
    "execMap": {
      "js": "node --inspect"
    },
}
```

This is all the information I could find out about the file.
