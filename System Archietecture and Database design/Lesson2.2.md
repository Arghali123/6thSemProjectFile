# 📘 Lesson 2.2 — Understanding Client-Server Architecture


## 1. What is Client-Server Architecture?

Client-server architecture is a model where a system is divided into two main sides:

```text
CLIENT  ↔  SERVER
```

### Client

The **client** is the part that the user directly interacts with.

In our project:

```text
React = Client
```

It provides:

* Login/Register pages
* Dashboard
* Career pages
* Skill pages
* Forms
* Recommendations
* Buttons and other UI elements

### Server

The **server** receives requests from the client, processes them, and sends responses back.

In our project:

```text
Spring Boot = Server
```

It handles:

* Business logic
* Authentication
* Authorization
* REST APIs
* Database operations
* AI communication

---

# 2. Simple Real-Life Example

Think about a restaurant.

```text
Customer → Waiter → Kitchen
```

The customer doesn't directly enter the kitchen.

Instead:

```text
Customer
   ↓
places order
   ↓
Waiter
   ↓
Kitchen
   ↓
prepares food
   ↓
Waiter
   ↓
Customer
```

Similarly, our application works like:

```text
User
 ↓
React
 ↓
Spring Boot
 ↓
PostgreSQL
```

React doesn't directly manipulate the PostgreSQL database.

---

# 3. Our Project's Client-Server Model

For our project:

```text
┌──────────────────────┐
│       USER           │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│   React Frontend     │
│      CLIENT          │
└──────────┬───────────┘
           │
           │ HTTP Request
           ▼
┌──────────────────────┐
│   Spring Boot        │
│       SERVER         │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│     PostgreSQL       │
│      DATABASE        │
└──────────────────────┘
```

Later, our AI component will also communicate with the backend.

---

# 4. What is a Request?

Suppose the user clicks:

> **"View My Skills"**

React needs the user's skill information.

It sends a request to Spring Boot.

For example:

```text
GET /api/skills/my-skills
```

The flow becomes:

```text
User
 ↓
Click "My Skills"
 ↓
React
 ↓
HTTP Request
 ↓
Spring Boot
 ↓
Database
```

---

# 5. What is a Response?

After Spring Boot gets the required information from PostgreSQL, it sends a response back.

For example:

```json
{
  "user": "Daenish",
  "skills": [
    "Java",
    "Spring Boot",
    "React",
    "PostgreSQL"
  ]
}
```

Then:

```text
Spring Boot
     ↓
   Response
     ↓
   React
     ↓
 Display skills
     ↓
    User
```

So the basic cycle is:

```text
REQUEST
   ↓
Client → Server
   ↓
Processing
   ↓
Server → Client
   ↓
RESPONSE
```

---

# 6. Another Example From Our Project

Suppose our platform has:

> **"Get Career Recommendation"**

The user clicks the button.

### Step 1 — User

```text
Click "Get Recommendation"
```

### Step 2 — React

React sends:

```text
POST /api/recommendations
```

with information such as the user's selected skills.

### Step 3 — Spring Boot

Spring Boot:

```text
Receive request
      ↓
Validate user
      ↓
Apply business logic
      ↓
Get required data
      ↓
Communicate with AI
```

### Step 4 — AI

The AI component analyzes the information and generates a recommendation.

### Step 5 — Spring Boot

Spring Boot processes the AI result and returns it to React.

### Step 6 — React

React displays:

```text
Recommended Career
        ↓
Java Backend Developer

Skill Gap
        ↓
Docker
Kubernetes
Microservices
```

The complete flow:

```text
User
 ↓
React
 ↓
Spring Boot
 ↓
AI
 ↓
Spring Boot
 ↓
React
 ↓
User
```

---

# 7. Why Don't We Let React Talk Directly to PostgreSQL?

This is **very important**.

We don't want:

```text
React ─────────→ PostgreSQL
```

Instead:

```text
React → Spring Boot → PostgreSQL
```

Why?

### Security 🔐

If React directly accessed the database, database credentials and access mechanisms could potentially be exposed to the client.

### Business Logic

Suppose we have:

```text
User wants to delete account
```

Spring Boot can check:

```text
Is the user authenticated?
        ↓
Is the user authorized?
        ↓
Can this user delete this account?
        ↓
Perform deletion
```

### Validation

The backend can validate incoming data before storing it.

### Centralized API

React doesn't need to know how PostgreSQL works.

It only needs to know:

```text
Which API should I call?
What data should I send?
What response will I receive?
```

---

# 8. Client and Server Have Different Responsibilities

This distinction will become very important when we build the project.

| Client — React    | Server — Spring Boot |
| ----------------- | -------------------- |
| User interface    | Business logic       |
| Forms             | Authentication       |
| Buttons           | Authorization        |
| Display data      | Validation           |
| User interaction  | Database operations  |
| Send API requests | REST APIs            |
| Display responses | AI communication     |

Think:

> **React = Presentation and interaction**

> **Spring Boot = Processing and business logic**

---

# 9. Is the Database a Server?

You may wonder:

> "If PostgreSQL receives requests, isn't PostgreSQL also a server?"

Technically, **PostgreSQL runs as a database server**.

But when we discuss our application's **client-server architecture**, we usually consider:

```text
React = Client
Spring Boot = Application Server
PostgreSQL = Database Server
```

This distinction will become clearer when we study **Three-Tier Architecture in Lesson 2.3**.

---

# 10. Where Does the Internet Come In?

When deployed, our architecture could look like:

```text
User's Browser
      │
      │ HTTPS
      ▼
React Application
      │
      │ REST API
      ▼
Spring Boot Server
      │
      ├──────────────► PostgreSQL
      │
      └──────────────► AI Service
```

For local development, it might instead look like:

```text
Browser
   │
   ▼
localhost:5173
React
   │
   ▼
localhost:8080
Spring Boot
   │
   ▼
localhost:5432
PostgreSQL
```

The ports are just examples based on a typical development setup.

---

# 11. Key Concept: Separation of Responsibilities

The biggest idea to remember from this lesson is:

```text
             OUR SYSTEM

        ┌───────────────┐
        │     React     │
        │    CLIENT     │
        └───────┬───────┘
                │
             HTTP
                │
                ▼
        ┌───────────────┐
        │ Spring Boot   │
        │    SERVER     │
        └───────┬───────┘
                │
              Data
                │
                ▼
        ┌───────────────┐
        │  PostgreSQL   │
        │   DATABASE    │
        └───────────────┘
```

Each component has a **specific responsibility**.

This makes the application easier to:

* Develop
* Test
* Maintain
* Secure
* Scale
* Deploy

---


