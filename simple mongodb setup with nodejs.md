```javascript
const { MongoClient } = require('mongodb');

// Connection URL
const url = 'mongodb://localhost:27017';

// Database Name
const dbName = 'mydatabase';

async function main() {
  const client = new MongoClient(url);
  
  try {
    await client.connect();
    console.log('Connected to MongoDB!');
    
    const db = client.db(dbName);
    const collection = db.collection('users');

    // Insert a document
    const user = { name: 'John Doe', age: 30 };
    await collection.insertOne(user);
    
    // Query the document
    const result = await collection.findOne({ name: 'John Doe' });
    console.log('Found user:', result);
  } finally {
    await client.close();
  }
}

main().catch(console.error);
```

