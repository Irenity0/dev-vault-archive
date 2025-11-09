### **Key Features of Express.js:**

1. **Routing**:  
    Express allows you to define routes to handle different HTTP requests (GET, POST, PUT, DELETE, etc.) with ease.
    
    ```javascript
    app.get('/', (req, res) => {
      res.send('Hello World!');
    });
    ```
    
2. **Middleware**:  
    Express supports middleware functions that allow you to handle requests, add extra functionality, and manipulate responses before they reach the client.
    
    ```javascript
    app.use((req, res, next) => {
      console.log('Request received');
      next(); // Pass control to the next middleware or route handler
    });
    ```
    
3. **Template Engines**:  
    Express supports template engines like **EJS**, **Pug**, and **Handlebars** to dynamically generate HTML pages based on server-side logic.
    
4. **Request Handling**:  
    Express simplifies working with incoming requests and outgoing responses, allowing you to easily access query parameters, request bodies, and headers.
    
    ```javascript
    app.post('/submit', (req, res) => {
      console.log(req.body);  // Access POST data
      res.send('Data received!');
    });
    ```
    
5. **Built-in HTTP Utilities**:  
    Express provides utility methods to handle various HTTP responses, like sending JSON data or setting status codes.
    
    ```javascript
    res.status(404).send('Not Found');
    ```
    
6. **Error Handling**:  
    Express has built-in support for handling errors and generating error pages.
    