# Lesson 1.7 — Non-Functional Requirements

## 1. What are Non-Functional Requirements?

Functional requirements describe:

> **What the system does.**

Non-functional requirements describe:

> **How the system should perform.**

### Simple example

**Functional:**

> The system shall allow users to log in.

**Non-functional:**

> The login process should respond quickly and securely.

So:

```text
Functional       → What?
Non-Functional   → How well?
```

---

# 2. Why are they important?

Imagine our application has all the required features but:

* pages take 20 seconds to load,
* passwords aren't properly protected,
* the application crashes with several users,
* users cannot use it easily on mobile,
* data is lost unexpectedly.

The application technically has the features, but it isn't a good system.

That's why we need non-functional requirements.

---

# 3. Main NFR categories for our project

For our project, we'll focus on:

1. Performance
2. Security
3. Availability
4. Scalability
5. Usability
6. Reliability
7. Maintainability
8. Compatibility
9. Data integrity
10. Backup and recovery

---

# 4. Performance

The application should respond within a reasonable amount of time.

### Example

When a user opens the dashboard:

```text
User → Request → Backend → Database → Response → Dashboard
```

We don't want unnecessary delays.

### Our requirement

> Common user operations should provide responses within an acceptable response time under normal system load.

For measurable testing later, we can define specific response-time targets.

---

# 5. Security 🔐

Security is particularly important because we'll store:

* User information
* Skills
* Assessment results
* Resume information
* Payment-related records

Our system should:

* Secure passwords.
* Use authentication.
* Use authorization.
* Protect APIs.
* Validate user input.
* Prevent unauthorized access.
* Protect sensitive configuration.
* Use HTTPS in production.

For our Spring Boot backend, we'll use **Spring Security**.

---

# 6. Usability

The application should be easy for students to understand.

For example:

Instead of:

```text
Career Compatibility Calculation Result
```

we could present:

```text
Your Career Match

Backend Developer
82%

Skills matched: 8/10
Skill gaps: 2
```

The UI should have:

* Clear navigation
* Understandable messages
* Consistent design
* Simple forms
* Meaningful error messages
* Responsive layouts

---

# 7. Reliability

The system should operate consistently without unexpected failures.

For example:

If a user submits an assessment, the result should not disappear because of a temporary application error.

We should also handle:

* Invalid requests
* Database errors
* AI service failures
* Payment failures
* Network failures

gracefully.

---

# 8. Availability

Availability means:

> **How often the system is accessible and working.**

For example, when deployed to the cloud, users should be able to access the platform whenever the service is expected to be available.

For our semester project, we don't need to promise unrealistic 99.999% availability.

Instead, we can state that the deployed system should remain available under normal operating conditions.

---

# 9. Scalability

Scalability means the application should be capable of handling increased users and data without requiring a complete redesign.

Our architecture helps with this:

```text
React
   ↓
Spring Boot API
   ↓
PostgreSQL
```

Later, we could scale the backend horizontally if required.

For our academic project, we should describe scalability as a design consideration rather than claiming that we've tested thousands of concurrent users.

---

# 10. Maintainability

Our code should be easy for developers to understand and modify.

We'll achieve this through:

* Layered Spring Boot architecture
* Separate frontend components
* Service/repository structure
* Meaningful naming
* Reusable React components
* Documentation
* Git version control
* Environment-based configuration

Example backend structure:

```text
controller
service
repository
entity
dto
security
config
```

---

# 11. Compatibility

Our application should work with commonly used environments.

### Browser

The React application should support modern browsers such as:

* Chrome
* Edge
* Firefox

### Device

The UI should be responsive for:

* Desktop
* Laptop
* Tablet
* Mobile

---

# 12. Data Integrity

Data integrity means:

> **Stored data should remain accurate and consistent.**

For example:

If a user has a skill:

```text
Java
```

the database should maintain the correct relationship between:

```text
User → Skill
```

We'll use PostgreSQL constraints and appropriate relationships to maintain consistency.

---

# 13. Backup & Recovery

Our database contains important project data.

We should therefore consider:

* Database backups
* Recovery procedures
* Persistent storage
* Disaster/error recovery

For our deployed environment, we'll define an appropriate backup approach.

---

# 14. Proposal-ready documentation

This can go directly into your proposal/SRS.

## Non-Functional Requirements

The proposed AI Skill & Career Management Platform shall satisfy the following non-functional requirements:

### 1. Performance

The system should provide timely responses for common user operations under normal operating conditions. Database queries and API operations should be designed efficiently to minimize unnecessary processing and delays.

### 2. Security

The system shall protect user accounts and sensitive information through secure authentication and authorization mechanisms. Passwords shall be securely stored, protected APIs shall require appropriate authorization, and user input shall be validated. Sensitive configuration information shall not be exposed in the source code.

### 3. Usability

The system should provide a simple, intuitive, and user-friendly interface. Navigation, forms, dashboards, assessment results, and career recommendations should be presented in a clear and understandable manner.

### 4. Reliability

The system should handle invalid requests, application errors, database failures, and external service failures gracefully without causing unnecessary data loss or application crashes.

### 5. Availability

The deployed application should remain accessible and operational under normal operating conditions and should provide appropriate handling of service interruptions.

### 6. Scalability

The system architecture should allow the application to accommodate increasing users, skills, career information, and other data without requiring major changes to the overall architecture.

### 7. Maintainability

The application should be developed using a modular and organized architecture so that individual components can be maintained, tested, and extended independently.

### 8. Compatibility

The web application should support commonly used modern web browsers and provide a responsive interface suitable for desktop, tablet, and mobile devices.

### 9. Data Integrity

The system shall maintain accurate and consistent data through appropriate database relationships, constraints, validation, and transaction management.

### 10. Backup and Recovery

The system should support appropriate database backup and recovery mechanisms to reduce the risk of permanent data loss.

### 11. Extensibility

The system architecture should allow additional career categories, skills, learning resources, AI/ML capabilities, and other features to be added in the future without requiring a complete redesign.

### 12. Deployment and Portability

The application should be containerizable using Docker so that the frontend, backend, and supporting services can be deployed consistently across suitable environments.

---

# 15. Functional vs Non-Functional — Remember This

| Functional                     | Non-Functional                                     |
| ------------------------------ | -------------------------------------------------- |
| User can register              | Registration should be secure                      |
| User can take assessment       | Assessment should respond quickly                  |
| User can upload resume         | Upload should validate file type/size              |
| System calculates career match | Calculation should complete within reasonable time |
| User can view dashboard        | Dashboard should be easy to use                    |
| Admin can manage careers       | Admin operations should be authorized              |

### Easy memory trick

> **Functional = WHAT**
> **Non-functional = HOW WELL**

---


