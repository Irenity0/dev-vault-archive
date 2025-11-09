```javascript
const express = require('express');
const app = express();
const port = 3000;

// Middleware to parse incoming JSON requests
app.use(express.json());

// Route to handle GET request
app.get('/', (req, res) => {
  res.send('Welcome to Express!');
});

// Route to handle POST request
app.post('/submit', (req, res) => {
  res.send(`Received data: ${JSON.stringify(req.body)}`);
});

// Start the server
app.listen(port, () => {
  console.log(`Server running at http://localhost:${port}`);
});
```
