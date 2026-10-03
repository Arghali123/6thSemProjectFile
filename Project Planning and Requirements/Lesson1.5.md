# Lesson 1.5 — Proposed System

## 1. What is a proposed system?

A proposed system describes the solution we intend to develop to address the problems identified in Lesson 1.4.

In simple words:

* Existing System: What solutions are currently available?

* Limitations: What challenges remain for our intended users?

* Proposed System: What will our application do to address those challenges?

### Example

Problem: Students struggle to identify missing skills for a career.

Proposed solution: Our application compares a student's skills with predefined career requirements and displays skill gaps with suggested learning activities.

## 2. Our proposed system

Our AI Skill & Career Management Platform will be a web-based application designed to help students and job seekers manage their skills, explore career paths, and plan professional development.

The platform will combine:

* User profile and skill management

* Skill assessment

* Career matching algorithm

* Skill-gap analysis

* AI-assisted resume analysis

* Personalized learning recommendations

* Progress dashboard

* Admin management

* Optional premium services and payment integration

The system will use React for the frontend, Spring Boot for the backend, and PostgreSQL for data storage.

## 3. How will our system work?

Let's understand the workflow from a student's perspective.

Step 1: User Registration

The student creates an account and completes their profile.

Step 2: Skill Assessment

The user provides skills, interests, and assessment responses.

Step 3: AI & Algorithm Processing

The system analyzes relevant profile information and compares skills with career requirements.

Step 4: Career Matching

The system calculates compatibility scores for supported career paths.

Step 5: Skill-Gap Analysis

The user sees skills they have and skills they may need to develop.

Step 6: Learning Recommendations

The platform suggests learning resources and activities based on identified gaps.

Step 7: Progress Dashboard

The user tracks assessments, skill development, and learning progress.

## 4. Proposed system architecture

Since we are using React, Spring Boot, and PostgreSQL, our application will follow a three-tier architecture.

### What is three-tier architecture?

It separates an application into three main layers:

| Layer              | Technology  | Responsibility                                      |
| ------------------ | ----------- | --------------------------------------------------- |
| Presentation Layer | React       | User interface                                      |
| Application Layer  | Spring Boot | Business logic, authentication, APIs, algorithms    |
| Data Layer         | PostgreSQL  | Store users, skills, assessments, and other records |

### Architecture overview

Presentation Layer

## React

Student dashboard · Admin dashboard · Forms · Charts

HTTPS / REST API

Application Layer

## Spring Boot

Authentication · User management · Career algorithm · AI integration · Business logic

Spring Data JPA / SQL

Data Layer

## PostgreSQL

Users · Skills · Careers · Assessments · Learning plans · Progress

### Where will AI/ML fit?

AI/ML will be integrated into the application layer through dedicated services.

For example:

* Resume analysis service: extracts relevant skills from uploaded resumes.

* Career matching service: calculates compatibility using our defined algorithm.

* Recommendation service: suggests learning activities based on skill gaps.

We can begin with a transparent rule-based matching algorithm and later evaluate whether an ML model adds value.

This keeps our project manageable and allows us to explain the algorithm during the final presentation.

## 5. Main modules of the proposed system

| Module              | Main functionality                           |
| ------------------- | -------------------------------------------- |
| Authentication      | Registration, login, authorization           |
| User Profile        | Personal information, interests, skills      |
| Skill Assessment    | Questions and evaluation                     |
| Career Management   | Career information and required skills       |
| Matching Engine     | Career compatibility scores                  |
| Skill-Gap Analysis  | Missing skill identification                 |
| AI Resume Analysis  | Skill extraction from resumes                |
| Learning Management | Personalized learning paths                  |
| Dashboard           | Progress and analytics                       |
| Payment             | Optional premium services                    |
| Admin               | Manage users, careers, skills, and resources |

These are planned modules; detailed requirements and feasibility will be finalized in later lessons.

## 6. Proposal-ready documentation

Proposed System

## Proposed System

The proposed AI Skill & Career Management Platform is a web-based application designed to provide an integrated solution for skill assessment, career exploration, and personalized professional development.

The system will allow users to create profiles, manage their skills and interests, complete skill assessments, and explore suitable career opportunities. A career-matching algorithm will compare users' available skill information with predefined career requirements to calculate compatibility scores and identify potential skill gaps.

Artificial Intelligence and Machine Learning techniques will be incorporated to support resume skill extraction and personalized learning recommendations. Based on identified skill gaps, the system will suggest relevant learning resources and activities to help users work toward their career goals.

An interactive dashboard will provide visual representations of career compatibility, assessment performance, skill development, and learning progress. The platform will also include administrative functionality for managing users, career information, skills, and learning resources. An online payment gateway may be integrated for selected premium services.

The application will be developed using React for the frontend, Spring Boot for backend services, and PostgreSQL for database management. The system will follow a layered architecture and use RESTful APIs for communication between the frontend and backend. Docker and suitable cloud deployment technologies will be considered for deployment.

The proposed system aims to provide a centralized and personalized environment that supports informed career exploration and structured skill development.

## 7. Example of the proposed system in action

Consider a fictional student named Alex.

Alex

Example student profile

Recorded skills

Java

SQL

HTML

CSS

Career goal: Backend Developer

Identified skill gaps

Spring Boot

REST APIs

Testing

Suggested next steps

* Learn Spring Boot fundamentals.

* Practice building REST APIs.

* Complete a small backend project.

* Track progress through the dashboard.

Illustrative example only; no actual assessment or compatibility score has been calculated.

This example demonstrates how our platform connects skill assessment, career goals, and learning recommendations.

