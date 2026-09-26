# 🧪 Test Cases Suite

**Target Application:** [Belajar Bareng Web App](https://belajar-bareng.onrender.com)

---

## 🔑 Module 1: Authentication (Login)

| Test Case ID   | Test Type | Test Scenario                 | Pre-conditions                                        | Test Steps                                                                    | Expected Result                                                                    | Status | Priority |
| -------------- | --------- | ----------------------------- | ----------------------------------------------------- | ----------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ------ | -------- |
| **TC-LOG-001** | Positive  | Login with valid credentials  | 1. User account is registered<br>2. On the Login page | 1. Enter valid username<br>2. Enter valid password<br>3. Click "Login" button | Successfully logged in and redirected to the Dashboard / User List page            | PASS   | High     |
| **TC-LOG-002** | Negative  | Login with incorrect password | 1. User account is registered<br>2. On the Login page | 1. Enter valid username<br>2. Enter wrong password<br>3. Click "Login" button | System displays an error message "Invalid credentials" and stays on the login page | PASS   | High     |
| **TC-LOG-003** | Negative  | Login with empty fields       | 1. On the Login page                                  | 1. Leave Username and Password fields empty<br>2. Click "Login" button        | System displays validation warnings indicating fields are required                 | PASS   | Medium   |

---

## 📋 Module 2: User Management - View User List

| Test Case ID   | Test Type | Test Scenario                                             | Pre-conditions                                                  | Test Steps                     | Expected Result                                                 | Status | Priority |
| -------------- | --------- | --------------------------------------------------------- | --------------------------------------------------------------- | ------------------------------ | --------------------------------------------------------------- | ------ | -------- |
| **TC-USR-001** | Positive  | Verify user list table displays Name, Age, and ID columns | 1. Active login session<br>2. On the Dashboard / User List page | 1. Inspect the user data table | Table displays user data with header columns: ID, Name, and Age | PASS   | High     |

---

## ➕ Module 3: User Management - Add User

| Test Case ID   | Test Type | Test Scenario                           | Pre-conditions                                      | Test Steps                                                                                                              | Expected Result                                                      | Status | Priority |
| -------------- | --------- | --------------------------------------- | --------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- | ------ | -------- |
| **TC-USR-002** | Positive  | Add a new user with valid data          | 1. Active login session<br>2. On the Dashboard page | 1. Click "Add User" action<br>2. Enter valid Username (e.g., "Budi")<br>3. Enter valid Age (e.g., 25)<br>4. Submit form | New user is successfully added and displayed in the User List table  | PASS   | High     |
| **TC-USR-003** | Negative  | Add user with text/letters in Age field | 1. Active login session<br>2. On the Add User form  | 1. Enter valid Username ("Budi")<br>2. Enter text in Age field ("Twenty")<br>3. Submit form                             | System rejects input with a validation error "Age must be a number"  | FAIL   | High     |
| **TC-USR-004** | Negative  | Add user with empty fields              | 1. Active login session<br>2. On the Add User form  | 1. Leave Username and Age fields empty<br>2. Submit form                                                                | System displays required field warnings and prevents saving data     | PASS   | Medium   |
| **TC-USR-005** | Negative  | Add user with a negative Age value      | 1. Active login session<br>2. On the Add User form  | 1. Enter valid Username ("Budi")<br>2. Enter negative number in Age field (e.g., -5)<br>3. Submit form                  | System rejects input and displays positive number validation message | FAIL   | Medium   |

---

## ✏️ Module 4: User Management - Update User

| Test Case ID   | Test Type | Test Scenario                              | Pre-conditions                                                                             | Test Steps                                                                                                    | Expected Result                                        | Status | Priority |
| -------------- | --------- | ------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ | ------ | -------- |
| **TC-USR-006** | Positive  | Update Username and Age of a selected user | 1. Active login session<br>2. At least 1 user exists in system<br>3. On the Dashboard page | 1. Click "Update User" action<br>2. Select User from dropdown<br>3. Change Username and Age<br>4. Submit form | Selected user's data is updated in the User List table | PASS   | Medium   |

---

## 🗑️ Module 5: User Management - Delete User

| Test Case ID   | Test Type | Test Scenario                          | Pre-conditions                                                                             | Test Steps                                                                            | Expected Result                                               | Status | Priority |
| -------------- | --------- | -------------------------------------- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- | ------------------------------------------------------------- | ------ | -------- |
| **TC-USR-007** | Positive  | Delete a selected user from the system | 1. Active login session<br>2. At least 1 user exists in system<br>3. On the Dashboard page | 1. Click "Delete User" action<br>2. Select User to delete<br>3. Click "Delete" button | User is removed from the system and disappears from User List | PASS   | High     |

---

## 🛒 Module 6: E-Commerce & Checkout Flow

| Test Case ID   | Test Type | Test Scenario                                            | Pre-conditions                                                      | Test Steps                                                                                                                                | Expected Result                                                                                       | Status | Priority |
| -------------- | --------- | -------------------------------------------------------- | ------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ------ | -------- |
| **TC-SHP-001** | Negative  | Access Checkout via main Dashboard button (Initial Flow) | 1. Active login session<br>2. On the main Dashboard page            | 1. Click blue "Checkout" button under Delete action                                                                                       | User is directed to a valid checkout flow (Not a bug/error modal "Congrats, you found a bug!")        | FAIL   | High     |
| **TC-SHP-002** | Positive  | Access Shop / Product Catalog via Cart icon              | 1. Active login session<br>2. On the Dashboard page                 | 1. Click "Shopping!" cart icon at top left                                                                                                | User is redirected to "Welcome to the Shop!" page displaying product catalog                          | PASS   | High     |
| **TC-SHP-003** | Positive  | Add product to Shopping Cart                             | 1. On Product Catalog page ("Welcome to the Shop!")                 | 1. Choose desired product<br>2. Click "Add to Cart" button on item card                                                                   | Item count on "Cart (n)" indicator increases accordingly                                              | PASS   | High     |
| **TC-SHP-004** | Positive  | Update item quantity (Qty) in Shopping Cart              | 1. Items exist in Shopping Cart<br>2. On "Shopping Cart" page       | 1. Click `+` or `-` icon in Quantity column                                                                                               | Product quantity changes and Total Price updates automatically                                        | PASS   | Medium   |
| **TC-SHP-005** | Positive  | Fill Checkout Form & complete order                      | 1. On "Shopping Cart" page with items<br>2. Click "Checkout" button | 1. Enter Name, Email, and Address<br>2. Solve Math Captcha<br>3. Check "I accept the Terms & Conditions"<br>4. Click "Submit" button      | "Checkout Successful!" modal displays item details, total price, and Booking Code (e.g., BK-605067B5) | PASS   | High     |
| **TC-SHP-006** | Negative  | Checkout without checking Terms & Conditions             | 1. On "Checkout Form" modal                                         | 1. Fill Name, Email, Address, and Captcha validly<br>2. Leave Terms & Conditions checkbox unchecked<br>3. Click "Submit" button           | System blocks submission and asks user to accept Terms & Conditions                                   | PASS   | Medium   |
| **TC-SHP-007** | Negative  | Checkout with incorrect Math Captcha answer              | 1. On "Checkout Form" modal                                         | 1. Fill Name, Email, and Address<br>2. Enter incorrect answer to math question<br>3. Check Terms & Conditions<br>4. Click "Submit" button | System rejects checkout and shows captcha error message                                               | PASS   | High     |

---

## 🔍 Module 7: Track Booking

| Test Case ID   | Test Type | Test Scenario                                   | Pre-conditions                                                          | Test Steps                                                                                                | Expected Result                                                                                           | Status | Priority |
| -------------- | --------- | ----------------------------------------------- | ----------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | ------ | -------- |
| **TC-TRK-001** | Positive  | Track booking using a valid Booking Code        | 1. User has a Booking Code from previous transaction<br>2. On Shop page | 1. Click "Track Booking" button<br>2. Enter valid Booking Code in input field<br>3. Click "Search"        | "Booking Details" modal displays Name, Email, Address, Created Date, Item List, and Total Price correctly | PASS   | High     |
| **TC-TRK-002** | Negative  | Track booking with an unregistered Booking Code | 1. On Shop page                                                         | 1. Click "Track Booking" button<br>2. Enter invalid/random code (e.g., `BK-0000000`)<br>3. Click "Search" | System displays a message stating Booking Code is not found                                               | PASS   | Medium   |
