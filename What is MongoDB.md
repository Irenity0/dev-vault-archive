**MongoDB** is a **NoSQL** (Not Only SQL) database management system that stores data in a flexible, document-oriented format, unlike traditional relational databases (SQL) which store data in tables. MongoDB uses **JSON-like documents** (specifically **BSON**, which stands for Binary JSON) to store data. This allows for greater flexibility and scalability when managing large volumes of data.

---

[[Key MongoDB Features]]

---

### **MongoDB vs. SQL Databases**

- **Data Storage**:
    - SQL databases store data in **tables** with a fixed schema. 
    - MongoDB stores data in **documents** (BSON) which are more flexible and do not require a fixed schema.
        
- **Scalability**:
    - SQL databases typically scale vertically (upgrading server capacity).
    - MongoDB scales **horizontally** (adding more machines/servers).
        
- **Flexibility**:
    - SQL databases are rigid with predefined schemas.
    - MongoDB allows for easy modification of the schema, making it ideal for applications that evolve rapidly.
        

---

### **Basic MongoDB Operations:**

1. **Inserting Data**:
    
    ```javascript
    db.users.insertOne({ name: "John Doe", age: 30, hobbies: ["reading", "sports"] });
    ```
    
2. **Finding Data**:
    
    ```javascript
    db.users.find({ age: { $gt: 25 } });
    ```
    
3. **Updating Data**:
    
    ```javascript
    db.users.updateOne(
      { _id: "12345" },
      { $set: { age: 31 } }
    );
    ```
    
4. **Deleting Data**:
    
    ```javascript
    db.users.deleteOne({ _id: "12345" });
    ```
    

---

### **When to Use MongoDB?**

- **When dealing with large volumes of unstructured or semi-structured data** (e.g., content management systems, social media platforms).
    
- **When flexibility in schema design is required**, such as evolving applications that need to store different types of data.
    
- **When scalability and performance** are critical, especially for applications requiring high availability and low-latency responses.
    

---

### **Example of a Simple MongoDB Setup with Node.js**:

[[simple mongodb setup with nodejs]]

---

### **Summary**:

**MongoDB** is a **NoSQL** database that stores data in a flexible, document-oriented format (BSON), making it highly suitable for applications that require scalability, high performance, and flexible data structures. Unlike traditional SQL databases, MongoDB offers a schema-less design, allowing for easier handling of complex or rapidly changing data. It is widely used in modern web applications, especially those requiring high availability and real-time performance.