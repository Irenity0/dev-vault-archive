
| u_id | name            | email              | gender | age | dob        |
| ---- | --------------- | ------------------ | ------ | --- | ---------- |
| 1    | ire             | ire@gmail          | female | 16  | 2009-01-01 |
| 2    | Naruto Uzumaki  | naruto@leaf        | male   | 17  | 2007-10-10 |
| 3    | Mikasa Ackerman | mikasa@paradis     | female | 19  | 2006-02-10 |
| 4    | L Lawliet       | l@wammyhouse       | male   | 24  | 2000-06-06 |
| 5    | Levi Ackerman   | levi@scoutregiment | male   | 30  | 1995-12-25 |

### What is a Key?
``
A **key** in a relational database is a field (or a combination of fields) that is used to uniquely identify each record (row) in a table.

### What is a Super Key?

- A **super key** is any combination of fields that can uniquely identify a row in the table.   
- It **may contain extra attributes** not necessary for uniqueness.
- Example from the table:
	- `{u_id}` is a super key.
    - `{u_id, email}`, `{u_id, name}`, `{u_id, email, name}` — all are super keys because they include a unique field (`u_id`) and still ensure uniqueness.

### What is a Candidate Key?

- A **candidate key** is a **minimal super key** — meaning it has **only the necessary fields** to ensure uniqueness (no extra attributes).
- There can be multiple candidate keys in a table.
- Example from the table:
    - `{u_id}` — because it uniquely identifies each record with no unnecessary fields.
    - `{email}` — assuming emails are unique, this could also be a candidate key.

### What is a Primary Key?

- A **primary key** is a **special candidate key** chosen to **uniquely identify** each record (row) in a table.
- It **must contain unique values** and **cannot be NULL**.
- Each table can have **only one primary key**.
- The primary key ensures that no two rows in the table have the same identifier.

### What is an Alternate Key?

- An **alternate key** is a **candidate key that is not chosen** as the primary key.    
- Used as a **backup unique identifier**.
- Example from the table:
    - If `u_id` is chosen as the primary key, then `email` becomes the alternate key (assuming it’s unique).

### What is a Unique Key?

- A **unique key** is a field (or combination of fields) that **must contain only unique values** across all rows in the table.
- Unlike the primary key, a unique key **can have NULL values** (usually one NULL per column, depending on the database).
- A table can have **multiple unique keys** in addition to the primary key.
- Used to enforce **data integrity** on fields that should be unique (like usernames, emails, etc.).
- Example from the table:
    - `email` can be set as a unique key to ensure **no two users share the same email address**, even if it's not the primary key.

### What is a Composite Key?

- A **composite key** is a **combination of two or more fields** used together to uniquely identify a record.    
- Used when **no single field is unique** on its own.
- Example:
    - If the table didn’t have `u_id`, and both `name` and `dob` were used together to uniquely identify a user, then `{name, dob}` would be a composite key.

> [!NOTE] Note
> Composite keys are not required if you already have a single unique field like `u_id`.

### What is a Foreign Key?

- A **foreign key** is a field (or collection of fields) in one table that refers to the **primary key in another table**.
- It is used to create **relationships between tables**.
- Example (not present in this table):
    - If there was another table `Orders` with a column `user_id` referencing the `u_id` in this table, then `user_id` in `Orders` would be a **foreign key**.


## Comparison Table

| Key Type          | Description                                                        | Uniquely Identifies Rows? | Can Have NULL Values?  | Single Field or Multiple?       | Example from Your Table                         |
| ----------------- | ------------------------------------------------------------------ | ------------------------- | ---------------------- | ------------------------------- | ----------------------------------------------- |
| **Primary Key**   | Main key chosen to uniquely identify each record                   | ✅ Yes                     | ❌ No                   | Usually single, can be multiple | `u_id`                                          |
| **Super Key**     | Any set of attributes that uniquely identifies a record            | ✅ Yes                     | ✅ Yes (if not primary) | Single or multiple              | `{u_id}`, `{u_id, email}`, `{email, name}`      |
| **Candidate Key** | Minimal super key (no unnecessary fields)                          | ✅ Yes                     | ❌ No                   | Single or multiple              | `{u_id}`, `{email}` (if unique)                 |
| **Alternate Key** | A candidate key not selected as the primary key                    | ✅ Yes                     | ❌ No                   | Single or multiple              | `email` (if `u_id` is the primary key)          |
| **Composite Key** | Key formed by combining two or more fields                         | ✅ Yes                     | ❌ No (as a whole)      | Always multiple                 | `{name, dob}` (if no `u_id`)                    |
| **Foreign Key**   | A key in one table that refers to the primary key in another table | ❌ No (not in own table)   | ✅ Yes (if allowed)     | Single or multiple              | `user_id` in another table → `u_id` in this one |

# some important shit

- **Primary key** ⊆ **Candidate key** ⊆ **Super key**
- **Composite keys** and **foreign keys** are more relevant in multi-table setups.
- **Foreign keys** help maintain **referential integrity**.

### ✅ **Primary key ⊆ Candidate key ⊆ Super key**

This is a way of saying:

- Every **primary key** is a **candidate key**.
- Every **candidate key** is a **super key**.
- But the reverse is **not always true**.

Let’s break it down:
### 🔹 **Super Key**

- **Any** field or combination of fields that can uniquely identify a row.
- **Can have extra (unnecessary) attributes**.
- Example: `{u_id}`, `{u_id, name}`, `{email, name}`  
    → All these can identify a user uniquely.

### 🔹 **Candidate Key**

- A **minimal super key** — just enough fields to uniquely identify a row.
- **No extra fields allowed**.
- Example: `{u_id}`, `{email}` (if unique)  
    → You don't need both `u_id` and `name` if `u_id` alone is enough.

### 🔹 **Primary Key**

- **One** candidate key that the database chooses as the **main identifier**.
- Must be **not null** and **unique**.
- Example: `{u_id}` — this is selected as the primary key in your table.

### Visual Summary

```plaintext
Super Keys:        {u_id}, {u_id, name}, {email, name}
                        ↑
Candidate Keys:     {u_id}, {email}
                        ↑
Primary Key:         {u_id}
```

So:
- **Primary key** is a special **candidate key**.
- **Candidate key** is a special **super key** (with no extra stuff).