# Express Server

This is the code that would create a basic ExpressJS server, which connects to a MongoDB database

```js
const express = require('express');
const mongoose = require('mongoose');
const cors = require('cors');

const app = express();

// Connect to MongoDB
mongoose.connect('mongodb://localhost/my-database', {
  useNewUrlParser: true,
  useUnifiedTopology: true,
});

// Define routes and middleware
app.use(cors());
app.use(express.json());
app.use('/api/users', require('./routes/users'));

// Start the server
const PORT = process.env.PORT || 5000;
app.listen(PORT, () => console.log(`Server started on port ${PORT}`));
```
