**Authorization** is the process of determining what actions, resources, or data a user is allowed to access after they have been authenticated. It ensures that users only have permissions relevant to their role or identity.

### Key Elements of Authorization
1. **Access Control**: Determines what a user can do within the system.
2. **Roles & Permissions**:
    - **Role-Based Access Control (RBAC)**: Users are assigned roles, and each role has predefined permissions (e.g., "Admin," "User").
    - **Permission-Based Access Control**: Specific permissions are granted to users or roles (e.g., "read-only," "edit").
3. **Resource Protection**: Ensures users access only the data or operations they are authorized for.
---
### **Authorization vs. Authentication**
- **Authentication**: Confirms _who you are_ (e.g., logging in with credentials).
- **Authorization**: Confirms _what you are allowed to do_ (e.g., accessing specific files or settings).

### **Importance of Authorization**
1. **Data Security**:
    - Protects sensitive information from unauthorized users.
2. **Prevents Misuse**:
    - Limits actions users can take to their intended scope.
3. **Compliance**:
    - Ensures systems meet regulatory requirements (e.g., HIPAA, GDPR).
4. **Granular Control**:
    - Fine-tunes access for complex systems and multiple user roles.

### **Examples**
1. **Social Media**:
    - A regular user can edit only their profile, while an admin can manage all user accounts.
2. **E-commerce**:
    - Customers can view and purchase items, but store managers can manage inventory.
3. **APIs**:
    - A token-based API may allow reading data but not writing or deleting it unless authorized.

### Related Notes

- [[Types of Authorization]]
- [[How Authorization Works]]
- [[Common Authorization Tools & Protocols]]