An **API (Application Programming Interface)** is a set of rules that allows different software applications to communicate with each other.

### In Web Development:

APIs enable a client (browser/app) to interact with a server to send or receive data, usually via HTTP requests.

### Example (Fetching data from an API in JavaScript):

```javascript
fetch("https://api.example.com/data")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error("Error:", error));
```

This fetches data from an API and logs it to the console.

