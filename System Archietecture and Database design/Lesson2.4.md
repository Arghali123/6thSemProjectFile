# 📘 Lesson 2.4 — Designing Our Project Architecture

This is where we stop discussing architecture only in theory and start designing the architecture of our actual **AI Skill & Career Management Platform**.


# 1. What Are We Designing?

Our project is:

> **AI Skill & Career Management Platform**

The system should allow users to manage their skills and receive intelligent career/learning recommendations.

From Module 1, we already identified the major functionality.

Conceptually:

```text
User
 │
 ├── Manage Profile
 ├── Manage Skills
 ├── Take Assessments
 ├── Explore Careers
 ├── Identify Skill Gaps
 ├── Get Career Recommendations
 └── Get Learning Recommendations
```

Now we need to decide:

> **Which part of our system handles each responsibility?**

---

# 2. Our Initial Architecture

Our architecture will initially look like this:

```text
                         USER
                           │
                           ▼
                  ┌─────────────────┐
                  │  React Frontend │
                  │  Presentation   │
                  │      Tier       │
                  └────────┬────────┘
                           │
                       REST API
                           │
                           ▼
                  ┌─────────────────┐
                  │  Spring Boot    │
                  │ Application Tier│
                  └───────┬─┬───────┘
                          │ │
             ┌────────────┘ └─────────────┐
             │                            │
             ▼                            ▼
      ┌──────────────┐            ┌──────────────┐
      │  PostgreSQL  │            │   AI / ML    │
      │  Data Tier   │            │   Component  │
      └──────────────┘            └──────────────┘
```

This is our **initial architecture**, not the final architecture.

We'll refine it throughout Module 2.

---

# 3. Component 1 — React Frontend

React is responsible for the **user-facing part** of the system.

For example:

```text
React
 │
 ├── Login
 ├── Registration
 ├── Dashboard
 ├── User Profile
 ├── Skills
 ├── Skill Assessment
 ├── Career Exploration
 ├── Recommendations
 └── Learning Resources
```

The user interacts with React.

For example:

```text
User
 ↓
Clicks "Get Career Recommendation"
 ↓
React
```

React then communicates with Spring Boot.

```text
React
   │
   │ HTTP Request
   ▼
Spring Boot
```

---

# 4. Component 2 — Spring Boot Backend

Spring Boot is the **core application layer**.

It will be responsible for:

```text
Spring Boot
 │
 ├── REST APIs
 ├── Authentication
 ├── Authorization
 ├── Business Logic
 ├── Validation
 ├── User Management
 ├── Skill Management
 ├── Career Management
 ├── Assessment Management
 ├── Recommendation Processing
 ├── Database Communication
 └── AI Communication
```

Think of Spring Boot as the **brain/coordinator of the application**.

For example:

```text
React
  ↓
"Give me career recommendations"
  ↓
Spring Boot
  ↓
Does user have permission?
  ↓
Get user information
  ↓
Get user's skills
  ↓
Analyze required information
  ↓
Call AI if necessary
  ↓
Prepare response
  ↓
React
```

---

# 5. Component 3 — PostgreSQL

PostgreSQL will store the application's persistent data.

At this stage, we don't know our exact tables yet.

We'll design those in **Lessons 2.6–2.12**.

But conceptually, we may have data such as:

```text
Users
Skills
Careers
User Skills
Assessments
Assessment Results
Learning Resources
Recommendations
```

For example:

```text
Spring Boot
     │
     │ SQL / JPA
     ▼
PostgreSQL
     │
     ▼
User's stored skills
```

---

# 6. Component 4 — AI/ML

Our platform is called an **AI Skill & Career Management Platform**, so AI is an important component.

Potential AI responsibilities include:

### Skill Gap Analysis

```text
User Skills
     +
Required Career Skills
     ↓
AI
     ↓
Missing Skills
```

Example:

```text
Career: Java Backend Developer

User has:
✓ Java
✓ Spring Boot
✓ PostgreSQL

Missing:
✗ Docker
✗ Kubernetes
✗ Microservices
```

### Career Recommendation

```text
User Profile
     +
Skills
     +
Assessment Results
     ↓
AI
     ↓
Recommended Careers
```

### Learning Recommendation

```text
Skill Gap
   ↓
AI
   ↓
Recommended Learning Resources
```

We'll design exactly how this AI component communicates with Spring Boot in **Lesson 2.15**.

---

# 7. Why Does Spring Boot Sit Between React and AI?

We could technically have:

```text
React → AI
```

But for our architecture, we want:

```text
React
  ↓
Spring Boot
  ↓
AI
```

Why?

Because Spring Boot can control:

```text
Authentication
Authorization
Validation
AI request preparation
AI response processing
Error handling
Business rules
```

This gives us a much cleaner architecture.

---

# 8. Example: Career Recommendation Flow

Let's design one actual feature.

### User action

```text
User clicks:

"Recommend Careers"
```

### Step 1 — React

React collects the necessary information and sends:

```text
POST /api/recommendations/careers
```

We'll design our exact API structure later.

### Step 2 — Spring Boot

Spring Boot receives the request.

```text
Request
  ↓
Authentication
  ↓
Validation
  ↓
Get user information
  ↓
Get relevant database data
```

### Step 3 — AI

Spring Boot sends appropriate information to the AI component.

```text
Spring Boot
     ↓
User Skills
Assessment Results
Career Information
     ↓
AI
```

### Step 4 — AI Response

AI produces recommendations.

```text
AI
 ↓
Career Recommendations
 ↓
Spring Boot
```

### Step 5 — Response to React

```text
Spring Boot
     ↓
JSON Response
     ↓
React
     ↓
Display recommendation
     ↓
User
```

Complete flow:

```text
User
 ↓
React
 ↓
Spring Boot
 ├──────────→ PostgreSQL
 │                │
 │                └── Data
 │
 └──────────→ AI
                  │
                  └── Recommendation
 ↓
React
 ↓
User
```

---

# 9. Architecture by Responsibility

This is something you should remember for your project presentation.

| Component       | Main Responsibility                      |
| --------------- | ---------------------------------------- |
| **React**       | User interface and interaction           |
| **Spring Boot** | Business logic and system coordination   |
| **PostgreSQL**  | Persistent data storage                  |
| **AI/ML**       | Intelligent analysis and recommendations |
| **Git/GitHub**  | Version control and collaboration        |
| **Docker**      | Application packaging and deployment     |
| **CI/CD**       | Automated build, test and deployment     |

Notice something important:

**Git, Docker and CI/CD are not application tiers.**

They support the development and deployment of the system.

---

# 10. Development Architecture vs Deployment Architecture

Don't confuse these two.

### Development architecture

When you're developing locally:

```text
Your Computer
│
├── React
├── Spring Boot
├── PostgreSQL
└── AI component
```

### Deployment architecture

Later, Docker/CI/CD may organize these components differently:

```text
Server
│
├── React Container
├── Spring Boot Container
├── PostgreSQL Container
└── AI Service/Container
```

We'll deal with deployment architecture later.

For now, our focus is the **logical application architecture**.

---

# 11. Our First Architecture Diagram

This is the architecture we currently understand:

```text
                         ┌──────────────┐
                         │     USER     │
                         └──────┬───────┘
                                │
                                ▼
                    ┌─────────────────────┐
                    │    REACT FRONTEND   │
                    │  Presentation Tier  │
                    └──────────┬──────────┘
                               │
                         REST / HTTP
                               │
                               ▼
                    ┌─────────────────────┐
                    │    SPRING BOOT      │
                    │  Application Tier   │
                    │                     │
                    │ Business Logic      │
                    │ Security            │
                    │ REST APIs           │
                    └──────┬───────┬──────┘
                           │       │
                    Database       │ AI Request
                           │       │
                           ▼       ▼
                  ┌────────────┐ ┌───────────┐
                  │ PostgreSQL │ │  AI / ML  │
                  │ Data Tier  │ │ Component │
                  └────────────┘ └───────────┘
```

**This is not our final diagram yet.**

In Lesson 2.17, we'll create the **final system architecture diagram** after we've learned all the required components.

---

# 12. A Very Important Design Principle

We want **loose coupling** between components.

For example:

```text
React
  ↓
API
  ↓
Spring Boot
  ↓
Database
```

React should not need to know:

```text
How PostgreSQL stores data
```

Similarly, React shouldn't care:

```text
How the AI model works internally
```

React only needs a clear API contract.

This makes it easier to change components later.

For example, if we replace:

```text
AI Service A
```

with:

```text
AI Service B
```

React ideally shouldn't need major changes.

---

