# 2.11 — Database Normalization

We are now at an important step before designing our **final PostgreSQL schema**.

## 1. What is Database Normalization?

**Database normalization** is the process of organizing data into tables properly to:

- reduce duplicate data
- prevent data inconsistency
- make relationships easier to manage
- make inserting, updating, and deleting data safer

A simple way to remember:

> **Normalization = Organize the database to avoid unnecessary duplication and data problems.**

---

# 2. Why Do We Need Normalization?

Imagine we store user skills like this:

| user_id | user_name | skills |
|---:|---|---|
| 1 | Daenish | Java, React, SQL |
| 2 | Niraj | Java, Python |
| 3 | Ram | Java, React |

There are several problems.

### Problem 1 — Multiple values in one column

```text
skills = "Java, React, SQL"
```

A column should ideally contain a single value, not a list of values.

### Problem 2 — Searching becomes difficult

Finding:

> "Which users have React?"

becomes harder.

### Problem 3 — Updating becomes difficult

If `React` changes or we need to update skill information, we may have to modify many records.

### Problem 4 — Duplicate data

`Java` appears repeatedly.

Instead, we can separate the data:

```text
users
skills
user_skills
```

This is where normalization helps.

---

# 3. The Three Normal Forms

For our project, we'll learn three levels:

```text
1NF
 ↓
2NF
 ↓
3NF
```

Each level solves a different type of database problem.

---

# 4. 1NF — First Normal Form

The main idea of **1NF** is:

> **Each column should contain atomic/single values, and there should be no repeating groups.**

### ❌ Not 1NF

```text
users

id | name    | skills
1  | Daenish | Java, React, SQL
```

The `skills` column contains multiple values.

### ✅ Better

Separate the values:

```text
users

id | name
1  | Daenish
```

```text
skills

id | name
1  | Java
2  | React
3  | SQL
```

And connect them:

```text
user_skills

user_id | skill_id
1       | 1
1       | 2
1       | 3
```

Now each value is stored properly.

---

# 5. 2NF — Second Normal Form

2NF is mainly important when a table has a **composite primary key**.

The basic idea is:

> **The table must already be in 1NF, and every non-key attribute must depend on the whole primary key.**

Consider:

```text
user_skills

user_id | skill_id | user_name | skill_name
--------|----------|-----------|-----------
1       | 1        | Daenish   | Java
1       | 2        | Daenish   | React
2       | 1        | Niraj     | Java
```

Suppose:

```text
(user_id, skill_id)
```

is the composite primary key.

But:

```text
user_name
```

depends only on `user_id`.

And:

```text
skill_name
```

depends only on `skill_id`.

They don't depend on the **whole composite key**.

So we separate them:

```text
users
id | name
```

```text
skills
id | name
```

```text
user_skills
user_id | skill_id
```

Now each table has a clear responsibility.

---

# 6. 3NF — Third Normal Form

3NF deals with **indirect dependencies**.

The simple rule is:

> **A non-key column should depend on the key, the whole key, and nothing but the key.**

Consider:

```text
users

id | name    | career_id | career_name
1  | Daenish | 10        | Software Developer
```

Here:

```text
id → career_id → career_name
```

`career_name` doesn't directly depend on `id`.

It depends on `career_id`.

This creates an indirect dependency.

Instead:

```text
users
id | name | career_id
```

and:

```text
careers
id | name
```

Now:

```text
users.career_id
        ↓
careers.id
```

The career information belongs in the `careers` table.

---

# 7. Easy Way to Remember

For your exam/project documentation, remember:

### 1NF

> **One value per cell.**

### 2NF

> **Depend on the whole primary key.**

### 3NF

> **Don't store data that depends indirectly on another non-key column.**

A common memory trick is:

```text
1NF → Atomic values
2NF → Whole key
3NF → Nothing but the key
```

---

# 8. Applying Normalization to Our Project

Our project might initially look like this:

```text
User
 ├── name
 ├── email
 ├── skills
 ├── career_name
 └── career_description
```

That would create several problems.

After normalization, we can have separate entities such as:

```text
users
skills
careers
user_skills
assessment
assessment_results
learning_resources
recommendations
```

And relationships connect them.

For example:

```text
users
   │
   │
   ▼
user_skills
   ▲
   │
skills
```

This is much cleaner than storing:

```text
skills = "Java, React, SQL"
```

inside the `users` table.

---

# 9. Important: Normalization Doesn't Mean "Make More Tables"

Don't think:

> "More tables = better normalization."

That's not necessarily true.

The goal is:

> **Store each piece of information in the appropriate place and avoid unnecessary duplication.**

We still need to balance normalization with practical application requirements.

---

