# quality-engineering-playbook
Comprehensive onboarding guide and QA strategy for high-performance teams. Focused on Shift-left, Accessibility, and Data Integrity.
# 🚀 QA Strategy & Junior Onboarding Playbook
### *Driving Product Excellence through Strategic Quality Engineering & Mentorship*

Welcome. This repository serves as a strategic blueprint for modern software testing. As an **ISTQB® Certified Tester** and testing instructor, my focus is transitioning Quality from a final gatekeeper to a core organizational culture.

---

## 🎯 Quality Vision & Strategy
We don't just find bugs; we ensure business alignment through:
* **Shift-Left Testing**: Engaging from the refinement of User Stories  to mitigate risks before development begins.
* **Accessibility (A11y)**: Guaranteeing software is inclusive for all users by adhering to WCAG standards.
* **Stakeholder Management**: Delivering high-impact demos and reports for global clients (C2 Proficiency ).

---

## 🛠️ Tech Stack & Essential Toolkit
Proficiency in these tools is mandatory for our Agile/Scrum workflow:

| Category | Tools |
| :--- | :--- |
| **Project & Bug Tracking** | JIRA, Azure DevOps, Mantis, RedMine  |
| **Test Management** | Test Link, TestRail, Xray  |
| **Technical Analysis** | SQL (Data Integrity), Postman, Rapid Reporter  |

---

## 📋 Quality Standards (The Senior Framework)

### 1. Defect Lifecycle Management
We proactively report, monitor, and validate bugs. A "Definition of Done" report must include:
* Clear, reproducible steps.
* Technical evidence (Logs, Console errors, Screenshots).
* Business impact analysis.

### 2. Data Integrity (SQL for QA)
We validate the "truth" behind the UI. Our team uses SQL to:
* Ensure backend data persistence.
* Verify complex business logic and edge cases.
* Prepare controlled data sets for functional execution.

### 3. Accessibility & Compliance
We actively conduct accessibility testing to ensure applications meet global compliance guidelines.

---

## 🤖 GenAI Strategy in Quality Engineering
Leveraging Google Cloud GenAI to accelerate the testing lifecycle and enhance precision. My strategy focuses on three core pillars:

### 1. Requirements Analysis & Test Design
* **User Story Refinement:** Using LLMs to identify edge cases, missing acceptance criteria, and potential ambiguities in requirements during the Shift-Left phase.
* **Synthetic Data Generation:** Prompting for complex, anonymized datasets to test SQL edge cases without compromising real user data.

### 2. Efficiency & Documentation
* **Test Case Optimization:** Transforming high-level requirements into detailed, structured test steps, reducing manual drafting time by ~40%.
* **Root Cause Analysis (RCA) Support:** Feeding sanitized log data to GenAI to identify patterns in complex defects and accelerate the reporting process.

### 3. Risk Assessment & Exploratory Testing
* **Predictive Risk Mapping:** Utilizing GenAI to suggest high-risk areas based on historical bug patterns and code change impact analysis.

> [!TIP]
> **Responsible AI:** All GenAI interactions follow strict data privacy protocols. No PII (Personally Identifiable Information) or proprietary client code is ever shared with public LLMs.

---

## 🧰 Integrated AI Toolkit
To see these strategies in action, explore my specialized prompt libraries designed to accelerate the testing lifecycle:

| 🦾 Accessibility (A11y) | 💾 Data Integrity (SQL) |
| :--- | :--- |
| Strategic prompts for WCAG 2.1/2.2 compliance, screen readers, and keyboard navigation. | Advanced patterns for ACID compliance, synthetic data, and migration auditing. |
| [**View A11y Prompts →**](./prompts/accessibility-login.md) | [**View SQL Prompts →**](./prompts/sql-data-integrity.md) |

---
## 🧠 Quality Fundamentals & Strategy

As a **Certified Tester (ISTQB®)**, my approach is built on a solid theoretical foundation that ensures efficiency and risk mitigation throughout the SDLC.

<details>
<summary><b>Click to expand: The 7 Fundamental Principles of Testing</b></summary>

These principles guide my decision-making process when planning and executing comprehensive tests:

1.  **Testing shows the presence of defects, not their absence:** Our goal is to reduce the probability of undiscovered defects. A clean test run doesn't mean the software is 100% bug-free.
2.  **Exhaustive testing is impossible:** I use risk analysis and prioritization to focus efforts on what matters most for project success.
3.  **Early testing (Shift-Left):** We start testing as early as possible—validating user stories and requirements—to find defects when they are cheaper to fix.
4.  **Defect clustering:** Experience shows that a small number of modules usually contain most defects. I target deep-dive sessions in these critical areas.
5.  **Pesticide paradox:** I regularly review and update test cases and documentation to ensure they remain effective in identifying new issues.
6.  **Testing is context-dependent:** The testing approach is adapted based on the specific needs of the application and stakeholders.
7.  **Absence-of-errors fallacy:** Fixing bugs is irrelevant if the system fails to fulfill user needs and expectations. I focus on delivering high-quality software solutions that align with end-user requirements.

</details>

## 🎓 About the Lead
I am **Ana González Lamé**, a Quality Engineering Analyst with 6+ years of experience. 
* **Senior QC Analyst** at Globant.
* **Professional Testing Master** (UTN FRBA).
* **Women Techmakers Ambassador** & International Speaker.
* **C2 Proficiency** in English.

---

> [!IMPORTANT]
> **New to the team?** Start by reviewing our "Test Strategies" section to understand how we plan and organize comprehensive testing for diverse applications.
