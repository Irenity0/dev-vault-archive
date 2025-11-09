**JWT (JSON Web Token)** is a compact and self-contained way to securely transmit information between parties as a **JSON object**. It is commonly used for **authentication** and **authorization** in web applications, especially when dealing with APIs.

---

### **Structure of a JWT:**

A JWT consists of **three parts** separated by dots (`.`):

1. **Header**:  
    The header typically contains two parts:
    
    - **Type of token** (JWT).
        
    - **Signing algorithm** (such as HMAC SHA256 or RSA).
        
    
    Example:
    
    ```json
    {
      "alg": "HS256",
      "typ": "JWT"
    }
    ```
    
2. **Payload**:  
    The payload contains the **claims**, which are statements about an entity (typically, the user) and additional data. These claims can be:
    
    - **Registered claims**: Predefined claims like `iss` (issuer), `exp` (expiration), `sub` (subject).
        
    - **Public claims**: Custom claims that can be used by anyone (e.g., user roles or permissions).
        
    - **Private claims**: Claims created to share information between parties that agree on them.
        
    
    Example:
    
    ```json
    {
      "sub": "1234567890",
      "name": "John Doe",
      "iat": 1516239022
    }
    ```
    
3. **Signature**:  
    The signature is used to verify that the sender of the JWT is who it says it is and to ensure that the message hasn't been altered. It is created by taking the encoded header, encoded payload, a secret key, and the algorithm specified in the header (e.g., `HS256`).
    
    Example:
    
    ```text
    HMACSHA256(
      base64UrlEncode(header) + "." + base64UrlEncode(payload),
      secret)
    ```
    

---

[[how JWT works]]

---

### **Example of a JWT:**

Here’s an example of a JWT:

```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c
```

This consists of three parts:

1. **Header** (Base64 URL encoded)
    
2. **Payload** (Base64 URL encoded)
    
3. **Signature** (Base64 URL encoded)
    

---

### **Why Use JWT?**

1. **Stateless**:  
    JWT is **stateless**, meaning the server does not need to store session information. The token itself contains all the necessary data to authenticate and authorize the user.
    
2. **Scalable**:  
    Because the server does not have to maintain session state, it is easier to scale the application, especially when dealing with multiple servers or microservices.
    
3. **Security**:  
    The signature ensures the integrity of the JWT, preventing tampering. Additionally, it can be encrypted for further security.
    
4. **Cross-Domain Authentication**:  
    JWT can be used for single sign-on (SSO) across different domains and platforms.
    

---

[[jwt explain with expressjs server snippet]]

---

### **Summary**:

**JWT (JSON Web Token)** is a secure way to transmit information between parties as a JSON object, commonly used for **authentication** and **authorization** in web applications. It allows for stateless communication, meaning no need for the server to store user sessions, making it scalable and efficient for modern web applications.