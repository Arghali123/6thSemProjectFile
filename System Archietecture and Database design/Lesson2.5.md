# 📘 Lesson 2.5 — Understanding REST API Communication

This lesson is extremely important because **REST API is the communication bridge between our React frontend and Spring Boot backend.**

Our architecture currently looks like:

```text
React
   │
   │ REST API
   ▼
Spring Boot
```

Let's understand exactly what happens here.

---

# 1. What is an API?

**API = Application Programming Interface**

An API provides a way for two software components to communicate with each other.

Think about a restaurant again.

```text
Customer
   ↓
Waiter
   ↓
Kitchen
```

The customer doesn't directly enter the kitchen.

The waiter acts as the communication interface.

In our application:

```text
React
   ↓
REST API
   ↓
Spring Boot
```

The REST API acts like the **communication interface**.

---

# 2. What is REST?

**REST = Representational State Transfer**

Don't worry about the complicated name.

For our project, simply remember:

> **REST is an architectural style commonly used to build APIs that allow applications to communicate over HTTP.**

Our React application can communicate with Spring Boot using HTTP requests.

For example:

```text
GET
POST
PUT
DELETE
```

These are called **HTTP methods**.

---

# 3. Basic REST Communication

Suppose our user wants to see their skills.

The flow is:

```text
User
 ↓
React
 ↓
GET request
 ↓
Spring Boot
 ↓
PostgreSQL
 ↓
Spring Boot
 ↓
JSON response
 ↓
React
 ↓
User
```

For example:

```text
GET /api/skills
```

Spring Boot processes this request and returns data.

---

# 4. HTTP Methods

There are four HTTP methods that you should understand first.

| Method | Common Purpose   |
| ------ | ---------------- |
| GET    | Retrieve data    |
| POST   | Create/send data |
| PUT    | Update data      |
| DELETE | Delete data      |

A simple memory trick:

```text
GET    → Give me data
POST   → Create something
PUT    → Update something
DELETE → Remove something
```

---

# 5. GET Example

Suppose the user wants to see all available skills.

React sends:

```http
GET /api/skills
```

Spring Boot might return:

```json
[
  {
    "id": 1,
    "name": "Java"
  },
  {
    "id": 2,
    "name": "Spring Boot"
  },
  {
    "id": 3,
    "name": "React"
  }
]
```

React then displays:

```text
Available Skills

Java
Spring Boot
React
```

So:

```text
GET = Retrieve information
```

---

# 6. POST Example

Suppose a user wants to register.

React sends:

```http
POST /api/auth/register
```

with data such as:

```json
{
  "name": "Daenish",
  "email": "user@example.com",
  "password": "********"
}
```

Spring Boot:

```text
Receive request
      ↓
Validate data
      ↓
Check existing user
      ↓
Create user
      ↓
Save to PostgreSQL
      ↓
Return response
```

So:

```text
POST = Create/send information
```

---

# 7. PUT Example

Suppose a user changes their profile.

React sends:

```http
PUT /api/users/15
```

with:

```json
{
  "name": "Daenish",
  "careerGoal": "Java Backend Developer"
}
```

Spring Boot updates the corresponding information.

So:

```text
PUT = Update existing information
```

---

# 8. DELETE Example

Suppose the user wants to delete a saved learning resource.

React might send:

```http
DELETE /api/learning-resources/25
```

Spring Boot:

```text
Receive request
      ↓
Check authentication
      ↓
Check authorization
      ↓
Delete resource
      ↓
Return response
```

So:

```text
DELETE = Remove information
```

---

# 9. What is an Endpoint?

An **endpoint** is a specific URL through which a client can access a backend operation.

For example:

```text
/api/skills
```

could be an endpoint.

Our project might eventually have endpoints such as:

```text
/api/auth/register
/api/auth/login

/api/users/me
/api/users/me/skills

/api/skills
/api/careers

/api/assessments
/api/recommendations
/api/learning-resources
```

⚠️ These are **examples for learning right now**, not our final API design.

We'll formally design our endpoint structure in **Lesson 2.14**.

---

# 10. What is JSON?

React and Spring Boot need a common format for exchanging data.

One very common format is:

**JSON = JavaScript Object Notation**

Example:

```json
{
  "name": "Java",
  "level": "Intermediate",
  "yearsOfExperience": 2
}
```

Spring Boot can send JSON:

```text
Spring Boot
     ↓
   JSON
     ↓
React
```

React can also send JSON:

```text
React
  ↓
 JSON
  ↓
Spring Boot
```

This is why you'll see JSON everywhere when working with REST APIs.

---

# 11. Complete Example From Our Project

Let's use an actual feature:

> **User wants to view their skills.**

### Step 1 — User

```text
User clicks "My Skills"
```

### Step 2 — React

React sends:

```http
GET /api/users/me/skills
```

### Step 3 — Spring Boot

Spring Boot receives the request:

```text
Controller
   ↓
Service
   ↓
Repository
```

### Step 4 — PostgreSQL

Repository communicates with PostgreSQL:

```text
PostgreSQL
    ↓
User's skills
```

### Step 5 — Spring Boot

Spring Boot converts the result into JSON:

```json
[
  {
    "name": "Java",
    "level": "Advanced"
  },
  {
    "name": "Spring Boot",
    "level": "Intermediate"
  }
]
```

### Step 6 — React

React receives the JSON and displays:

```text
My Skills

Java             Advanced
Spring Boot      Intermediate
```

Complete flow:

```text
             REQUEST
React ──────────────────► Spring Boot
                              │
                              ▼
                         PostgreSQL
                              │
                              ▼
React ◄────────────────── Spring Boot
             RESPONSE
```

---

# 12. REST API in Our Architecture

Now our architecture becomes more understandable:

```text
┌───────────────┐
│     React     │
│   Frontend    │
└───────┬───────┘
        │
        │ REST API
        │ HTTP
        ▼
┌───────────────┐
│ Spring Boot   │
│   Backend     │
└───────┬───────┘
        │
        ├──────────────► PostgreSQL
        │
        └──────────────► AI/ML
```

This REST API layer is the **bridge between our frontend and backend**.

---

# 13. Important Concept: Frontend Doesn't Call Repository

A beginner mistake would be thinking:

```text
React
 ↓
Repository
 ↓
PostgreSQL
```

That's not our architecture.

Instead:

```text
React
 ↓
REST API
 ↓
Controller
 ↓
Service
 ↓
Repository
 ↓
PostgreSQL
```

We'll learn this Spring Boot structure in more detail later.

---

# 🧠 Remember These 6 Things

For this lesson, remember:

```text
API
→ Communication interface

REST
→ Architecture style for APIs

HTTP
→ Communication protocol

GET
→ Retrieve

POST
→ Create

PUT
→ Update

DELETE
→ Delete
```

And:

```text
React
   ↓
REST API
   ↓
Spring Boot
   ↓
PostgreSQL
```

---


