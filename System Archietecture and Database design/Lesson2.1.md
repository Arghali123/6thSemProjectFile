# 2.1 — Introduction to System Architecture

Before designing our database or writing backend code, we need to understand **how all parts of our project will work together**.

## 1. What is System Architecture?

**System architecture is the overall blueprint of a software system.**

It describes:

* What components our system contains
* What each component does
* How components communicate
* Where data is stored
* How users interact with the system
* How external services such as AI communicate with our application

Think of it like the **blueprint of a house**.

Before building a house, you decide:

```text
Where is the bedroom?
Where is the kitchen?
Where is the bathroom?
How are rooms connected?
Where are electricity and water lines?
```

Similarly, before building our software, we decide:

```text
Where is React?
Where is Spring Boot?
Where is PostgreSQL?
Where is the AI component?
How does React communicate with Spring Boot?
How does Spring Boot communicate with PostgreSQL?
How does Spring Boot communicate with AI?
```

---

# 2. Our Project's Main Components

Our **AI Skill & Career Management Platform** will have several major components.

At a high level:

```text
                USER
                 │
                 ▼
        ┌─────────────────┐
        │ React Frontend  │
        └────────┬────────┘
                 │
                 │ HTTP / REST API
                 ▼
        ┌─────────────────┐
        │ Spring Boot     │
        │ Backend         │
        └───────┬─────────┘
                │
        ┌───────┴──────────┐
        │                  │
        ▼                  ▼
┌───────────────┐   ┌───────────────┐
│ PostgreSQL    │   │ AI/ML         │
│ Database      │   │ Component     │
└───────────────┘   └───────────────┘
```

Don't worry about the details yet. **We will design this properly in Lessons 2.4 onward.**

---

# 3. Why Do We Need Architecture?

Without architecture, developers may start coding immediately:

```text
Niraj → writes some backend code
You → write some React code
Someone → creates database tables
Someone → adds AI
```

Eventually, problems can appear:

```text
❌ Frontend doesn't know which API to call
❌ Backend structure becomes confusing
❌ Database relationships are unclear
❌ AI component doesn't have a clear communication method
❌ Security responsibilities are unclear
❌ Adding new features becomes difficult
```

Architecture gives everyone a **common plan**.

---

# 4. Architecture Helps You and Niraj Work Together

This is especially important because you're developing the project as a team.

For example, you could divide responsibilities like:

```text
                 PROJECT
                    │
        ┌───────────┴───────────┐
        │                       │
   FRONTEND                  BACKEND
     You?                     Niraj?
        │                       │
     React                  Spring Boot
        │                       │
        └────────── API ────────┘
                    │
                PostgreSQL
```

The exact division doesn't matter yet.

The important point is that **both developers understand the boundaries between components**.

---

# 5. Architecture vs Code

This is an important distinction.

### Code

Code answers:

> "How do I implement this feature?"

For example:

```java
@GetMapping("/skills")
public List<Skill> getSkills() {
    return skillService.getAllSkills();
}
```

### Architecture

Architecture answers:

> "Where should this functionality live and how should components communicate?"

For example:

```text
React
  ↓
REST API
  ↓
Spring Boot Controller
  ↓
Service
  ↓
Repository
  ↓
PostgreSQL
```

So:

**Architecture comes before detailed implementation.**

---

# 6. Architecture of Our Actual Project

Let's think about one feature from our platform.

Suppose a user wants:

> **"Show me the skills I need to become a Java Backend Developer."**

A simplified flow could be:

```text
User
 │
 │ clicks "Career Recommendation"
 ▼
React Frontend
 │
 │ GET /api/careers/java-backend
 ▼
Spring Boot Backend
 │
 ├── checks user information
 │
 ├── gets required skills
 │
 └── requests AI recommendation if needed
 │
 ├───────────────┐
 ▼               ▼
PostgreSQL      AI Component
 │               │
 └───────┬───────┘
         ▼
   Spring Boot
         │
         ▼
   React Frontend
         │
         ▼
        User
```

This is architecture thinking.

We aren't implementing it yet. We're first deciding **how the system should work**.

---

# 7. Important Architecture Components

For our project, we'll eventually design these areas:

### Frontend

```text
React
```

Responsible for:

* User interface
* Forms
* Dashboards
* Skill visualization
* Career recommendations display
* Sending API requests

### Backend

```text
Spring Boot
```

Responsible for:

* Business logic
* Authentication/authorization
* REST APIs
* User management
* Skill management
* Career management
* Recommendation processing

### Database

```text
PostgreSQL
```

Responsible for persistent data such as:

```text
Users
Skills
Careers
User Skills
Learning Resources
Recommendations
Assessments
...
```

We'll identify the exact entities later in **Lesson 2.7**.

### AI/ML

```text
Python / AI Service
```

Potential responsibilities:

* Skill recommendations
* Career recommendations
* Skill-gap analysis
* Personalized learning suggestions

We'll design this properly in **Lesson 2.15**.

---

# 8. A Simple Mental Model

Remember this:

```text
USER
  ↓
REACT
  ↓
SPRING BOOT
  ↓
POSTGRESQL
```

And when AI is needed:

```text
USER
  ↓
REACT
  ↓
SPRING BOOT
  ↓
AI
  ↓
SPRING BOOT
  ↓
REACT
  ↓
USER
```

This is only our **initial conceptual architecture**.

We will improve it throughout Module 2.

---

# 9. Proposal-Ready Documentation

You can use the following idea in your project proposal.

### System Architecture

System architecture defines the overall structure and organization of the AI Skill & Career Management Platform. It describes the major components of the system, their responsibilities, and the communication between them.

The proposed system consists of a React-based frontend, a Spring Boot backend, a PostgreSQL database, and an AI/ML component. The React frontend provides the user interface through which users interact with the platform. The Spring Boot backend manages business logic, authentication, REST APIs, and communication with other system components. PostgreSQL is used for persistent storage of user, skill, career, learning, and recommendation-related data. The AI/ML component is responsible for intelligent features such as skill-gap analysis, career recommendations, and personalized learning recommendations.

The major components communicate through well-defined interfaces. The frontend communicates with the backend through REST APIs, while the backend communicates with the PostgreSQL database and the AI/ML component as required.

This architectural approach provides a structured, maintainable, scalable, and modular foundation for the development of the AI Skill & Career Management Platform.

---


