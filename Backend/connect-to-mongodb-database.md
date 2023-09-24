
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
