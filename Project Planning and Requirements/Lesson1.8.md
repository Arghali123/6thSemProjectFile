# Lesson 1.8 — User Roles & Permissions

## 1. What is a user role?

A **user role** defines what type of user someone is in our system.

For our platform, the two main roles should be:

```text
USER
  │
  ├── Student / Job Seeker
  │
  └── Administrator
```

We should avoid creating too many roles because this is a semester project.

---

# 2. Student / Job Seeker

This is the **main user** of our platform.

They will use the system to manage their skills and explore career opportunities.

### Student can:

* Register
* Login
* Manage profile
* Add/remove skills
* Select interests
* Take assessments
* View assessment results
* Upload resume
* Review extracted skills
* Explore careers
* Select career goals
* View career matches
* View skill gaps
* View learning recommendations
* Track learning progress
* View dashboard
* Purchase premium services, if applicable

### Student cannot:

* Manage other users
* Add/delete system-wide careers
* Modify assessment questions
* Manage all learning resources
* Access administrator functions

---

# 3. Administrator

The administrator manages the platform.

### Admin can:

* Login to admin dashboard
* View users
* Manage users
* Manage skills
* Manage careers
* Manage career requirements
* Manage assessment questions
* Manage learning resources
* Manage premium services
* View system information

### Admin should not:

Normally, an administrator does not need to modify a student's personal assessment answers or impersonate the student's account.

Keeping responsibilities separated makes the system easier to secure and explain.

---

# 4. What are permissions?

A **permission** defines what a particular role is allowed to do.

For example:

```text
Student → View own profile
Admin   → Manage all users
```

This is called **Role-Based Access Control (RBAC)**.

### Simple idea

```text
Role
  ↓
Permissions
  ↓
Allowed actions
```

---

# 5. Example of RBAC

Imagine our backend has:

```text
GET /api/users/me
```

A logged-in student can access their own profile.

But:

```text
DELETE /api/admin/users/{id}
```

should only be accessible to an administrator.

So:

```text
Student
   ❌ DELETE /api/admin/users/{id}

Admin
   ✅ DELETE /api/admin/users/{id}
```

Spring Security will help us implement this later.

---

# 6. Permission Matrix

This is an important table for our proposal.

| Function                    | Student | Admin |
| --------------------------- | :-----: | :---: |
| Register                    |    ✅    |   —   |
| Login                       |    ✅    |   ✅   |
| Manage own profile          |    ✅    |   —   |
| Manage own skills           |    ✅    |   —   |
| Take assessment             |    ✅    |   —   |
| View own results            |    ✅    |   —   |
| Upload resume               |    ✅    |   —   |
| Analyze resume              |    ✅    |   —   |
| Explore careers             |    ✅    |   ✅   |
| View career requirements    |    ✅    |   ✅   |
| Manage careers              |    ❌    |   ✅   |
| View skill gaps             |    ✅    |   —   |
| View recommendations        |    ✅    |   —   |
| Track learning progress     |    ✅    |   —   |
| Manage learning resources   |    ❌    |   ✅   |
| Manage assessment questions |    ❌    |   ✅   |
| Manage users                |    ❌    |   ✅   |
| Manage skills               |    ❌    |   ✅   |
| Manage premium services     |    ❌    |   ✅   |
| Access admin dashboard      |    ❌    |   ✅   |

**— = not a normal role responsibility**

---

# 7. Authentication vs Authorization

These two terms are very important for your project.

### Authentication

> **Who are you?**

Example:

```text
Email + Password
       ↓
Login
       ↓
User authenticated
```

### Authorization

> **What are you allowed to do?**

Example:

```text
Authenticated User
       ↓
Role = STUDENT
       ↓
Can access student features
       ↓
Cannot access admin APIs
```

### Easy way to remember

**Authentication = Identity**

**Authorization = Permission**

---

# 8. How this fits Spring Boot

Later, our backend can have roles such as:

```text
STUDENT
ADMIN
```

A user record might conceptually look like:

```text
User
----------------
id
name
email
password
role
```

For example:

```text
Alex
alex@email.com
STUDENT
```

and:

```text
Admin
admin@email.com
ADMIN
```

Then Spring Security can protect endpoints according to the user's role.

For example:

```text
/api/student/**  → STUDENT
/api/admin/**    → ADMIN
```

The exact API structure will be designed during the backend module.

---

# 9. Proposal-ready documentation

## User Roles and Permissions

The proposed AI Skill & Career Management Platform will primarily consist of two user roles: **Student/Job Seeker** and **Administrator**. Role-Based Access Control (RBAC) will be used to restrict system functionality according to the permissions assigned to each role.

### 1. Student / Job Seeker

The Student/Job Seeker is the primary user of the platform. This role will have access to features related to personal skill development and career management.

The Student/Job Seeker shall be able to:

* Register and authenticate with the system.
* Create and update their personal profile.
* Add, update, and remove their skills.
* Specify interests and career preferences.
* Complete skill assessments.
* View their assessment results.
* Upload resumes for AI-assisted analysis.
* Review skills extracted from their resumes.
* Explore available career paths and their requirements.
* View career matching results.
* View identified skill gaps.
* Receive learning recommendations.
* Track learning and skill-development progress.
* Access their personalized dashboard.
* Access selected premium services after successful payment, where applicable.

The Student/Job Seeker shall not have permission to manage other users, system-wide career information, assessment questions, or administrative resources.

### 2. Administrator

The Administrator is responsible for managing and maintaining platform-level information and functionality.

The Administrator shall be able to:

* Authenticate through the administrative account.
* Access the administrative dashboard.
* View and manage users.
* Manage skills and skill information.
* Manage career paths and career requirements.
* Manage assessment questions.
* Manage learning resources.
* Manage applicable premium services.
* Perform other authorized administrative operations.

Administrative functions shall be protected from normal student accounts.

### 3. Role-Based Access Control

The system shall implement role-based access control to ensure that users can access only the functionality permitted by their assigned roles.

Authentication will determine the identity of a user, while authorization will determine whether the authenticated user has permission to perform a particular operation.

The proposed system will initially use the following roles:

* **STUDENT**
* **ADMIN**

This role structure provides a simple and manageable access-control model while allowing additional roles to be introduced in the future if required.

---

# 10. Simple architecture view

Our authorization flow will eventually look like this:

```text
                 User
                  │
                  ▼
             Login Request
                  │
                  ▼
          Authentication
                  │
                  ▼
            User + Role
                  │
          ┌───────┴───────┐
          ▼               ▼
       STUDENT           ADMIN
          │               │
          ▼               ▼
 Student APIs          Admin APIs
          │               │
          └───────┬───────┘
                  ▼
              Database
```

This will connect nicely with the **Spring Security** work we'll do later.

---

