# Node servers

1. go to the Node.js website Download and install the LTS version (recommended for most users).

2. Verify with `node -v` and `npm -v`

3. Make a project directory

4. `npm init -y`

5. To create a Node.js server you need a package called `express`. install it with `npm install express` or `npm i express`

5. create a `server.js` file. use `touch` or whatever.

6. Stuff needs to be kept secret so, create a .env file and also `npm i dotenv` or `npm install dotenv`
the most common use for this is secure keys and also port number for the server by using the PORT variable .

7. app.use() app.post() app.get() are all express methods 

8. in order to use express in your `server.js` file you need to require it and use it by

```js
const express = require('express');
const app = express();
```

Keep in mind this is the ES5/ES6 way which is still accepted even though ES7+ uses import.
