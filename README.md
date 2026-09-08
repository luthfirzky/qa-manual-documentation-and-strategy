# 🧪 Manual QA Testing Documentation & Strategy

This repository contains end-to-end manual testing documentation for the **[Belajar Bareng](https://belajar-bareng.onrender.com)** web.

It is structured to showcase a methodical testing approach within an _Agile/Scrum_ software development lifecycle—covering test strategy planning, detailed test suite design, bug reporting, and requirements traceability.

---

## 📌 Project Overview

| Attribute              | Details                                                                      |
| ---------------------- | ---------------------------------------------------------------------------- |
| **Target Application** | [Belajar Bareng Web App](https://belajar-bareng.onrender.com)                |
| **Testing Types**      | Functional Testing, Negative Testing, Boundary Value Analysis, UI/UX Testing |
| **Feature Scope**      | Authentication (Login), User Management (CRUD), Checkout / E-commerce        |
| **Deliverables**       | Test Plan, Test Cases, Bug Reports, Requirements Traceability Matrix (RTM)   |

---

## 📂 Testing Documentation Index

Explore the core test artifacts in the [`docs/`](./docs) directory:

1. 📋 **[Test Plan & Strategy](./docs/01-test-plan.md)**
   - Outlines the testing approach, scope (_in-scope & out-of-scope_), _entry/exit criteria_, and risk management strategy.
2. 🧪 **[Test Cases Suite](./docs/02-test-cases.md)**
   - Comprehensive list of manual test scenarios (Positive & Negative Cases) covering Login, User List, Add User, Update User, Delete User, and Checkout modules.
3. 🐛 **[Bug Reports](./docs/03-bug-reports.md)**
   - Detailed bug reports discovered during testing—complete with _Steps to Reproduce_, _Severity_, _Priority_, and visual evidence (_Screenshots_).
4. 🔗 **[Requirements Traceability Matrix (RTM)](./docs/04-traceability-matrix.md)**
   - Maps functional requirements directly to Test Case IDs to guarantee 100% test coverage.

---

## 🛠️ Testing Methodology

Testing was performed using _Black-Box Testing_ techniques, focusing on:

- **Equivalence Partitioning:** Segmenting input data into valid and invalid partitions to test system handling.
- **Negative & Exploratory Testing:** Executing edge cases and unintended user journeys to discover validation weaknesses.
