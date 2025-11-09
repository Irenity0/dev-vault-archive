### **How JWT Works (Authentication Process)**:

1. **User Login**:  
    The user logs in by sending their credentials (username/password) to the server.
    
2. **JWT Creation**:  
    If the credentials are valid, the server generates a JWT containing the user’s information (e.g., user ID, role) and sends it back to the client (usually in the response body or HTTP header).
    
3. **Client Stores JWT**:  
    The client (browser or app) stores the JWT, typically in **localStorage** or **sessionStorage** for later use.
    
4. **Subsequent Requests**:  
    For subsequent requests to protected routes, the client includes the JWT in the `Authorization` header (usually with the `Bearer` prefix).
    
    ```text
    Authorization: Bearer <token>
    ```
    
5. **Token Validation**:  
    The server checks the token’s signature and expiration date. If the token is valid, the server processes the request; otherwise, it rejects the request.
    