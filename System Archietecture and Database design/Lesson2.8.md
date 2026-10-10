# 2.8 — Understanding Primary Keys & Foreign Keys

Now that we know our entities, we need to understand **how to uniquely identify records and connect tables**.

## 1. What is a Primary Key?

A **Primary Key (PK)** is a column that uniquely identifies each record in a table.

Example:

```text
users
+----+---------+----------------------+
| id | name    | email                |
+----+---------+----------------------+
| 1  | Daenish | daenish@example.com  |
| 2  | Niraj   | niraj@example.com    |
+----+---------+----------------------+
```

Here:

```text
id = Primary Key
```

Why?

Because every user has a unique `id`.

```text
Daenish → id 1
Niraj   → id 2
```

Two users should not have the same primary-key value.

---

## 2. Characteristics of a Primary Key

A primary key should generally be:

- ✅ Unique
- ✅ Not `NULL`
- ✅ Stable
- ✅ Used to identify one specific record

Example:

```text
id
1
2
3
4
```

---

# 3. What is a Foreign Key?

A **Foreign Key (FK)** is a column that references a primary key in another table.

It is used to **create a relationship between tables**.

For example:

```text
users
+----+---------+
| id | name    |
+----+---------+
| 1  | Daenish |
| 2  | Niraj   |
+----+---------+
```

Suppose we have:

```text
assessment_results
+----+---------+-------+
| id | user_id | score |
+----+---------+-------+
| 1  | 1       | 85    |
| 2  | 2       | 78    |
+----+---------+-------+
```

Here:

```text
users.id       → Primary Key
assessment_results.user_id → Foreign Key
```

The `user_id` tells us:

> This assessment result belongs to which user?

For example:

```text
user_id = 1
      ↓
users.id = 1
      ↓
Daenish
```

---

# 4. PK vs FK

Remember this simple rule:

```text
Primary Key
     ↓
Identifies a record

Foreign Key
     ↓
Connects to another table
```

Example:

```text
users
┌─────────────┐
│ id (PK)     │
│ name        │
│ email       │
└──────┬──────┘
       │
       │ referenced by
       ▼
┌────────────────────────┐
│ assessment_results     │
│ id (PK)                │
│ user_id (FK)           │
│ score                  │
└────────────────────────┘
```

---

# 5. Why Do We Need Foreign Keys?

Imagine we only stored:

```text
assessment_results

id | score
1  | 85
2  | 78
```

We know the scores, but we don't know **which user** achieved them.

With:

```text
id | user_id | score
1  | 1       | 85
2  | 2       | 78
```

we can connect the result to the user.

This is how relational databases maintain relationships between tables.

---

# 6. Primary Key and Foreign Key in Our Project

Our project will eventually have relationships such as:

```text
users
  │
  │ user_id
  ▼
assessment_results
```

and potentially:

```text
users
  │
  ▼
recommendations
```

The exact relationships will be designed in **Lesson 2.9 — Database Relationships**.

---

