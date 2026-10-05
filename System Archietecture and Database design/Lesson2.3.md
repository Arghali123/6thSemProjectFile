# 📘 Lesson 2.3 — Three-Tier Architecture

## 1. What is Three-Tier Architecture?

Three-tier architecture divides an application into **three logical layers**:

```text
┌─────────────────────────┐
│    Presentation Tier    │
│       React             │
└────────────┬────────────┘
             │
             ▼
┌─────────────────────────┐
│    Application Tier     │
│      Spring Boot        │
└────────────┬────────────┘
             │
             ▼
┌─────────────────────────┐
│       Data Tier         │
│       PostgreSQL        │
└─────────────────────────┘
```

The three tiers are:

1. **Presentation Tier**
2. **Application/Business Tier**
3. **Data Tier**

This architecture is extremely important for our project because our technology stack naturally fits into these layers.

---

# 2. Tier 1 — Presentation Tier

The presentation tier is responsible for **what the user sees and interacts with**.

For our project:

```text
Presentation Tier
        ↓
      React
```

Examples:

```text
Login Page
Registration Page
Dashboard
Skill Assessment
Career Recommendation
Learning Resources
Profile
```

React's job is primarily to:

```text
Display UI
   ↓
Collect user input
   ↓
Send requests
   ↓
Receive responses
   ↓
Display results
```

### Example

User enters:

```text
Java
Spring Boot
PostgreSQL
```

React collects this information and sends it to the backend.

---

# 3. Tier 2 — Application / Business Tier

This is where the **main processing and business rules** live.

For our project:

```text
Application Tier
       ↓
   Spring Boot
```

This layer handles things like:

```text
Authentication
Authorization
Validation
Business Logic
REST APIs
Recommendation processing
AI communication
Database communication
```

For example:

> User wants a career recommendation.

Spring Boot might perform:

```text
Receive request
      ↓
Authenticate user
      ↓
Validate information
      ↓
Retrieve user's skills
      ↓
Analyze skill gap
      ↓
Call AI component if required
      ↓
Prepare recommendation
      ↓
Send response
```

This is why we don't put important business rules only inside React.

---

# 4. Tier 3 — Data Tier

The data tier is responsible for **storing and retrieving persistent data**.

For our project:

```text
Data Tier
    ↓
PostgreSQL
```

Potential data:

```text
Users
Skills
Careers
User Skills
Learning Resources
Assessments
Recommendations
```

For example:

```text
Spring Boot
     ↓
SELECT user skills
     ↓
PostgreSQL
     ↓
User's stored skills
```

PostgreSQL's main responsibility is **data persistence**, not deciding how the application should behave.

---

# 5. Complete Three-Tier Flow

Now combine everything:

```text
                 USER
                   │
                   ▼
       ┌─────────────────────┐
       │  PRESENTATION TIER  │
       │       React         │
       └──────────┬──────────┘
                  │
             HTTP Request
                  │
                  ▼
       ┌─────────────────────┐
       │ APPLICATION TIER    │
       │     Spring Boot     │
       │                     │
       │ Business Logic      │
       │ Authentication      │
       │ Authorization       │
       │ REST APIs           │
       └──────────┬──────────┘
                  │
             Database Query
                  │
                  ▼
       ┌─────────────────────┐
       │      DATA TIER      │
       │     PostgreSQL      │
       └─────────────────────┘
```

And the response travels back:

```text
PostgreSQL
    ↓
Spring Boot
    ↓
React
    ↓
User
```

---

# 6. Real Example From Our Project

Imagine the user opens:

> **My Skills**

### Step 1 — Presentation

User clicks:

```text
"My Skills"
```

React sends:

```text
GET /api/users/me/skills
```

### Step 2 — Application

Spring Boot receives the request.

It might:

```text
Check authentication
        ↓
Identify user
        ↓
Call service
        ↓
Retrieve skills
```

### Step 3 — Data

Spring Boot asks PostgreSQL:

```text
"Give me the skills belonging to this user."
```

PostgreSQL returns the data.

### Step 4 — Back to User

```text
PostgreSQL
    ↓
Spring Boot
    ↓
JSON Response
    ↓
React
    ↓
Skills displayed
```

---

# 7. Why Separate the Three Tiers?

Imagine putting everything together:

```text
React
 ├── UI
 ├── Database queries
 ├── Authentication
 ├── Business logic
 ├── AI logic
 └── Everything else
```

This would quickly become difficult to maintain.

Instead:

```text
React
   ↓
Presentation

Spring Boot
   ↓
Business/Application

PostgreSQL
   ↓
Data
```

Each layer has a clear responsibility.

### Benefits

**1. Maintainability**

Changes in one layer are less likely to affect unrelated layers.

**2. Security**

Database access can be controlled through the backend.

**3. Scalability**

We can scale different components independently when needed.

**4. Team collaboration**

You and Niraj can work on different parts with clearer boundaries.

**5. Testing**

Each layer can be tested independently.

---

# 8. Three-Tier vs Client-Server

These concepts are related but not exactly the same.

### Client-Server

Focuses mainly on:

```text
Client ↔ Server
```

Example:

```text
React ↔ Spring Boot
```

### Three-Tier

Gives us a more detailed structure:

```text
Presentation
     ↓
Application
     ↓
Data
```

For our project:

```text
React
  ↓
Spring Boot
  ↓
PostgreSQL
```

So you can think of **three-tier architecture as a more structured way of organizing our client-server application**.

---

# 9. Important: Three-Tier ≠ Three Physical Servers

This is a common beginner confusion.

Three tiers are **logical layers**.

It does not necessarily mean:

```text
Computer 1 → React
Computer 2 → Spring Boot
Computer 3 → PostgreSQL
```

During development, everything might run on your own computer:

```text
Your Computer

React       → localhost:5173
Spring Boot → localhost:8080
PostgreSQL  → localhost:5432
```

When deployed with Docker, they can also be separate containers:

```text
Docker
├── frontend container
├── backend container
└── postgres container
```

We'll learn deployment architecture later.

---

# 10. Our Project's Three-Tier Architecture

For **AI Skill & Career Management Platform**, our initial mapping is:

| Tier         | Technology  | Main Responsibility            |
| ------------ | ----------- | ------------------------------ |
| Presentation | React       | UI and user interaction        |
| Application  | Spring Boot | APIs, business logic, security |
| Data         | PostgreSQL  | Persistent data storage        |

The AI component is a little different. We will decide exactly where it fits when we reach **Lesson 2.15 — AI/ML Component Architecture**.

---

