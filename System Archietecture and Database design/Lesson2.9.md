# 2.9 — Database Relationships (1:1, 1:M, M:N)

Now we know **Primary Keys and Foreign Keys**. The next question is:

> **How are our entities connected to each other?**

This is called a **database relationship**.

There are three important relationship types:

1. **1:1 — One-to-One**
2. **1:M — One-to-Many**
3. **M:N — Many-to-Many**

---

## 1. One-to-One (1:1)

One record in Table A is related to **one record** in Table B.

### Example

Suppose each user has exactly one profile.

```text
User
  │
  │ 1
  │
  │ 1
  ▼
Profile
```

Example:

```text
users
id | name
1  | Daenish
2  | Niraj
```

```text
profiles
id | user_id | bio
1  | 1       | Developer
2  | 2       | Student
```

So:

```text
Daenish → One Profile
Niraj   → One Profile
```

That's **1:1**.

---

# 2. One-to-Many (1:M)

One record in Table A can be related to **many records** in Table B.

This is very common.

### Example: User → Assessment Results

One user can have multiple assessment results.

```text
User
  │
  │ 1
  │
  │ M
  ▼
Assessment Results
```

Example:

```text
users
id | name
1  | Daenish
```

```text
assessment_results
id | user_id | score
1  | 1       | 75
2  | 1       | 82
3  | 1       | 91
```

One user:

```text
Daenish
   │
   ├── Result 1
   ├── Result 2
   └── Result 3
```

Therefore:

**User → Assessment Results = 1:M**

---

# 3. Many-to-Many (M:N)

Many records in Table A can be related to many records in Table B.

### Example: Users and Skills

A user can have many skills.

```text
Daenish
 ├── Java
 ├── React
 └── PostgreSQL
```

But one skill can belong to many users.

```text
Java
 ├── Daenish
 ├── Niraj
 └── Another User
```

Therefore:

```text
Users ↔ Skills
```

is **Many-to-Many (M:N)**.

---

# 4. How Do We Store M:N?

Relational databases normally use a **junction/join table**.

For example:

```text
users
skills
user_skills
```

The `user_skills` table connects them.

```text
user_skills
+---------+----------+
| user_id | skill_id |
+---------+----------+
|    1    |    1     |
|    1    |    2     |
|    2    |    1     |
+---------+----------+
```

This means:

```text
Daenish → Java
Daenish → React
Niraj   → Java
```

Conceptually:

```text
Users
  │
  │
  ▼
user_skills
  ▲
  │
  │
Skills
```

We'll study this more deeply when designing our actual schema.

---

# 5. Our Project Examples

Some possible relationships in our platform:

| Relationship | Type |
|---|---|
| User → Assessment Results | 1:M |
| User → Recommendations | 1:M |
| User ↔ Skills | M:N |
| Career ↔ Skills | M:N |
| Assessment → Assessment Results | 1:M |

⚠️ These are **initial design candidates**, not the final schema. We'll finalize them later.

---

## Easy Way to Remember

```text
1:1
One → One

1:M
One → Many

M:N
Many ↔ Many
```

Real-world analogy:

```text
1:1
Person → Passport

1:M
User → Assessment Results

M:N
Users ↔ Skills
```

---


### Why do we need juction/join table in DBMS?.Explain me with a simple example.

We need a junction table (also called a join, bridge, or associative table) in a Database Management System (DBMS) to model a many-to-many relationship between two tables.
Relational databases cannot directly link two tables if multiple rows in the first table relate to multiple rows in the second table. Attempting to do so by stuffing multiple values into a single column violates database design rules, while creating duplicate rows leads to massive data redundancy. A junction table solves this by breaking the many-to-many relationship into two clean, manageable one-to-many relationships.

------------------------------
## 💡 A Simple Example: Students and Courses
Let's look at a school database:

* One Student can enroll in multiple Courses.
* One Course can have multiple Students enrolled in it.

This is a classic many-to-many relationship.
## Step 1: The Two Main Tables
First, we have our primary tables, which only hold unique information about the entities themselves.
Students Table

| student_id (PK) | student_name |
|---|---|
| 1 | Alice |
| 2 | Bob |

Courses Table

| course_id (PK) | course_name |
|---|---|
| 101 | Mathematics |
| 102 | Computer Science |

(Note: PK stands for Primary Key, a unique identifier for each row).
## Step 2: The Junction Table (The Bridge)
To link them without messing up our clean tables, we create a third table: Enrollments.
This junction table holds the Foreign Keys (FK) pointing back to both primary tables. Each row represents a single link between one student and one course.
Enrollments Table (Junction Table)

| student_id (FK) | course_id (FK) |
|---|---|
| 1 | 101 |
| 1 | 102 |
| 2 | 102 |

## 🚀 Why This Matters

   1. No Data Duplication: We don't have to repeat Alice's name or the course titles over and over again. We only store numbers (IDs).
   2. Easy Extra Data: If you want to track the grade a student got or the date they enrolled, you can simply add a grade column right into this junction table.




