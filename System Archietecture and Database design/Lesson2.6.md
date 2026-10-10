# 📘 Lesson 2.6 — Introduction to Database Design

Now we are moving from **system architecture** into **database design**.

This is a very important transition.

Until now, we have mainly asked:

> "How will the components of our application communicate?"

Now we'll start asking:

> **"What data does our application need, and how should we organize that data?"**

---

# 1. What is Database Design?

**Database design is the process of deciding how data will be stored, organized, related, and managed in a database.**

For our project, we need to decide things like:

```text
What information should we store about users?
What information should we store about skills?
What information should we store about careers?
How are users connected to skills?
How are careers connected to skills?
Where should assessment results be stored?
```

We should answer these questions **before creating PostgreSQL tables**.

---

# 2. Why Do We Need Database Design?

Imagine we start creating tables without planning.

We might end up with something like:

```text
users
skills
career
user_data
student_information
user_skills_data
career_skills_data
random_table
```

And later discover:

```text
❌ Duplicate data
❌ Difficult relationships
❌ Difficult queries
❌ Data inconsistency
❌ Difficult maintenance
```

Good database design prevents many of these problems.

---

# 3. Our Project Depends Heavily on Data

Think about our platform.

A user might have:

```text
Name
Email
Skills
Skill levels
Career goals
Assessment results
Learning history
Recommendations
```

A skill might have:

```text
Skill name
Description
Category
Difficulty
```

A career might have:

```text
Career name
Description
Required skills
```

So we need a proper structure for storing all of this.

---

# 4. Database Design Starts With Requirements

We don't immediately start with SQL.

Instead:

```text
Requirements
     ↓
Identify Data
     ↓
Identify Entities
     ↓
Identify Relationships
     ↓
Design Tables
     ↓
Normalize
     ↓
Create Database Schema
```

For our project:

```text
Module 1
Requirements
     ↓
Module 2
Database Design
     ↓
PostgreSQL
```

That's why completing Module 1 first was important.

---

# 5. What is Data?

**Data is information that our application needs to store or process.**

For example:

```text
User:
Daenish
user@example.com
```

That's data.

Another example:

```text
Skill:
Java
```

Another:

```text
Career:
Java Backend Developer
```

Our database will store structured versions of this information.

---

# 6. What is a Database Table?

A database table organizes related data into **rows and columns**.

For example, imagine a simple `users` table:

| id | name | email |
|---:|---|---|
| 1 | Daenish | daenish@example.com |
| 2 | Niraj | niraj@example.com |

Here:

- `users` = table
- `id`, `name`, `email` = columns
- Each user record = row

Conceptually:

```text
users
┌────┬─────────┬────────────────────┐
│ id │ name    │ email              │
├────┼─────────┼────────────────────┤
│ 1  │ Daenish │ daenish@example.com│
│ 2  │ Niraj   │ niraj@example.com  │
└────┴─────────┴────────────────────┘
```

We'll learn the exact database keys and relationships in the next lessons.

---

# 7. Example From Our Project

Suppose we have a `skills` table:

| id | name | category |
|---:|---|---|
| 1 | Java | Programming |
| 2 | Spring Boot | Backend |
| 3 | React | Frontend |
| 4 | PostgreSQL | Database |

Then our application can retrieve this information.

For example:

```text
GET /api/skills
```

Spring Boot could retrieve:

```text
Java
Spring Boot
React
PostgreSQL
```

from PostgreSQL.

---

# 8. One Important Problem

Now think about this:

A user can have **multiple skills**.

For example:

```text
Daenish
 ├── Java
 ├── Spring Boot
 ├── React
 └── PostgreSQL
```

And another user can also have:

```text
Niraj
 ├── Java
 ├── React
 └── Docker
```

Should we store everything like this?

```text
users

id | name | skills
1  | Daenish | Java, Spring Boot, React, PostgreSQL
2  | Niraj   | Java, React, Docker
```

This creates problems.

For example:

```text
"Java, Spring Boot, React, PostgreSQL"
```

is multiple pieces of information stored inside one column.

This is one of the problems that proper database design and **normalization** will help us solve.

We'll study normalization in **Lesson 2.11**.

---

# 9. Database Design Is About Relationships Too

It's not enough to know:

```text
Users
Skills
Careers
```

We also need to know:

```text
How is a user connected to a skill?

How is a career connected to a skill?

How is a user connected to an assessment?

How is a user connected to a recommendation?
```

For example:

```text
User ─────── Skills
```

A user can have many skills.

A skill can belong to many users.

That is a **many-to-many relationship**.

We'll study this properly in **Lesson 2.9**.

---

# 10. Database Design for Our Platform

At a high level, our database may eventually contain entities such as:

```text
User
Skill
Career
Assessment
Assessment Result
Learning Resource
Recommendation
```

⚠️ **Don't treat this as our final list yet.**

In **Lesson 2.7**, we'll systematically identify the actual entities from our project requirements.

---

# 11. Database Design vs Database Implementation

These are different.

### Database Design

We decide:

```text
What data?
What tables?
What columns?
What relationships?
What keys?
How should data be organized?
```

### Database Implementation

We actually create:

```sql
CREATE TABLE users (...);
```

We are currently learning **design**, not implementation.

---

# 12. Our Database Design Process

Throughout the next lessons, we'll follow this path:

```text
2.6
Introduction to Database Design
        ↓
2.7
Identify Entities
        ↓
2.8
Primary & Foreign Keys
        ↓
2.9
Relationships
        ↓
2.10
ER Diagram
        ↓
2.11
Normalization
        ↓
2.12
Complete Database Schema
        ↓
2.13
Spring Boot Entity Mapping
```

This is a very important sequence.

**Don't skip ahead to writing SQL yet.**

---

# 🧠 Simple Example

Imagine a small library system.

We might identify:

```text
Student
Book
Borrowing
```

Then:

```text
Student
   ↓
borrows
   ↓
Book
```

We would design tables based on this relationship.

Our project works similarly, but it has more complex entities.

For our platform:

```text
User
   ↓
has
   ↓
Skill
```

and:

```text
User
   ↓
takes
   ↓
Assessment
```

and:

```text
User
   ↓
receives
   ↓
Recommendation
```

We'll formally design these later.

---

# 📄 Proposal-Ready Documentation


### Database Design

Database design is the process of organizing and structuring the data required by the AI Skill & Career Management Platform. It determines what information needs to be stored, how the information will be organized into entities and tables, and how different entities will be related to each other.

The proposed platform requires persistent storage for information such as user profiles, skills, career information, assessments, learning resources, and recommendations. A properly designed PostgreSQL database will ensure that this information can be stored, retrieved, and maintained efficiently.

The database design process will begin by identifying the major entities from the system requirements. Primary keys, foreign keys, relationships, and normalization techniques will then be used to create a structured database schema. This design will provide a reliable foundation for integrating the PostgreSQL database with the Spring Boot backend.


---

