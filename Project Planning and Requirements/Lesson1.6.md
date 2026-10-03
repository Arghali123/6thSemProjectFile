# Lesson 1.6 — Functional Requirements

## 1. What are functional requirements?

A **functional requirement describes what the system must do.**

Think of it as:

> **"What actions should our application provide?"**

For example:

> The system shall allow users to register an account.

That's a functional requirement because it describes something the system must perform.

### Simple difference

| Requirement    | Question                              |
| -------------- | ------------------------------------- |
| Functional     | **What should the system do?**        |
| Non-functional | **How well should the system do it?** |

We'll study non-functional requirements in **Lesson 1.7**.

---

# 2. Example

Suppose we have a registration feature.

### Functional requirement

> The system shall allow users to create an account using their name, email, and password.

### Another example

> The system shall allow users to update their skills.

These describe actual functionality.

---

# 3. Functional requirements for our project

Let's divide them according to system modules.

## A. User Authentication

Our system should:

* Allow users to register.
* Allow users to log in.
* Allow users to log out.
* Validate user credentials.
* Allow users to manage their account.
* Restrict protected features to authenticated users.

---

## B. User Profile Management

Users should be able to:

* Create their profile.
* Update personal information.
* Add skills.
* Remove skills.
* Select interests.
* Specify career preferences.
* View their profile.

### Example

A user could have:

```text
Name: Alex
Education: BSc CSIT
Skills:
  Java
  SQL
  React
Interests:
  Backend Development
  Cloud Computing
```

---

# 4. Skill Assessment

The platform should allow users to take assessments.

### Required functionality

* Display assessment questions.
* Allow users to submit answers.
* Calculate assessment results.
* Store assessment results.
* Display results to the user.
* Use relevant assessment results in career analysis.

### Example

```text
Question:
Which technology is commonly used to build REST APIs
with Spring Boot?

A. Spring MVC
B. Photoshop
C. MySQL Workbench
D. Figma
```

The system evaluates the submitted answer and updates the user's assessment result.

---

# 5. Career Management

The platform should maintain information about different career paths.

For example:

```text
Career: Backend Developer

Required Skills:
- Java
- Spring Boot
- SQL
- REST API
- Git
```

Users should be able to:

* Browse careers.
* View career descriptions.
* View required skills.
* Select career goals.
* View career recommendations.

Administrators should be able to manage career information.

---

# 6. Career Matching Algorithm

This is one of the important technical parts of our project.

The system should:

1. Obtain the user's relevant skills.
2. Obtain the required skills for a career.
3. Compare the two.
4. Calculate a compatibility score.
5. Identify matched skills.
6. Identify missing skills.
7. Display the results.

### Simple example

Career requires:

```text
Java
Spring Boot
SQL
REST API
Git
```

User has:

```text
Java
SQL
Git
```

The system can identify:

```text
Matched:
Java
SQL
Git

Missing:
Spring Boot
REST API
```

The exact scoring formula will be designed later in our **Career & Skill Matching Algorithm** module.

---

# 7. Skill-Gap Analysis

The system should:

* Identify skills required for a selected career.
* Compare them with the user's skills.
* Display missing skills.
* Categorize or prioritize gaps where appropriate.
* Connect identified gaps with learning recommendations.

### Example

```text
Career: Backend Developer

Your Skills:
✓ Java
✓ SQL
✓ Git

Skill Gaps:
○ Spring Boot
○ REST API
○ Unit Testing
```

---

# 8. AI Resume Analysis

This is where AI becomes useful for a real project feature.

The user should be able to upload a resume.

The system can:

1. Receive the resume.
2. Extract relevant text.
3. Send appropriate text to an AI/ML processing component.
4. Identify potential skills.
5. Present extracted skills to the user.
6. Allow the user to review or confirm them.

### Example

Resume contains:

```text
Developed REST APIs using Spring Boot
and worked with PostgreSQL databases.
```

AI-assisted processing may identify:

```text
Skills:
✓ Spring Boot
✓ REST API
✓ PostgreSQL
```

The user should have an opportunity to review extracted information rather than treating AI output as automatically correct.

---

# 9. Learning Recommendations

Based on skill gaps, the platform should provide relevant learning recommendations.

Example:

```text
Skill Gap: Spring Boot

Recommended Learning:
→ Spring Boot Fundamentals
→ REST API Development
→ Spring Boot + PostgreSQL Project
```

Initially, we can use a structured recommendation system based on skill-to-resource relationships. More advanced ML recommendations can be added if time and data permit.

---

# 10. Progress Dashboard

The dashboard should allow users to view important information in one place.

For example:

```text
----------------------------------
       MY DASHBOARD
----------------------------------

Skills:              12

Assessment Score:    78%

Career Match:
Backend Developer    82%

Skill Gaps:          3

Learning Progress:   65%

----------------------------------
```

Possible visualizations:

* Skill progress
* Assessment performance
* Career compatibility
* Learning progress
* Completed recommendations

---

# 11. Payment

If premium functionality is included, the system should:

* Display premium services.
* Allow users to initiate payment.
* Communicate with the payment gateway.
* Verify payment status.
* Record relevant transaction information.
* Provide access to the purchased service after successful verification.

We should decide the exact premium feature and payment provider during the payment module.

---

# 12. Admin functionality

The administrator should be able to:

* Manage users.
* Manage skills.
* Manage careers.
* Manage career requirements.
* Manage assessment questions.
* Manage learning resources.
* View relevant platform information.
* Manage premium services where applicable.

---

# 13. Complete Functional Requirements List

This is the version we can use as the basis for our proposal/SRS.

## Functional Requirements

The proposed AI Skill & Career Management Platform shall provide the following functional requirements:

### 1. User Authentication and Account Management

* The system shall allow users to register an account.
* The system shall allow registered users to log in and log out.
* The system shall validate user credentials.
* The system shall restrict protected resources to authorized users.
* The system shall allow users to manage their account information.

### 2. User Profile Management

* The system shall allow users to create and update their profiles.
* The system shall allow users to add, update, and remove skills.
* The system shall allow users to specify their interests and career preferences.
* The system shall allow users to view their profile information.

### 3. Skill Assessment

* The system shall provide skill-based assessments.
* The system shall display assessment questions to users.
* The system shall allow users to submit their answers.
* The system shall evaluate submitted answers.
* The system shall store assessment results.
* The system shall display assessment results to users.

### 4. Career Management

* The system shall provide information about supported career paths.
* The system shall display the skills required for each career.
* The system shall allow users to select career goals.
* The system shall allow authorized administrators to manage career information and requirements.

### 5. Career Matching

* The system shall compare user skills with career requirements.
* The system shall calculate a career compatibility score using the defined matching algorithm.
* The system shall identify skills that match career requirements.
* The system shall identify relevant skill gaps.
* The system shall display career matching results to users.

### 6. Skill-Gap Analysis

* The system shall identify missing skills for selected or recommended careers.
* The system shall display identified skill gaps to users.
* The system shall associate relevant learning recommendations with identified skill gaps.

### 7. AI-Assisted Resume Analysis

* The system shall allow users to upload supported resume files.
* The system shall extract relevant resume content.
* The system shall use an AI/ML component to identify potential skills from resume content.
* The system shall display extracted skills for user review.
* The system shall allow confirmed information to contribute to the user's skill profile.

### 8. Learning Recommendations

* The system shall provide learning recommendations based on identified skill gaps and career goals.
* The system shall allow users to view recommended learning resources.
* The system shall allow users to track relevant learning progress.

### 9. Dashboard and Progress Tracking

* The system shall provide users with an interactive dashboard.
* The dashboard shall display relevant skill information.
* The dashboard shall display assessment results.
* The dashboard shall display career compatibility information.
* The dashboard shall display learning progress.

### 10. Payment and Premium Services

* The system shall provide selected premium services where applicable.
* The system shall allow users to initiate payments through an integrated payment gateway.
* The system shall verify payment status.
* The system shall record relevant transaction information.
* The system shall provide appropriate premium access after successful payment verification.

### 11. Administration

* The system shall provide an administrative interface.
* Administrators shall be able to manage users.
* Administrators shall be able to manage skills.
* Administrators shall be able to manage careers and career requirements.
* Administrators shall be able to manage assessment questions.
* Administrators shall be able to manage learning resources.
* Administrators shall be able to manage applicable premium services.

### 12. Data Management

* The system shall store user information securely in the database.
* The system shall store skills, career requirements, assessments, learning information, and relevant progress records.
* The system shall maintain appropriate relationships between related data entities.
* The system shall retrieve and update data according to user permissions.

# 14. What we've accomplished

We now have a clear answer to:

> **"What exactly should our application do?"**

Our major functional flow is:

**Register → Profile → Skills/Assessment → Resume Analysis → Career Matching → Skill Gaps → Learning Recommendations → Progress Dashboard**

And administrators manage the underlying:

**Users + Skills + Careers + Assessments + Learning Resources**

---


