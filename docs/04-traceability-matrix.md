# 🗺️ Requirements Traceability Matrix (RTM)

**Target Application:** [Belajar Bareng Web App](https://belajar-bareng.onrender.com)

---

## 📌 Executive Summary

The Requirements Traceability Matrix (RTM) ensures complete test coverage across all core modules and requirements of the **Belajar Bareng** web application. It maps business requirements to corresponding test cases, execution statuses, and reported defects.

---

## 📊 Traceability Matrix Table

| Requirement ID  | Module / Feature Description | Test Case ID | Test Case Title                                           | Test Status | Associated Bug ID |
| --------------- | ---------------------------- | ------------ | --------------------------------------------------------- | ----------- | ----------------- |
| **REQ-AUTH-01** | User Authentication (Login)  | `TC-LOG-001` | Login with valid credentials                              | **PASS**    | None              |
| **REQ-AUTH-01** | User Authentication (Login)  | `TC-LOG-002` | Login with incorrect password                             | **PASS**    | None              |
| **REQ-AUTH-01** | User Authentication (Login)  | `TC-LOG-003` | Login with empty fields                                   | **PASS**    | None              |
| **REQ-USR-01**  | View User List               | `TC-USR-001` | Verify user list table displays Name, Age, and ID columns | **PASS**    | None              |
| **REQ-USR-02**  | Add New User                 | `TC-USR-002` | Add a new user with valid data                            | **PASS**    | None              |
| **REQ-USR-02**  | Add New User                 | `TC-USR-003` | Add user with text/letters in Age field                   | **PASS**    | None              |
| **REQ-USR-02**  | Add New User                 | `TC-USR-004` | Add user with empty fields                                | **PASS**    | None              |
| **REQ-USR-02**  | Add New User                 | `TC-USR-005` | Add user with a negative Age value                        | **PASS**    | None              |
| **REQ-USR-03**  | Update User                  | `TC-USR-006` | Update Username and Age of a selected user                | **PASS**    | None              |
| **REQ-USR-04**  | Delete User                  | `TC-USR-007` | Delete a selected user from the system                    | **PASS**    | None              |
| **REQ-SHP-01**  | Dashboard Quick Checkout     | `TC-SHP-001` | Access Checkout via main Dashboard button (Initial Flow)  | **FAIL**    | `BUG-001`         |
| **REQ-SHP-02**  | Shop Catalog Access          | `TC-SHP-002` | Access Shop / Product Catalog via Cart icon               | **PASS**    | None              |
| **REQ-SHP-03**  | Add Item to Cart             | `TC-SHP-003` | Add product to Shopping Cart                              | **PASS**    | None              |
| **REQ-SHP-04**  | Cart Quantity Adjustment     | `TC-SHP-004` | Update item quantity (Qty) in Shopping Cart               | **PASS**    | None              |
| **REQ-SHP-05**  | Order Checkout & Form        | `TC-SHP-005` | Fill Checkout Form & complete order                       | **FAIL**    | `BUG-002`         |
| **REQ-SHP-05**  | Order Checkout Validation    | `TC-SHP-006` | Checkout without checking Terms & Conditions              | **PASS**    | None              |
| **REQ-SHP-05**  | Math Captcha Verification    | `TC-SHP-007` | Checkout with incorrect Math Captcha answer               | **FAIL**    | `BUG-002`         |
| **REQ-TRK-01**  | Track Booking Details        | `TC-TRK-001` | Track booking using a valid Booking Code                  | **PASS**    | None              |
| **REQ-TRK-01**  | Track Booking Validation     | `TC-TRK-002` | Track booking with an unregistered Booking Code           | **PASS**    | None              |

---

## 📈 Coverage Summary

- **Total Requirements Identified:** 9 Requirements (`REQ-AUTH-01` to `REQ-TRK-01`)
- **Total Test Cases Executed:** 19 Test Cases
- **Passed Test Cases:** 16 (84.2%)
- **Failed Test Cases:** 3 (15.8%)
- **Open Defects Tracked:** 2 (`BUG-001`, `BUG-002`)
