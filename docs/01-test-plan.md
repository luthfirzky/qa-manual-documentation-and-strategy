# 📋 Test Plan & Strategy

## Project

**Platform User Management & Checkout (Belajar Bareng)**

---

## Objective

To test the functionality when a user logs in, views the user list, adds, updates, deletes users, and accesses the checkout feature to ensure the system operates securely, maintains data integrity, and remains free of critical bugs.

---

## Scope

- User authentication & login workflow on the web application.
- User Management: Viewing user list (ID, Name, Age), Add User form, Update User form, and Delete User form.
- Redirection and core workflow of the Checkout / E-commerce module.
- Input validation and error handling (such as age boundary testing and empty field checks).

---

## Features to Test

- **Login Functionality:** Valid/invalid credentials and field input validations.
- **User Management (View List):** Verifying the user table displays ID, Name, and Age columns accurately.
- **User Management (Add User):** Adding new users and input/error validation checks.
- **User Management (Update User):** Updating Username and Age for a selected user.
- **User Management (Delete User):** Deleting a selected user from the system.
- **Checkout Functionality:** Accessing and redirection to the e-commerce/checkout page.

---

## Exclusions

- Advanced Security Penetration Testing & Vulnerability Scanning.
- Performance & Stress Testing under high concurrent traffic (handled in the API Automation repository).
- Legacy browser compatibility (e.g., Internet Explorer).

---

## Test Strategy

- **Functional Testing:** Black-box testing using Equivalence Partitioning & Boundary Value Analysis for form inputs.
- **User Acceptance Testing (UAT):** Verifying end-to-end user workflows against business expectations.

---

## Resources

- **Team:** 1 QA Engineer
- **Tools:** Staging/Production-like test environment (Render hosting), Google Chrome, VS Code, Git/GitHub.

---

## Risks

- Network latency or server issues due to cold-starts on the free-tier Render server.
- Potential lack of backend input validation (e.g., accepting text/letters in the Age field).
- Test execution delays if the test environment experiences downtime.

---

## Deliverables

- Test Plan & Strategy documentation
- Test Cases Suite
- Bug Reports with visual evidence (screenshots)
- Requirements Traceability Matrix (RTM)
- Final Test Execution Summary

---

## Success Criteria

- 100% pass rate on high-priority test cases.
- Zero (0) critical or high-severity bugs open.
- Approval from UAT stakeholders.

---

## Environment

- **Target URL:** https://belajar-bareng.onrender.com
- **Server:** Staging / Production-like environment (Render hosting)
- **Devices & Network:** Desktop devices (Windows/macOS), Google Chrome browser, standard network simulation.
