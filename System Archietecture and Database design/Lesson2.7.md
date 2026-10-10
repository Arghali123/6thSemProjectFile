# 2.7 — Identifying Database Entities

Now we move from:

> **"What data does our system need?"**

to:

> **"What are the main things/entities that our system needs to store?"**

### 1. What is an Entity?

An **entity** is a real-world object or concept about which our system needs to store information.

For example:

```text
User
Skill
Career
Assessment
Learning Resource
```

Each of these can become a **database table**.

Think of it like this:

```text
Entity → Database Table
```

For example:

```text
User → users table

Skill → skills table

Career → careers table
```

---

## 2. Entity vs Attribute

This is very important.

Suppose we have:

```text
User
```

The **User** is the entity.

Its information can be:

```text
User
 ├── id
 ├── name
 ├── email
 ├── password
 └── phone
```

Here:

- `User` → **Entity**
- `id`, `name`, `email`, `password`, `phone` → **Attributes**

So:

```text
Entity = What thing are we storing?

Attribute = What information do we store about that thing?
```

---

# 3. Entities in Our Project

For the **AI Skill & Career Management Platform**, we can identify several important entities.

### 1. User

Stores information about people using the platform.

```text
User
 ├── id
 ├── name
 ├── email
 └── password
```

---

### 2. Skill

Stores skills available in the platform.

```text
Skill
 ├── id
 ├── name
 └── description
```

Examples:

```text
Java
Spring Boot
React
Python
Machine Learning
SQL
```

---

### 3. Career

Stores career paths.

```text
Career
 ├── id
 ├── name
 └── description
```

Examples:

```text
Software Developer
Data Scientist
AI Engineer
Web Developer
DevOps Engineer
```

---

### 4. Assessment

Stores information about assessments.

```text
Assessment
 ├── id
 ├── title
 └── description
```

---

### 5. Assessment Result

Stores a user's assessment result.

```text
Assessment Result
 ├── id
 ├── score
 └── result
```

Notice something important:

**Assessment** and **Assessment Result** are different concepts.

An assessment is the test itself.

An assessment result belongs to a user's attempt/result.

---

### 6. Learning Resource

Stores resources that help users learn skills.

```text
Learning Resource
 ├── id
 ├── title
 ├── description
 └── url
```

Examples:

```text
Java Course
Spring Boot Tutorial
React Documentation
Python Course
```

---

### 7. Recommendation

Our system may also need to store AI-generated recommendations.

```text
Recommendation
 ├── id
 ├── type
 ├── content
 └── created_at
```

For example:

```text
User needs React skills
        ↓
AI analyzes skill gap
        ↓
Recommendation
        ↓
"Learn React Hooks"
```

---

# 4. Important: Don't Create Tables Too Early

At this stage, we are **identifying entities**, not creating the final database schema.

For example, we currently have:

```text
User
Skill
Career
Assessment
Assessment Result
Learning Resource
Recommendation
```

But we haven't decided:

- Primary keys
- Foreign keys
- Relationships
- Many-to-many tables
- Exact columns
- Normalization

Those will be covered in the upcoming lessons.

---

# 5. How to Identify an Entity

A simple technique is to look at the **nouns** in our requirements.

For example:

> "A user can select skills and receive career recommendations based on assessment results."

Important nouns:

```text
User
Skills
Career
Recommendation
Assessment
Assessment Result
```

These are potential entities.

Then we ask:

> **Does the system need to store information about this thing?**

If yes → it may be an entity.

---

