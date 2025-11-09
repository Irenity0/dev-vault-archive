```javascript
const jwt = require('jsonwebtoken');

// Create a JWT when the user logs in
app.post('/login', (req, res) => {
  const username = req.body.username;
  const user = { id: 1, username: username };
  const token = jwt.sign(user, 'secretkey', { expiresIn: '1h' });
  res.json({ token });
});

// Middleware to verify JWT
app.get('/protected', (req, res) => {
  const token = req.header('Authorization').replace('Bearer ', '');
  jwt.verify(token, 'secretkey', (err, user) => {
    if (err) return res.sendStatus(403); // Forbidden
    res.send('Protected content');
  });
});
```
