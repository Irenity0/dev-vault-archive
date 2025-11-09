CRUD stands for **Create, Read, Update, Delete**—the four basic operations performed on a database or API. It is the foundation of most web applications that interact with data.

---

### **CRUD Operations in a REST API**

CRUD operations typically map to HTTP methods as follows:

|CRUD Operation|HTTP Method|Example Endpoint|
|---|---|---|
|**Create**|POST|`/users` (Add a new user)|
|**Read**|GET|`/users` (Get all users)|
|**Update**|PUT/PATCH|`/users/1` (Update user 1)|
|**Delete**|DELETE|`/users/1` (Remove user 1)|

---

### **Example Using Axios (CRUD with a Users API)**

#### **1. Create (POST) - Add a new user**

```javascript
axios.post("https://api.example.com/users", {
  name: "Alice",
  age: 25
})
.then(response => console.log(response.data))
.catch(error => console.error("Error:", error));
```

#### **2. Read (GET) - Fetch users**

```javascript
axios.get("https://api.example.com/users")
  .then(response => console.log(response.data))
  .catch(error => console.error("Error:", error));
```

#### **3. Update (PUT) - Modify a user’s data**

```javascript
axios.put("https://api.example.com/users/1", {
  name: "Alice Johnson",
  age: 26
})
.then(response => console.log(response.data))
.catch(error => console.error("Error:", error));
```

#### **4. Delete (DELETE) - Remove a user**

```javascript
axios.delete("https://api.example.com/users/1")
  .then(response => console.log("User deleted"))
  .catch(error => console.error("Error:", error));
```

---

### **Where is CRUD Used?**

✔ Web apps (social media, e-commerce, blogs)  
✔ APIs and backend services  
✔ Databases (SQL, NoSQL)