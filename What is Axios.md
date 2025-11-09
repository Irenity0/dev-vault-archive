Axios is a **promise-based HTTP client** for making requests to APIs. It works in both **browsers** and **Node.js** and is often used instead of the built-in `fetch()` method because of its **simpler syntax, automatic JSON handling, and better error handling**.

---

### **Why Use Axios Instead of Fetch?**

✅ **Automatic JSON parsing** (no need for `.json()`)  
✅ **Simpler syntax** for GET and POST requests  
✅ **Better error handling** (fetch doesn’t catch HTTP errors like 404)  
✅ **Supports request/response interception**  
✅ **Works with older browsers**

---

### **Example: GET Request with Axios**

```javascript
// Install Axios (if using Node.js): npm install axios

const axios = require("axios"); // Not needed in browsers

async function fetchData() {
  try {
    const response = await axios.get("https://api.example.com/data");
    console.log(response.data); // No need to manually parse JSON
  } catch (error) {
    console.error("Error:", error.response ? error.response.data : error.message);
  }
}

fetchData();
```

---

### **Example: POST Request with Axios**

```javascript
axios.post("https://api.example.com/users", {
  name: "Alice",
  age: 25
})
.then(response => console.log(response.data))
.catch(error => console.error("Error:", error));
```

➡ Sends data to the API and logs the response.

---

### **Key Features of Axios:**

✔ **GET, POST, PUT, DELETE support**  
✔ **Custom headers** (useful for authentication)  
✔ **Automatic JSON parsing**  
✔ **Request timeout handling**  
✔ **Built-in response interception**