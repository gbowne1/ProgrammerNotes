# MongoDB Database connection

Here is how to connect to a MongoDB database.

I use MongoDB on the command line, not MongoDB Atlas or MongoDB Compass.

The MongoDB localhost port is: 27017

To get MongoDB  the import is `const mongoose = require('mongoose');`

In NodeJS and ExpressJS:

```js
const mongoose = require('mongoose');
const mongoURI = 'mongodb://localhost:27017/codebooker';

 mongoose.connect(mongoURI, {
    useNewUrlParser: true,
    useUnifiedTopology: true,
    useCreateIndex: true,
    useFindAndModify: false
 }).then(() => {
    console.log('Connected to MongoDB');
 }).catch((err) => {
    console.log('Failed to connect to MongoDB', err);
 });
```

Here are some of the MongoDB show commands:

- show dbs: This command is used to display a list of all available databases.
- show collections: This command is used to display a list of all collections in the current database.
- show users: This command is used to display a list of all users for the current database.
- show roles: This command is used to display a list of all roles for the current database.
- show profile: This command is used to display system.profile information.
- show logs: This command is used to display recent log messages.
- show databases: This command is used to display the current database being used2

Finding information in collections is basically

db.collectioname.findOne()
