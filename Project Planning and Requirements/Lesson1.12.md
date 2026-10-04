# Module 1.12 — Final Requirements Review

In Progress

Final Lesson of Module 1

Excellent! Lesson 1.11 — MVP & Advanced Features is completed.

Today, we will consolidate everything we have decided for our 6th-semester project:

AI Skill & Career Management Platform

Our objective is to create a clear requirements document that you and Niraj can use during development, project proposal preparation, and supervisor discussions.

## 1. Module 1 — Complete Review

Here is our updated tracker.

| Lesson | Topic                         | Status      |
| ------ | ----------------------------- | ----------- |
| 1.1    | Project Definition & Vision   | Completed   |
| 1.2    | Problem Statement             | Completed   |
| 1.3    | Project Objectives            | Completed   |
| 1.4    | Existing System & Limitations | Completed   |
| 1.5    | Proposed System               | Completed   |
| 1.6    | Functional Requirements       | Completed   |
| 1.7    | Non-Functional Requirements   | Completed   |
| 1.8    | User Roles & Permissions      | Completed   |
| 1.9    | Use Cases & User Stories      | Completed   |
| 1.10   | Scope In/Out                  | Completed   |
| 1.11   | MVP & Advanced Features       | Completed   |
| 1.12   | Final Requirements Review     | In Progress |

Module 1 Progress

# 11/12

91.7% complete — only the final review remains.

## 2. Final Project Definition

Let's establish one consistent description of our project.

# AI Skill & Career Management Platform

![Тест Тотал для профориентации и психологической диагностики | Проф-Диалог](https://images.openai.com/static-rsc-4/uKhkI1j0t1hryyyGUtPDl2MbWZDzf7XwmzGUwfV9pIpeFaHw4RM3xKJFXRp53WfFwffZCziclRpdYibZFWJxcL3rr9XpRnegR0nszrDVOjJGzNRtYJvgdhf610xy3Bg04y2Ff4FQsPT0Un6XrwsiUgSeBs-N_57P9N7oVwhBZKk?purpose=inline)

A web-based platform for skill assessment, career exploration, and personalized development.

Technology Stack

![React Logo Vector PNG | Modern JavaScript UI Library Emblem  - freepng](https://images.openai.com/static-rsc-4/v_YRxkVgaIO4SDeoNvs8wqFWCUPPpZZsL5kVx_ktDQiKtZgMAHiSkxHMJjDkyVuTICNI24RF-lwOIJxaeydWu09nWdyQFsirfUWfJani7GSpYOfLBE-LNBdDDc_8acLBouV10tSEh5cWrc3WFWUieGkP2unLzBMX37Q6Sq2WqGs?purpose=inline)

Frontend — React

Interactive user interface

Backend — Spring Boot

REST APIs, business logic, authentication, and matching

![Docker Hub Container Image Library | App Containerization](https://images.openai.com/static-rsc-4/Pole4xk5FkyhFJxxWDBh3yHjF1pQlxteoZyEQA0ykJQSPxLpLcdTrKWhkIQ2-SeCQp9ObINiyVMBFzoUkAM9P9RUAWW761nUuSEzxGOPsF9Keb0OX7HGw8IiQD84tSEoRfxnWrmYPSxGM1Bq9IBWZrT-EGb7Ta0uoZ1t6-qsVoY?purpose=inline)

Database — PostgreSQL

Persistent application data

![Audacity icon in Windows 11 Color Style](https://images.openai.com/static-rsc-4/X_BcrYvAjkCCCWGdLEhdQSnYQEtDuflLQ_YmzmwHUlTK3u5RN3BtWIqtRRWO3Ym5Zp4tZ5gN1SfSMFMHyDXcZ32F6pnMsTLCtruBdv_eBJK-ciV1zgqKYlfW8pppbj-91fz_qv900QF6tvPygsPG1APgdaH0TbGZ5JPEK0dlmNY?purpose=inline)

AI/ML — Python or an AI service

Resume skill extraction and optional intelligent enhancements

![Yatri Cloud · 50% OFF Cloud Certification Vouchers](https://images.openai.com/static-rsc-4/Mif5Qzd0qx3Jbj-4TuWVI_O9UDwBlSBL30CyUxSUfYZGP9oKeaWHiWDAVPpobyT8lL6Wrb-lZ1pWXRD-zaUMMUg2XXOaEPzknWtoW7BVHHjTTjHFXwt7f9DNRNV8bPVbZOCAXIqXMgnyelx4CBxJ_ZSfEsqXafuxj078-zWQ5fI?purpose=inline)

Deployment — Docker

Containerization and deployment workflow

The AI/ML implementation can be selected based on feasibility. Our custom career matching algorithm remains the core matching component.

## 3. Consolidated Functional Requirements

Functional requirements describe what the system must do.

| ID    | Requirement                       | Priority    |
| ----- | --------------------------------- | ----------- |
| FR-01 | User registration and login       | Must Have   |
| FR-02 | Role-based access control         | Must Have   |
| FR-03 | Student profile management        | Must Have   |
| FR-04 | Add, update, and manage skills    | Must Have   |
| FR-05 | Skill assessment                  | Must Have   |
| FR-06 | Career profile management         | Must Have   |
| FR-07 | Career matching algorithm         | Must Have   |
| FR-08 | Skill-gap analysis                | Must Have   |
| FR-09 | Learning resource recommendations | Must Have   |
| FR-10 | Student dashboard                 | Must Have   |
| FR-11 | Admin management module           | Must Have   |
| FR-12 | AI-assisted resume analysis       | Should Have |
| FR-13 | Career compatibility score        | Should Have |
| FR-14 | Learning progress tracking        | Should Have |
| FR-15 | Premium payment gateway           | Could Have  |

## 4. Consolidated Non-Functional Requirements

These describe how well the system should operate.

| ID     | Requirement     | Expected Behavior                        |
| ------ | --------------- | ---------------------------------------- |
| NFR-01 | Security        | Protect accounts and user data           |
| NFR-02 | Performance     | Provide responsive operations            |
| NFR-03 | Usability       | Simple and understandable interface      |
| NFR-04 | Reliability     | Handle errors without unexpected failure |
| NFR-05 | Maintainability | Organized and modular code               |
| NFR-06 | Scalability     | Allow future feature expansion           |
| NFR-07 | Data Integrity  | Maintain consistent database records     |
| NFR-08 | Compatibility   | Support modern web browsers              |
| NFR-09 | Portability     | Support containerized deployment         |
| NFR-10 | Privacy         | Restrict access to personal information  |

## 5. Final Project Workflow

This is the central workflow our application should support.

Diagram options

![](data\:image/svg+xml;utf8,%3Csvg%20id%3D%22mermaid-_r_ro_%22%20width%3D%22542.7560424804688%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20class%3D%22flowchart%22%20height%3D%221087.2000732421875%22%20viewBox%3D%224%204%20542.7560424804688%201087.2000732421875%22%20role%3D%22graphics-document%20document%22%20aria-roledescription%3D%22flowchart-v2%22%3E%3Cstyle%3E%23mermaid-_r_ro_%7Bfont-family%3A%22-apple-system%22%2C%22BlinkMacSystemFont%22%2C%22Segoe%20UI%22%2C%22Roboto%22%2C%22Oxygen%22%2C%22Ubuntu%22%2C%22Cantarell%22%2C%22Helvetica%20Neue%22%2C%22Arial%22%2C%22sans-serif%22%3Bfont-size%3A14px%3Bfill%3Argb\(13%2C%2013%2C%2013\)%3B%7D%40keyframes%20edge-animation-frame%7Bfrom%7Bstroke-dashoffset%3A0%3B%7D%7D%40keyframes%20dash%7Bto%7Bstroke-dashoffset%3A0%3B%7D%7D%23mermaid-_r_ro_%20.edge-animation-slow%7Bstroke-dasharray%3A9%2C5!important%3Bstroke-dashoffset%3A900%3Banimation%3Adash%2050s%20linear%20infinite%3Bstroke-linecap%3Around%3B%7D%23mermaid-_r_ro_%20.edge-animation-fast%7Bstroke-dasharray%3A9%2C5!important%3Bstroke-dashoffset%3A900%3Banimation%3Adash%2020s%20linear%20infinite%3Bstroke-linecap%3Around%3B%7D%23mermaid-_r_ro_%20.error-icon%7Bfill%3Argb\(249%2C%20249%2C%20249\)%3B%7D%23mermaid-_r_ro_%20.error-text%7Bfill%3Argb\(13%2C%2013%2C%2013\)%3Bstroke%3Argb\(13%2C%2013%2C%2013\)%3B%7D%23mermaid-_r_ro_%20.edge-thickness-normal%7Bstroke-width%3A1px%3B%7D%23mermaid-_r_ro_%20.edge-thickness-thick%7Bstroke-width%3A3.5px%3B%7D%23mermaid-_r_ro_%20.edge-pattern-solid%7Bstroke-dasharray%3A0%3B%7D%23mermaid-_r_ro_%20.edge-thickness-invisible%7Bstroke-width%3A0%3Bfill%3Anone%3B%7D%23mermaid-_r_ro_%20.edge-pattern-dashed%7Bstroke-dasharray%3A3%3B%7D%23mermaid-_r_ro_%20.edge-pattern-dotted%7Bstroke-dasharray%3A2%3B%7D%23mermaid-_r_ro_%20.marker%7Bfill%3Argb\(93%2C%2093%2C%2093\)%3Bstroke%3Argb\(93%2C%2093%2C%2093\)%3B%7D%23mermaid-_r_ro_%20.marker.cross%7Bstroke%3Argb\(93%2C%2093%2C%2093\)%3B%7D%23mermaid-_r_ro_%20svg%7Bfont-family%3A%22-apple-system%22%2C%22BlinkMacSystemFont%22%2C%22Segoe%20UI%22%2C%22Roboto%22%2C%22Oxygen%22%2C%22Ubuntu%22%2C%22Cantarell%22%2C%22Helvetica%20Neue%22%2C%22Arial%22%2C%22sans-serif%22%3Bfont-size%3A14px%3B%7D%23mermaid-_r_ro_%20p%7Bmargin%3A0%3B%7D%23mermaid-_r_ro_%20.label%7Bfont-family%3A%22-apple-system%22%2C%22BlinkMacSystemFont%22%2C%22Segoe%20UI%22%2C%22Roboto%22%2C%22Oxygen%22%2C%22Ubuntu%22%2C%22Cantarell%22%2C%22Helvetica%20Neue%22%2C%22Arial%22%2C%22sans-serif%22%3Bcolor%3Argb\(13%2C%2013%2C%2013\)%3B%7D%23mermaid-_r_ro_%20.cluster-label%20text%7Bfill%3Argb\(13%2C%2013%2C%2013\)%3B%7D%23mermaid-_r_ro_%20.cluster-label%20span%7Bcolor%3Argb\(13%2C%2013%2C%2013\)%3B%7D%23mermaid-_r_ro_%20.cluster-label%20span%20p%7Bbackground-color%3Atransparent%3B%7D%23mermaid-_r_ro_%20.label%20text%2C%23mermaid-_r_ro_%20span%7Bfill%3Argb\(13%2C%2013%2C%2013\)%3Bcolor%3Argb\(13%2C%2013%2C%2013\)%3B%7D%23mermaid-_r_ro_%20.node%20rect%2C%23mermaid-_r_ro_%20.node%20circle%2C%23mermaid-_r_ro_%20.node%20ellipse%2C%23mermaid-_r_ro_%20.node%20polygon%2C%23mermaid-_r_ro_%20.node%20path%7Bfill%3Argb\(222%2C%20234%2C%20251\)%3Bstroke%3Argb\(83%2C%20154%2C%20248\)%3Bstroke-width%3A1px%3B%7D%23mermaid-_r_ro_%20.rough-node%20.label%20text%2C%23mermaid-_r_ro_%20.node%20.label%20text%2C%23mermaid-_r_ro_%20.image-shape%20.label%2C%23mermaid-_r_ro_%20.icon-shape%20.label%7Btext-anchor%3Amiddle%3B%7D%23mermaid-_r_ro_%20.node%20.katex%20path%7Bfill%3A%23000%3Bstroke%3A%23000%3Bstroke-width%3A1px%3B%7D%23mermaid-_r_ro_%20.rough-node%20.label%2C%23mermaid-_r_ro_%20.node%20.label%2C%23mermaid-_r_ro_%20.image-shape%20.label%2C%23mermaid-_r_ro_%20.icon-shape%20.label%7Btext-align%3Acenter%3B%7D%23mermaid-_r_ro_%20.node.clickable%7Bcursor%3Apointer%3B%7D%23mermaid-_r_ro_%20.root%20.anchor%20path%7Bfill%3Argb\(93%2C%2093%2C%2093\)!important%3Bstroke-width%3A0%3Bstroke%3Argb\(93%2C%2093%2C%2093\)%3B%7D%23mermaid-_r_ro_%20.arrowheadPath%7Bfill%3Argb\(93%2C%2093%2C%2093\)%3B%7D%23mermaid-_r_ro_%20.edgePath%20.path%7Bstroke%3Argb\(93%2C%2093%2C%2093\)%3Bstroke-width%3A2.0px%3B%7D%23mermaid-_r_ro_%20.flowchart-link%7Bstroke%3Argb\(93%2C%2093%2C%2093\)%3Bfill%3Anone%3B%7D%23mermaid-_r_ro_%20.edgeLabel%7Bbackground-color%3Argb\(252%2C%20252%2C%20252\)%3Btext-align%3Acenter%3B%7D%23mermaid-_r_ro_%20.edgeLabel%20p%7Bbackground-color%3Argb\(252%2C%20252%2C%20252\)%3B%7D%23mermaid-_r_ro_%20.edgeLabel%20rect%7Bopacity%3A0.5%3Bbackground-color%3Argb\(252%2C%20252%2C%20252\)%3Bfill%3Argb\(252%2C%20252%2C%20252\)%3B%7D%23mermaid-_r_ro_%20.labelBkg%7Bbackground-color%3Argba\(252%2C%20252%2C%20252%2C%200.5\)%3B%7D%23mermaid-_r_ro_%20.cluster%20rect%7Bfill%3Argb\(249%2C%20249%2C%20249\)%3Bstroke%3Argba\(0%2C%200%2C%200%2C%200.05\)%3Bstroke-width%3A1px%3B%7D%23mermaid-_r_ro_%20.cluster%20text%7Bfill%3Argb\(13%2C%2013%2C%2013\)%3B%7D%23mermaid-_r_ro_%20.cluster%20span%7Bcolor%3Argb\(13%2C%2013%2C%2013\)%3B%7D%23mermaid-_r_ro_%20div.mermaidTooltip%7Bposition%3Aabsolute%3Btext-align%3Acenter%3Bmax-width%3A200px%3Bpadding%3A2px%3Bfont-family%3A%22-apple-system%22%2C%22BlinkMacSystemFont%22%2C%22Segoe%20UI%22%2C%22Roboto%22%2C%22Oxygen%22%2C%22Ubuntu%22%2C%22Cantarell%22%2C%22Helvetica%20Neue%22%2C%22Arial%22%2C%22sans-serif%22%3Bfont-size%3A12px%3Bbackground%3Argb\(249%2C%20249%2C%20249\)%3Bborder%3A1px%20solid%20rgba\(0%2C%200%2C%200%2C%200.05\)%3Bborder-radius%3A2px%3Bpointer-events%3Anone%3Bz-index%3A100%3B%7D%23mermaid-_r_ro_%20.flowchartTitleText%7Btext-anchor%3Amiddle%3Bfont-size%3A18px%3Bfill%3Argb\(13%2C%2013%2C%2013\)%3B%7D%23mermaid-_r_ro_%20rect.text%7Bfill%3Anone%3Bstroke-width%3A0%3B%7D%23mermaid-_r_ro_%20.icon-shape%2C%23mermaid-_r_ro_%20.image-shape%7Bbackground-color%3Argb\(252%2C%20252%2C%20252\)%3Btext-align%3Acenter%3B%7D%23mermaid-_r_ro_%20.icon-shape%20p%2C%23mermaid-_r_ro_%20.image-shape%20p%7Bbackground-color%3Argb\(252%2C%20252%2C%20252\)%3Bpadding%3A2px%3B%7D%23mermaid-_r_ro_%20.icon-shape%20rect%2C%23mermaid-_r_ro_%20.image-shape%20rect%7Bopacity%3A0.5%3Bbackground-color%3Argb\(252%2C%20252%2C%20252\)%3Bfill%3Argb\(252%2C%20252%2C%20252\)%3B%7D%23mermaid-_r_ro_%20.label-icon%7Bdisplay%3Ainline-block%3Bheight%3A1em%3Boverflow%3Avisible%3Bvertical-align%3A-0.125em%3B%7D%23mermaid-_r_ro_%20.node%20.label-icon%20path%7Bfill%3AcurrentColor%3Bstroke%3Arevert%3Bstroke-width%3Arevert%3B%7D%23mermaid-_r_ro_%20.node%20text%7Bfont-size%3A16px%3Bfont-weight%3A600%3Bletter-spacing%3A-0.32px%3Bfill%3A%23004f99%3B%7D%23mermaid-_r_ro_%20.edgeLabels%20text%7Bfont-size%3A13px%3Bfont-weight%3A600%3Bletter-spacing%3A-0.08px%3Bfill%3A%23004f99%3B%7D%23mermaid-_r_ro_%20.node%20tspan%5Bfont-weight%3D%22normal%22%5D%2C%23mermaid-_r_ro_%20.edgeLabels%20tspan%5Bfont-weight%3D%22normal%22%5D%7Bfont-weight%3A600%3B%7D%23mermaid-_r_ro_%20.edgeLabel%20.label%20rect%7Bopacity%3A1%3Brx%3A13px%3Bry%3A13px%3Bfill%3A%23f5faff%3Bstroke%3Argb\(206%2C%20219%2C%20229\)%3Bstroke-width%3A1px%3B%7D%23mermaid-_r_ro_%20.node%20rect%2C%23mermaid-_r_ro_%20.node%20circle%2C%23mermaid-_r_ro_%20.node%20ellipse%2C%23mermaid-_r_ro_%20.node%20polygon%2C%23mermaid-_r_ro_%20.node%20path%7Bfill%3Argb\(229%2C%20243%2C%20255\)%3Bstroke%3Argba\(0%2C%200%2C%200%2C%200.1\)%3Bstroke-width%3A1px%3B%7D%23mermaid-_r_ro_%20.node%20rect%7Brx%3A16px%3Bry%3A16px%3B%7D%23mermaid-_r_ro_%20.node.mermaid-decision%20.label-container%7Bfill%3A%23f5faff%3Bstroke%3Argb\(206%2C%20219%2C%20229\)%3Bstroke-dasharray%3A2%202%3B%7D%23mermaid-_r_ro_%20.edgePaths%20.flowchart-link%7Bstroke%3Argb\(206%2C%20219%2C%20229\)%3Bstroke-width%3A1px%3Bstroke-linecap%3Around%3Bstroke-linejoin%3Around%3B%7D%23mermaid-_r_ro_%20.marker%7Bfill%3Argb\(206%2C%20219%2C%20229\)%3Bstroke%3Argb\(206%2C%20219%2C%20229\)%3B%7D%23mermaid-_r_ro_%20.node%7Bcolor-scheme%3Alight%3B%7D%23mermaid-_r_ro_%20%3Aroot%7B--mermaid-font-family%3A%22-apple-system%22%2C%22BlinkMacSystemFont%22%2C%22Segoe%20UI%22%2C%22Roboto%22%2C%22Oxygen%22%2C%22Ubuntu%22%2C%22Cantarell%22%2C%22Helvetica%20Neue%22%2C%22Arial%22%2C%22sans-serif%22%3B%7D%3C%2Fstyle%3E%3Cg%3E%3Cmarker%20id%3D%22mermaid-_r_ro__flowchart-v2-pointEnd%22%20class%3D%22marker%20flowchart-v2%22%20viewBox%3D%22-5%20-5%2010%2010%22%20refX%3D%220%22%20refY%3D%220%22%20markerUnits%3D%22userSpaceOnUse%22%20markerWidth%3D%2210%22%20markerHeight%3D%2210%22%20orient%3D%22auto%22%3E%3Cpath%20d%3D%22M%200%200%20L%204%200%20M%200.8180194846605362%20-3.181980515339464%20L%204%200%20L%200.8180194846605362%203.181980515339464%22%20class%3D%22arrowMarkerPath%22%20style%3D%22stroke-width%3A%201%3B%20stroke-dasharray%3A%20none%3B%20fill%3A%20none%3B%20stroke-linecap%3A%20round%3B%20stroke-linejoin%3A%20round%3B%22%3E%3C%2Fpath%3E%3C%2Fmarker%3E%3Cmarker%20id%3D%22mermaid-_r_ro__flowchart-v2-pointStart%22%20class%3D%22marker%20flowchart-v2%22%20viewBox%3D%22-5%20-5%2010%2010%22%20refX%3D%220%22%20refY%3D%220%22%20markerUnits%3D%22userSpaceOnUse%22%20markerWidth%3D%2210%22%20markerHeight%3D%2210%22%20orient%3D%22auto%22%3E%3Cpath%20d%3D%22M%200%200%20L%20-4%200%20M%20-0.8180194846605362%20-3.181980515339464%20L%20-4%200%20L%20-0.8180194846605362%203.181980515339464%22%20class%3D%22arrowMarkerPath%22%20style%3D%22stroke-width%3A%201%3B%20stroke-dasharray%3A%20none%3B%20fill%3A%20none%3B%20stroke-linecap%3A%20round%3B%20stroke-linejoin%3A%20round%3B%22%3E%3C%2Fpath%3E%3C%2Fmarker%3E%3Cmarker%20id%3D%22mermaid-_r_ro__flowchart-v2-circleEnd%22%20class%3D%22marker%20flowchart-v2%22%20viewBox%3D%220%200%2010%2010%22%20refX%3D%2211%22%20refY%3D%225%22%20markerUnits%3D%22userSpaceOnUse%22%20markerWidth%3D%2211%22%20markerHeight%3D%2211%22%20orient%3D%22auto%22%3E%3Ccircle%20cx%3D%225%22%20cy%3D%225%22%20r%3D%225%22%20class%3D%22arrowMarkerPath%22%20style%3D%22stroke-width%3A%201%3B%20stroke-dasharray%3A%201%2C%200%3B%22%3E%3C%2Fcircle%3E%3C%2Fmarker%3E%3Cmarker%20id%3D%22mermaid-_r_ro__flowchart-v2-circleStart%22%20class%3D%22marker%20flowchart-v2%22%20viewBox%3D%220%200%2010%2010%22%20refX%3D%22-1%22%20refY%3D%225%22%20markerUnits%3D%22userSpaceOnUse%22%20markerWidth%3D%2211%22%20markerHeight%3D%2211%22%20orient%3D%22auto%22%3E%3Ccircle%20cx%3D%225%22%20cy%3D%225%22%20r%3D%225%22%20class%3D%22arrowMarkerPath%22%20style%3D%22stroke-width%3A%201%3B%20stroke-dasharray%3A%201%2C%200%3B%22%3E%3C%2Fcircle%3E%3C%2Fmarker%3E%3Cmarker%20id%3D%22mermaid-_r_ro__flowchart-v2-crossEnd%22%20class%3D%22marker%20cross%20flowchart-v2%22%20viewBox%3D%220%200%2011%2011%22%20refX%3D%2212%22%20refY%3D%225.2%22%20markerUnits%3D%22userSpaceOnUse%22%20markerWidth%3D%2211%22%20markerHeight%3D%2211%22%20orient%3D%22auto%22%3E%3Cpath%20d%3D%22M%201%2C1%20l%209%2C9%20M%2010%2C1%20l%20-9%2C9%22%20class%3D%22arrowMarkerPath%22%20style%3D%22stroke-width%3A%202%3B%20stroke-dasharray%3A%201%2C%200%3B%22%3E%3C%2Fpath%3E%3C%2Fmarker%3E%3Cmarker%20id%3D%22mermaid-_r_ro__flowchart-v2-crossStart%22%20class%3D%22marker%20cross%20flowchart-v2%22%20viewBox%3D%220%200%2011%2011%22%20refX%3D%22-1%22%20refY%3D%225.2%22%20markerUnits%3D%22userSpaceOnUse%22%20markerWidth%3D%2211%22%20markerHeight%3D%2211%22%20orient%3D%22auto%22%3E%3Cpath%20d%3D%22M%201%2C1%20l%209%2C9%20M%2010%2C1%20l%20-9%2C9%22%20class%3D%22arrowMarkerPath%22%20style%3D%22stroke-width%3A%202%3B%20stroke-dasharray%3A%201%2C%200%3B%22%3E%3C%2Fpath%3E%3C%2Fmarker%3E%3C%2Fg%3E%3Cg%20class%3D%22subgraphs%22%3E%3C%2Fg%3E%3Cg%20class%3D%22nodes%22%3E%3Cg%20class%3D%22node%20default%22%20id%3D%22flowchart-A-0%22%20transform%3D%22translate\(158.78627014160156%2C%2042\)%22%3E%3Crect%20class%3D%22basic%20label-container%22%20style%3D%22%22%20x%3D%22-133.85000610351562%22%20y%3D%22-30%22%20width%3D%22267.70001220703125%22%20height%3D%2260%22%3E%3C%2Frect%3E%3Cg%20class%3D%22label%22%20style%3D%22%22%20transform%3D%22translate\(0%2C%20-10.800000190734863\)%22%3E%3Crect%3E%3C%2Frect%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3Ctext%20y%3D%22-10.1%22%20style%3D%22%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3EStudent%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Registration%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20%2F%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Login%3C%2Ftspan%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22node%20default%22%20id%3D%22flowchart-B-1%22%20transform%3D%22translate\(158.78627014160156%2C%20142\)%22%3E%3Crect%20class%3D%22basic%20label-container%22%20style%3D%22%22%20x%3D%22-123.67142486572266%22%20y%3D%22-30%22%20width%3D%22247.3428497314453%22%20height%3D%2260%22%3E%3C%2Frect%3E%3Cg%20class%3D%22label%22%20style%3D%22%22%20transform%3D%22translate\(0%2C%20-10.800000190734863\)%22%3E%3Crect%3E%3C%2Frect%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3Ctext%20y%3D%22-10.1%22%20style%3D%22%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3EComplete%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Student%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Profile%3C%2Ftspan%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22node%20default%22%20id%3D%22flowchart-C-3%22%20transform%3D%22translate\(141.0961151123047%2C%20342\)%22%3E%3Crect%20class%3D%22basic%20label-container%22%20style%3D%22%22%20x%3D%22-70.60095596313477%22%20y%3D%22-30%22%20width%3D%22141.20191192626953%22%20height%3D%2260%22%3E%3C%2Frect%3E%3Cg%20class%3D%22label%22%20style%3D%22%22%20transform%3D%22translate\(0%2C%20-10.800000190734863\)%22%3E%3Crect%3E%3C%2Frect%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3Ctext%20y%3D%22-10.1%22%20style%3D%22%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3EAdd%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Skills%3C%2Ftspan%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22node%20default%22%20id%3D%22flowchart-D-5%22%20transform%3D%22translate\(141.0961151123047%2C%20447.5999984741211\)%22%3E%3Crect%20class%3D%22basic%20label-container%22%20style%3D%22%22%20x%3D%22-129.09612274169922%22%20y%3D%22-30%22%20width%3D%22258.19224548339844%22%20height%3D%2260%22%3E%3C%2Frect%3E%3Cg%20class%3D%22label%22%20style%3D%22%22%20transform%3D%22translate\(0%2C%20-10.800000190734863\)%22%3E%3Crect%3E%3C%2Frect%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3Ctext%20y%3D%22-10.1%22%20style%3D%22%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3EComplete%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Skill%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Assessment%3C%2Ftspan%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22node%20default%22%20id%3D%22flowchart-E-7%22%20transform%3D%22translate\(184.773198445638%2C%20553.1999969482422\)%22%3E%3Crect%20class%3D%22basic%20label-container%22%20style%3D%22%22%20x%3D%22-131.03125%22%20y%3D%22-30%22%20width%3D%22262.0625%22%20height%3D%2260%22%3E%3C%2Frect%3E%3Cg%20class%3D%22label%22%20style%3D%22%22%20transform%3D%22translate\(0%2C%20-10.800000190734863\)%22%3E%3Crect%3E%3C%2Frect%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3Ctext%20y%3D%22-10.1%22%20style%3D%22%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3ECareer%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Matching%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Algorithm%3C%2Ftspan%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22node%20default%22%20id%3D%22flowchart-F-9%22%20transform%3D%22translate\(184.773198445638%2C%20653.1999969482422\)%22%3E%3Crect%20class%3D%22basic%20label-container%22%20style%3D%22%22%20x%3D%22-134.05892181396484%22%20y%3D%22-30%22%20width%3D%22268.1178436279297%22%20height%3D%2260%22%3E%3C%2Frect%3E%3Cg%20class%3D%22label%22%20style%3D%22%22%20transform%3D%22translate\(0%2C%20-10.800000190734863\)%22%3E%3Crect%3E%3C%2Frect%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3Ctext%20y%3D%22-10.1%22%20style%3D%22%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3ECareer%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Compatibility%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Results%3C%2Ftspan%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22node%20default%22%20id%3D%22flowchart-G-11%22%20transform%3D%22translate\(184.773198445638%2C%20753.1999969482422\)%22%3E%3Crect%20class%3D%22basic%20label-container%22%20style%3D%22%22%20x%3D%22-96.5918960571289%22%20y%3D%22-30%22%20width%3D%22193.1837921142578%22%20height%3D%2260%22%3E%3C%2Frect%3E%3Cg%20class%3D%22label%22%20style%3D%22%22%20transform%3D%22translate\(0%2C%20-10.800000190734863\)%22%3E%3Crect%3E%3C%2Frect%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3Ctext%20y%3D%22-10.1%22%20style%3D%22%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3ESkill%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Gap%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Analysis%3C%2Ftspan%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22node%20default%22%20id%3D%22flowchart-H-13%22%20transform%3D%22translate\(184.773198445638%2C%20853.1999969482422\)%22%3E%3Crect%20class%3D%22basic%20label-container%22%20style%3D%22%22%20x%3D%22-133.73831939697266%22%20y%3D%22-30%22%20width%3D%22267.4766387939453%22%20height%3D%2260%22%3E%3C%2Frect%3E%3Cg%20class%3D%22label%22%20style%3D%22%22%20transform%3D%22translate\(0%2C%20-10.800000190734863\)%22%3E%3Crect%3E%3C%2Frect%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3Ctext%20y%3D%22-10.1%22%20style%3D%22%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3ELearning%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Recommendations%3C%2Ftspan%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22node%20default%22%20id%3D%22flowchart-I-15%22%20transform%3D%22translate\(184.773198445638%2C%20953.1999969482422\)%22%3E%3Crect%20class%3D%22basic%20label-container%22%20style%3D%22%22%20x%3D%22-118.64189910888672%22%20y%3D%22-30%22%20width%3D%22237.28379821777344%22%20height%3D%2260%22%3E%3C%2Frect%3E%3Cg%20class%3D%22label%22%20style%3D%22%22%20transform%3D%22translate\(0%2C%20-10.800000190734863\)%22%3E%3Crect%3E%3C%2Frect%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3Ctext%20y%3D%22-10.1%22%20style%3D%22%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3ETrack%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Learning%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Progress%3C%2Ftspan%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22node%20default%22%20id%3D%22flowchart-J-17%22%20transform%3D%22translate\(184.773198445638%2C%201053.1999969482422\)%22%3E%3Crect%20class%3D%22basic%20label-container%22%20style%3D%22%22%20x%3D%22-127.65065002441406%22%20y%3D%22-30%22%20width%3D%22255.30130004882812%22%20height%3D%2260%22%3E%3C%2Frect%3E%3Cg%20class%3D%22label%22%20style%3D%22%22%20transform%3D%22translate\(0%2C%20-10.800000190734863\)%22%3E%3Crect%3E%3C%2Frect%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3Ctext%20y%3D%22-10.1%22%20style%3D%22%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3EUpdated%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Career%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Readiness%3C%2Ftspan%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22node%20default%22%20id%3D%22flowchart-K-19%22%20transform%3D%22translate\(274.25435638427734%2C%20242\)%22%3E%3Crect%20class%3D%22basic%20label-container%22%20style%3D%22%22%20x%3D%22-135.69189453125%22%20y%3D%22-30%22%20width%3D%22271.3837890625%22%20height%3D%2260%22%3E%3C%2Frect%3E%3Cg%20class%3D%22label%22%20style%3D%22%22%20transform%3D%22translate\(0%2C%20-10.800000190734863\)%22%3E%3Crect%3E%3C%2Frect%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3Ctext%20y%3D%22-10.1%22%20style%3D%22%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3EOptional%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20AI%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Resume%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Analysis%3C%2Ftspan%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22node%20default%22%20id%3D%22flowchart-L-22%22%20transform%3D%22translate\(424.47412872314453%2C%20342\)%22%3E%3Crect%20class%3D%22basic%20label-container%22%20style%3D%22%22%20x%3D%22-59.63750076293945%22%20y%3D%22-30%22%20width%3D%22119.2750015258789%22%20height%3D%2260%22%3E%3C%2Frect%3E%3Cg%20class%3D%22label%22%20style%3D%22%22%20transform%3D%22translate\(0%2C%20-10.800000190734863\)%22%3E%3Crect%3E%3C%2Frect%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3Ctext%20y%3D%22-10.1%22%20style%3D%22%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3EAdmin%3C%2Ftspan%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22node%20default%22%20id%3D%22flowchart-M-23%22%20transform%3D%22translate\(424.47412872314453%2C%20447.5999984741211\)%22%3E%3Crect%20class%3D%22basic%20label-container%22%20style%3D%22%22%20x%3D%22-114.28189849853516%22%20y%3D%22-35.599998474121094%22%20width%3D%22228.5637969970703%22%20height%3D%2271.19999694824219%22%3E%3C%2Frect%3E%3Cg%20class%3D%22label%22%20style%3D%22%22%20transform%3D%22translate\(0%2C%20-19.599998474121094\)%22%3E%3Crect%3E%3C%2Frect%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3Ctext%20y%3D%22-10.1%22%20style%3D%22%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3EManage%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Users%2C%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Skills%2C%3C%2Ftspan%3E%3C%2Ftspan%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%221em%22%20dy%3D%221.1em%22%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3ECareers%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20and%3C%2Ftspan%3E%3Ctspan%20font-style%3D%22normal%22%20class%3D%22text-inner-tspan%22%20font-weight%3D%22normal%22%3E%20Resources%3C%2Ftspan%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22edges%20edgePaths%22%3E%3Cpath%20d%3D%22M158.78627014160156%2C72L158.78627014160156%2C100%22%20id%3D%22L_A_B_0%22%20class%3D%22edge-thickness-normal%20edge-pattern-solid%20edge-thickness-normal%20edge-pattern-solid%20flowchart-link%22%20style%3D%22%3B%22%20data-edge%3D%22true%22%20data-et%3D%22edge%22%20data-id%3D%22L_A_B_0%22%20data-points%3D%22W3sieCI6MTU4Ljc4NjI3MDE0MTYwMTU2LCJ5Ijo3Mn0seyJ4IjoxNTguNzg2MjcwMTQxNjAxNTYsInkiOjEwNH1d%22%20marker-end%3D%22url\(%23mermaid-_r_ro__flowchart-v2-pointEnd\)%22%3E%3C%2Fpath%3E%3Cpath%20d%3D%22M117.56246185302732%2C172L117.56246185302734%2C242L117.56246185302734%2C300%22%20id%3D%22L_B_C_0%22%20class%3D%22edge-thickness-normal%20edge-pattern-solid%20edge-thickness-normal%20edge-pattern-solid%20flowchart-link%22%20style%3D%22%3B%22%20data-edge%3D%22true%22%20data-et%3D%22edge%22%20data-id%3D%22L_B_C_0%22%20data-points%3D%22W3sieCI6MTE3LjU2MjQ2MTg1MzAyNzMyLCJ5IjoxNzJ9LHsieCI6MTE3LjU2MjQ2MTg1MzAyNzM0LCJ5IjoyNDJ9LHsieCI6MTE3LjU2MjQ2MTg1MzAyNzM0LCJ5IjozMDR9XQ%3D%3D%22%20marker-end%3D%22url\(%23mermaid-_r_ro__flowchart-v2-pointEnd\)%22%3E%3C%2Fpath%3E%3Cpath%20d%3D%22M141.0961151123047%2C372L141.0961151123047%2C405.5999984741211%22%20id%3D%22L_C_D_0%22%20class%3D%22edge-thickness-normal%20edge-pattern-solid%20edge-thickness-normal%20edge-pattern-solid%20flowchart-link%22%20style%3D%22%3B%22%20data-edge%3D%22true%22%20data-et%3D%22edge%22%20data-id%3D%22L_C_D_0%22%20data-points%3D%22W3sieCI6MTQxLjA5NjExNTExMjMwNDcsInkiOjM3Mn0seyJ4IjoxNDEuMDk2MTE1MTEyMzA0NywieSI6NDA5LjU5OTk5ODQ3NDEyMTF9XQ%3D%3D%22%20marker-end%3D%22url\(%23mermaid-_r_ro__flowchart-v2-pointEnd\)%22%3E%3C%2Fpath%3E%3Cpath%20d%3D%22M141.0961151123047%2C477.5999984741211L141.0961151123047%2C511.1999969482422%22%20id%3D%22L_D_E_0%22%20class%3D%22edge-thickness-normal%20edge-pattern-solid%20edge-thickness-normal%20edge-pattern-solid%20flowchart-link%22%20style%3D%22%3B%22%20data-edge%3D%22true%22%20data-et%3D%22edge%22%20data-id%3D%22L_D_E_0%22%20data-points%3D%22W3sieCI6MTQxLjA5NjExNTExMjMwNDcsInkiOjQ3Ny41OTk5OTg0NzQxMjExfSx7IngiOjE0MS4wOTYxMTUxMTIzMDQ3LCJ5Ijo1MTUuMTk5OTk2OTQ4MjQyMn1d%22%20marker-end%3D%22url\(%23mermaid-_r_ro__flowchart-v2-pointEnd\)%22%3E%3C%2Fpath%3E%3Cpath%20d%3D%22M184.773198445638%2C583.1999969482422L184.773198445638%2C611.1999969482422%22%20id%3D%22L_E_F_0%22%20class%3D%22edge-thickness-normal%20edge-pattern-solid%20edge-thickness-normal%20edge-pattern-solid%20flowchart-link%22%20style%3D%22%3B%22%20data-edge%3D%22true%22%20data-et%3D%22edge%22%20data-id%3D%22L_E_F_0%22%20data-points%3D%22W3sieCI6MTg0Ljc3MzE5ODQ0NTYzOCwieSI6NTgzLjE5OTk5Njk0ODI0MjJ9LHsieCI6MTg0Ljc3MzE5ODQ0NTYzOCwieSI6NjE1LjE5OTk5Njk0ODI0MjJ9XQ%3D%3D%22%20marker-end%3D%22url\(%23mermaid-_r_ro__flowchart-v2-pointEnd\)%22%3E%3C%2Fpath%3E%3Cpath%20d%3D%22M184.773198445638%2C683.1999969482422L184.773198445638%2C711.1999969482422%22%20id%3D%22L_F_G_0%22%20class%3D%22edge-thickness-normal%20edge-pattern-solid%20edge-thickness-normal%20edge-pattern-solid%20flowchart-link%22%20style%3D%22%3B%22%20data-edge%3D%22true%22%20data-et%3D%22edge%22%20data-id%3D%22L_F_G_0%22%20data-points%3D%22W3sieCI6MTg0Ljc3MzE5ODQ0NTYzOCwieSI6NjgzLjE5OTk5Njk0ODI0MjJ9LHsieCI6MTg0Ljc3MzE5ODQ0NTYzOCwieSI6NzE1LjE5OTk5Njk0ODI0MjJ9XQ%3D%3D%22%20marker-end%3D%22url\(%23mermaid-_r_ro__flowchart-v2-pointEnd\)%22%3E%3C%2Fpath%3E%3Cpath%20d%3D%22M184.773198445638%2C783.1999969482422L184.773198445638%2C811.1999969482422%22%20id%3D%22L_G_H_0%22%20class%3D%22edge-thickness-normal%20edge-pattern-solid%20edge-thickness-normal%20edge-pattern-solid%20flowchart-link%22%20style%3D%22%3B%22%20data-edge%3D%22true%22%20data-et%3D%22edge%22%20data-id%3D%22L_G_H_0%22%20data-points%3D%22W3sieCI6MTg0Ljc3MzE5ODQ0NTYzOCwieSI6NzgzLjE5OTk5Njk0ODI0MjJ9LHsieCI6MTg0Ljc3MzE5ODQ0NTYzOCwieSI6ODE1LjE5OTk5Njk0ODI0MjJ9XQ%3D%3D%22%20marker-end%3D%22url\(%23mermaid-_r_ro__flowchart-v2-pointEnd\)%22%3E%3C%2Fpath%3E%3Cpath%20d%3D%22M184.773198445638%2C883.1999969482422L184.773198445638%2C911.1999969482422%22%20id%3D%22L_H_I_0%22%20class%3D%22edge-thickness-normal%20edge-pattern-solid%20edge-thickness-normal%20edge-pattern-solid%20flowchart-link%22%20style%3D%22%3B%22%20data-edge%3D%22true%22%20data-et%3D%22edge%22%20data-id%3D%22L_H_I_0%22%20data-points%3D%22W3sieCI6MTg0Ljc3MzE5ODQ0NTYzOCwieSI6ODgzLjE5OTk5Njk0ODI0MjJ9LHsieCI6MTg0Ljc3MzE5ODQ0NTYzOCwieSI6OTE1LjE5OTk5Njk0ODI0MjJ9XQ%3D%3D%22%20marker-end%3D%22url\(%23mermaid-_r_ro__flowchart-v2-pointEnd\)%22%3E%3C%2Fpath%3E%3Cpath%20d%3D%22M184.773198445638%2C983.1999969482422L184.773198445638%2C1011.1999969482422%22%20id%3D%22L_I_J_0%22%20class%3D%22edge-thickness-normal%20edge-pattern-solid%20edge-thickness-normal%20edge-pattern-solid%20flowchart-link%22%20style%3D%22%3B%22%20data-edge%3D%22true%22%20data-et%3D%22edge%22%20data-id%3D%22L_I_J_0%22%20data-points%3D%22W3sieCI6MTg0Ljc3MzE5ODQ0NTYzOCwieSI6OTgzLjE5OTk5Njk0ODI0MjJ9LHsieCI6MTg0Ljc3MzE5ODQ0NTYzOCwieSI6MTAxNS4xOTk5OTY5NDgyNDIyfV0%3D%22%20marker-end%3D%22url\(%23mermaid-_r_ro__flowchart-v2-pointEnd\)%22%3E%3C%2Fpath%3E%3Cpath%20d%3D%22M200.01007843017578%2C172L200.01007843017578%2C185.21704397470535Q200.01007843017578%2C187%20201.09586486780267%2C188.4142135623731L201.09586486780267%2C188.4142135623731Q202.1816513054296%2C189.82842712474618%20203.59586486780267%2C190.9142135623731L203.59586486780267%2C190.9142135623731Q205.01007843017578%2C192%20206.79303445547043%2C192L267.4714003589827%2C192Q269.25435638427734%2C192%20270.66856994665045%2C193.0857864376269L270.66856994665045%2C193.08578643762692Q272.08278350902356%2C194.17157287525382%20273.16856994665045%2C195.5857864376269L273.16856994665045%2C195.5857864376269Q274.25435638427734%2C197%20274.25435638427734%2C198.78295602529465L274.25435638427734%2C202%22%20id%3D%22L_B_K_0%22%20class%3D%22edge-thickness-normal%20edge-pattern-dotted%20edge-thickness-normal%20edge-pattern-solid%20flowchart-link%22%20style%3D%22%3B%22%20data-edge%3D%22true%22%20data-et%3D%22edge%22%20data-id%3D%22L_B_K_0%22%20data-points%3D%22W3sieCI6MjAwLjAxMDA3ODQzMDE3NTc4LCJ5IjoxNzJ9LHsieCI6MjAwLjAxMDA3ODQzMDE3NTc4LCJ5IjoxOTJ9LHsieCI6Mjc0LjI1NDM1NjM4NDI3NzM0LCJ5IjoxOTJ9LHsieCI6Mjc0LjI1NDM1NjM4NDI3NzM0LCJ5IjoyMDZ9XQ%3D%3D%22%20marker-end%3D%22url\(%23mermaid-_r_ro__flowchart-v2-pointEnd\)%22%3E%3C%2Fpath%3E%3Cpath%20d%3D%22M274.25435638427734%2C272L274.25435638427734%2C285.21704397470535Q274.25435638427734%2C287%20273.16856994665045%2C288.4142135623731L273.16856994665045%2C288.4142135623731Q272.08278350902356%2C289.8284271247462%20270.66856994665045%2C290.9142135623731L270.66856994665045%2C290.9142135623731Q269.25435638427734%2C292%20267.4714003589827%2C292L171.41272439687668%2C292Q169.62976837158203%2C292%20168.21555480920892%2C293.0857864376269L168.21555480920892%2C293.0857864376269Q166.80134124683585%2C294.1715728752538%20165.71555480920895%2C295.5857864376269L165.71555480920892%2C295.5857864376269Q164.62976837158203%2C297%20164.62976837158203%2C298.78295602529465L164.62976837158203%2C302%22%20id%3D%22L_K_C_0%22%20class%3D%22edge-thickness-normal%20edge-pattern-dotted%20edge-thickness-normal%20edge-pattern-solid%20flowchart-link%22%20style%3D%22%3B%22%20data-edge%3D%22true%22%20data-et%3D%22edge%22%20data-id%3D%22L_K_C_0%22%20data-points%3D%22W3sieCI6Mjc0LjI1NDM1NjM4NDI3NzM0LCJ5IjoyNzJ9LHsieCI6Mjc0LjI1NDM1NjM4NDI3NzM0LCJ5IjoyOTJ9LHsieCI6MTY0LjYyOTc2ODM3MTU4MjAzLCJ5IjoyOTJ9LHsieCI6MTY0LjYyOTc2ODM3MTU4MjAzLCJ5IjozMDZ9XQ%3D%3D%22%20marker-end%3D%22url\(%23mermaid-_r_ro__flowchart-v2-pointEnd\)%22%3E%3C%2Fpath%3E%3Cpath%20d%3D%22M424.47412872314453%2C372L424.47412872314453%2C400%22%20id%3D%22L_L_M_0%22%20class%3D%22edge-thickness-normal%20edge-pattern-solid%20edge-thickness-normal%20edge-pattern-solid%20flowchart-link%22%20style%3D%22%3B%22%20data-edge%3D%22true%22%20data-et%3D%22edge%22%20data-id%3D%22L_L_M_0%22%20data-points%3D%22W3sieCI6NDI0LjQ3NDEyODcyMzE0NDUzLCJ5IjozNzJ9LHsieCI6NDI0LjQ3NDEyODcyMzE0NDUzLCJ5Ijo0MDR9XQ%3D%3D%22%20marker-end%3D%22url\(%23mermaid-_r_ro__flowchart-v2-pointEnd\)%22%3E%3C%2Fpath%3E%3Cpath%20d%3D%22M424.47412872314453%2C483.1999969482422L424.47412872314453%2C496.41704092294754Q424.47412872314453%2C498.1999969482422%20423.38834228551764%2C499.6142105106153L423.38834228551764%2C499.6142105106153Q422.30255584789074%2C501.0284240729884%20420.88834228551764%2C502.1142105106153L420.88834228551764%2C502.1142105106153Q419.47412872314453%2C503.1999969482422%20417.6911726978499%2C503.1999969482422L235.23323780426603%2C503.1999969482422Q233.45028177897137%2C503.1999969482422%20232.03606821659827%2C504.2857833858691L232.03606821659827%2C504.2857833858691Q230.6218546542252%2C505.371569823496%20229.5360682165983%2C506.7857833858691L229.53606821659827%2C506.7857833858691Q228.45028177897137%2C508.1999969482422%20228.45028177897137%2C509.98295297353684L228.45028177897137%2C513.1999969482422%22%20id%3D%22L_M_E_0%22%20class%3D%22edge-thickness-normal%20edge-pattern-solid%20edge-thickness-normal%20edge-pattern-solid%20flowchart-link%22%20style%3D%22%3B%22%20data-edge%3D%22true%22%20data-et%3D%22edge%22%20data-id%3D%22L_M_E_0%22%20data-points%3D%22W3sieCI6NDI0LjQ3NDEyODcyMzE0NDUzLCJ5Ijo0ODMuMTk5OTk2OTQ4MjQyMn0seyJ4Ijo0MjQuNDc0MTI4NzIzMTQ0NTMsInkiOjUwMy4xOTk5OTY5NDgyNDIyfSx7IngiOjIyOC40NTAyODE3Nzg5NzEzNywieSI6NTAzLjE5OTk5Njk0ODI0MjJ9LHsieCI6MjI4LjQ1MDI4MTc3ODk3MTM3LCJ5Ijo1MTcuMTk5OTk2OTQ4MjQyMn1d%22%20marker-end%3D%22url\(%23mermaid-_r_ro__flowchart-v2-pointEnd\)%22%3E%3C%2Fpath%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabels%22%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3C%2Fg%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3C%2Fg%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3C%2Fg%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3C%2Fg%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3C%2Fg%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3C%2Fg%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3C%2Fg%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3C%2Fg%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3C%2Fg%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3C%2Fg%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3C%2Fg%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3C%2Fg%3E%3Cg%3E%3Crect%20class%3D%22background%22%20style%3D%22stroke%3A%20none%22%3E%3C%2Frect%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabel%22%3E%3Cg%20class%3D%22label%22%20data-id%3D%22L_A_B_0%22%20transform%3D%22translate\(0%2C%200\)%22%3E%3Ctext%20y%3D%22-10.1%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabel%22%3E%3Cg%20class%3D%22label%22%20data-id%3D%22L_B_C_0%22%20transform%3D%22translate\(0%2C%200\)%22%3E%3Ctext%20y%3D%22-10.1%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabel%22%3E%3Cg%20class%3D%22label%22%20data-id%3D%22L_C_D_0%22%20transform%3D%22translate\(0%2C%200\)%22%3E%3Ctext%20y%3D%22-10.1%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabel%22%3E%3Cg%20class%3D%22label%22%20data-id%3D%22L_D_E_0%22%20transform%3D%22translate\(0%2C%200\)%22%3E%3Ctext%20y%3D%22-10.1%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabel%22%3E%3Cg%20class%3D%22label%22%20data-id%3D%22L_E_F_0%22%20transform%3D%22translate\(0%2C%200\)%22%3E%3Ctext%20y%3D%22-10.1%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabel%22%3E%3Cg%20class%3D%22label%22%20data-id%3D%22L_F_G_0%22%20transform%3D%22translate\(0%2C%200\)%22%3E%3Ctext%20y%3D%22-10.1%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabel%22%3E%3Cg%20class%3D%22label%22%20data-id%3D%22L_G_H_0%22%20transform%3D%22translate\(0%2C%200\)%22%3E%3Ctext%20y%3D%22-10.1%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabel%22%3E%3Cg%20class%3D%22label%22%20data-id%3D%22L_H_I_0%22%20transform%3D%22translate\(0%2C%200\)%22%3E%3Ctext%20y%3D%22-10.1%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabel%22%3E%3Cg%20class%3D%22label%22%20data-id%3D%22L_I_J_0%22%20transform%3D%22translate\(0%2C%200\)%22%3E%3Ctext%20y%3D%22-10.1%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabel%22%3E%3Cg%20class%3D%22label%22%20data-id%3D%22L_B_K_0%22%20transform%3D%22translate\(0%2C%200\)%22%3E%3Ctext%20y%3D%22-10.1%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabel%22%3E%3Cg%20class%3D%22label%22%20data-id%3D%22L_K_C_0%22%20transform%3D%22translate\(0%2C%200\)%22%3E%3Ctext%20y%3D%22-10.1%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabel%22%3E%3Cg%20class%3D%22label%22%20data-id%3D%22L_L_M_0%22%20transform%3D%22translate\(0%2C%200\)%22%3E%3Ctext%20y%3D%22-10.1%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3Cg%20class%3D%22edgeLabel%22%3E%3Cg%20class%3D%22label%22%20data-id%3D%22L_M_E_0%22%20transform%3D%22translate\(0%2C%200\)%22%3E%3Ctext%20y%3D%22-10.1%22%3E%3Ctspan%20class%3D%22text-outer-tspan%22%20x%3D%220%22%20y%3D%22-0.1em%22%20dy%3D%221.1em%22%3E%3C%2Ftspan%3E%3C%2Ftext%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fsvg%3E)

### Example scenario

A student interested in becoming a Java Backend Developer:

* Adds Java, SQL, and Spring Boot to their profile.

* Completes a skill assessment.

* Receives career compatibility results.

* Sees missing skills such as REST API development or testing, depending on the career requirements and assessment.

* Receives learning resources.

* Tracks progress as they develop those skills.

This is the primary problem our platform aims to solve.

## 6. Proposal-Ready Consolidated Requirements Document

The following is a consolidated draft for your project proposal. Review it with Niraj and your supervisor before treating it as the final approved specification.

AI Skill & Career Management Platform

# AI Skill & Career Management Platform

## Project Requirements Specification

### 1. Project Overview

The AI Skill & Career Management Platform is a web-based application designed to assist students and job seekers in identifying their skills, exploring suitable career opportunities, understanding skill gaps, and planning their professional development.

The system will integrate skill assessment, career matching, AI-assisted resume analysis, personalized learning recommendations, and progress tracking into a unified platform.

The application will use React for frontend development, Spring Boot for backend services, and PostgreSQL for database management. Artificial Intelligence and Machine Learning techniques will be applied where feasible to support resume skill extraction and intelligent career-related functionalities.

### 2. Problem Statement

Students and job seekers often face difficulties identifying suitable career paths, understanding industry skill requirements, evaluating their current abilities, and finding relevant learning resources.

Existing tools may address individual aspects of career development, but users can still face difficulties managing these activities as a connected process.

Therefore, an integrated platform is proposed to support career exploration, skill assessment, career compatibility analysis, skill-gap identification, and learning recommendations.

### 3. General Objective

To design and develop an AI-assisted web platform that helps students and job seekers evaluate their skills, explore suitable career paths, identify skill gaps, and plan their career development.

### 4. Specific Objectives

* To develop secure user registration and authentication.

* To provide student profile and skill management.

* To implement skill assessment functionality.

* To maintain career profiles and their required skills.

* To develop a custom career-matching algorithm.

* To identify skill gaps between user capabilities and career requirements.

* To recommend relevant learning resources.

* To integrate AI-assisted resume skill extraction, subject to feasibility.

* To provide dashboards for career insights and progress tracking.

* To develop administrative functionalities for managing platform data.

* To deploy and evaluate the application using suitable tools and infrastructure.

### 5. User Roles

**Student / Job Seeker:** Manages personal information, skills, assessments, career interests, recommendations, and learning progress.

**Administrator:** Manages users, career profiles, skills, assessment questions, and learning resources.

### 6. Functional Requirements

The system shall provide:

1. User registration and login.

2. Role-based authorization.

3. Student profile management.

4. Skill management.

5. Skill assessment.

6. Career profile management.

7. Career matching and compatibility results.

8. Skill-gap analysis.

9. Learning resource recommendations.

10. Student dashboard.

11. Administrative management.

12. AI-assisted resume analysis as a prioritized enhancement.

13. Learning progress tracking.

14. Optional premium payment functionality, subject to feasibility.

### 7. Non-Functional Requirements

The system shall prioritize:

* Security and privacy of user data.

* Usability and accessibility.

* Responsive performance.

* Reliability and error handling.

* Maintainable and modular architecture.

* Data consistency and integrity.

* Compatibility with modern browsers.

* Extensibility for future enhancements.

* Portability through containerization.

* Appropriate backup and recovery practices.

### 8. Project Scope

The project will focus on career exploration, skill assessment, career matching, skill-gap analysis, and learning recommendations.

Native mobile applications, a full recruitment platform, guaranteed job placement, and enterprise-scale infrastructure are excluded from the current implementation.

Advanced AI features, external job portal integration, and premium payment services may be considered based on time and technical feasibility.

### 9. Minimum Viable Product

The MVP will include authentication, student profiles, skill management, assessment, career profiles, career matching, skill-gap analysis, learning recommendations, dashboard functionality, and administration.

These features will be prioritized before optional enhancements.

### 10. Proposed Technology Stack

| Layer             | Technology                           |
| ----------------- | ------------------------------------ |
| Frontend          | React                                |
| Backend           | Spring Boot                          |
| Database          | PostgreSQL                           |
| AI/ML             | Python or an appropriate AI service  |
| API Communication | REST API                             |
| Containerization  | Docker                               |
| Version Control   | Git and GitHub                       |
| Deployment        | Suitable cloud or server environment |

### 11. Expected Outcome

The expected outcome is a functional web application that enables students and job seekers to understand their current skills, explore suitable career opportunities, identify areas for improvement, and receive learning recommendations.

The platform will demonstrate the practical integration of web development, database management, custom algorithms, and AI-assisted functionality in a career development context.

