# 2.10 — ER Diagram

Now we are going to visually represent the entities and their relationships.

## 1. What is an ER Diagram?

**ER Diagram = Entity Relationship Diagram**

It is a visual representation of:

- Entities
- Attributes
- Relationships between entities

Think of it as a **blueprint of our database**.

For example:

```text
        ┌──────────────┐
        │    Users     │
        ├──────────────┤
        │ id           │
        │ name         │
        │ email        │
        └──────┬───────┘
               │
              1:M
               │
               ▼
        ┌────────────────────┐
        │ Assessment Results │
        ├────────────────────┤
        │ id                 │
        │ user_id            │
        │ score              │
        └────────────────────┘
```

This immediately tells us:

> One user can have many assessment results.

---

# 2. Main Components of an ER Diagram

### Entity

Usually represented as a rectangle:

```text
┌──────────┐
│  User    │
└──────────┘
```

### Attribute

Properties of the entity:

```text
User
 ├── id
 ├── name
 └── email
```

### Relationship

Shows how entities are connected:

```text
User ─────── Assessment Result
       1:M
```

---

# 3. ER Diagram for Our Project

Based on what we've learned so far, we can create an **initial ER design**:

```text
                    ┌──────────────┐
                    │    USER      │
                    ├──────────────┤
                    │ id           │
                    │ name         │
                    │ email        │
                    └──────┬───────┘
                           │
                         1:M
                           │
              ┌────────────▼────────────┐
              │   ASSESSMENT_RESULT     │
              ├─────────────────────────┤
              │ id                      │
              │ user_id                 │
              │ score                   │
              └─────────────────────────┘
```

We also have:

```text
USER  M:N  SKILL
```

which will eventually use:

```text
USER
  │
  │ 1:M
  ▼
USER_SKILL
  ▲
  │ 1:M
  │
SKILL
```

---

# 4. Why ER Diagrams Are Important

Before creating actual PostgreSQL tables, an ER diagram helps us:

### 1. Understand the database

We can see what entities exist.

### 2. Find relationships

We can identify:

```text
1:1
1:M
M:N
```

### 3. Find missing entities

For example, while drawing the diagram, we may realize:

> "We need a separate `user_skills` table."

### 4. Reduce database design mistakes

We can identify problems **before writing SQL**.

### 5. Communicate with your teammate

Since you're working with **Niraj**, both of you can look at the same diagram and understand how the database should work.

---

# 5. ER Diagram vs Database Schema

Don't confuse these two.

### ER Diagram

Visual design:

```text
User ──1:M── Assessment_Result
```

### Database Schema

Actual table structure:

```sql
CREATE TABLE assessment_results (
    id BIGSERIAL PRIMARY KEY,
    user_id BIGINT,
    score INTEGER
);
```

So:

```text
ER Diagram
    ↓
Database Design
    ↓
Database Schema
    ↓
PostgreSQL Tables
```

---

# 6. Important Point for Our Project

Our ER diagram at this stage is **not final**.

We still need to learn:

```text
2.10 → ER Diagram
2.11 → Normalization
2.12 → Complete Database Schema
```

After normalization, we'll refine the ER diagram and then create our **final database schema**.

---

