# 🐛 Bug Reports

**Target Application:** [Belajar Bareng Web App](https://belajar-bareng.onrender.com)

---

## 📌 Summary of Reported Bugs

| Bug ID      | Title                                                                 | Severity | Priority | Status | Related Test Case      |
| ----------- | --------------------------------------------------------------------- | -------- | -------- | ------ | ---------------------- |
| **BUG-001** | Dashboard Checkout Button Displays "Congrats, you found a bug!" Modal | High     | High     | Open   | TC-SHP-001             |
| **BUG-002** | Captcha Text Element Overlapped by Refresh Button in Checkout Modal   | Medium   | High     | Open   | TC-SHP-005, TC-SHP-007 |

---

## 📑 Detailed Bug Logs

### 1. BUG-001: Dashboard Checkout Button Displays "Congrats, you found a bug!" Modal

- **Bug ID:** `BUG-001`
- **Severity:** High
- **Priority:** High
- **Status:** Open
- **Related Test Case:** `TC-SHP-001`
- **Component / Module:** Main Dashboard / Checkout Button

#### Description

Clicking the blue "Checkout" button located on the main dashboard page (underneath the "Delete User" section) triggers an unexpected error modal displaying the text _"Congrats, you found a bug!"_ instead of leading the user to a functional checkout flow.

#### Steps to Reproduce

1. Log in to the application with valid credentials.
2. Navigate to the main Dashboard page.
3. Scroll down past the "Delete User" section.
4. Click the blue **"Checkout"** button.

#### Expected Result

The user should either be directed to a valid Checkout page/modal or the button should be properly linked to the E-Commerce shopping flow.

#### Actual Result

An unexpected modal pops up displaying the message: `"Congrats, you found a bug!"`.

---

### 2. BUG-002: Captcha Text Element Overlapped by Refresh Button in Checkout Modal

- **Bug ID:** `BUG-002`
- **Severity:** Medium
- **Priority:** High
- **Status:** Open
- **Related Test Case:** `TC-SHP-005`, `TC-SHP-007`
- **Component / Module:** E-Commerce / Checkout Form Modal (Math Captcha)

#### Description

On the Checkout Form modal (where users enter their order details), the Math Captcha text/question is partially or fully obscured by the Refresh button (_overlapping UI element_). This makes it difficult for users to read the math problem required to complete the verification step.

#### Steps to Reproduce

1. Access the application and go to the **Shop** page (Product Catalog).
2. Add at least 1 product to the cart and navigate to the **Shopping Cart** page.
3. Click the **"Checkout"** button to open the Checkout Form modal.
4. Observe the **Math Captcha** input section.

#### Expected Result

The Math Captcha text and the Refresh button should have proper spacing, padding, and layout alignment so that the math equation is clearly readable.

#### Actual Result

The Captcha equation text is overlapped by the Refresh icon/button, obscuring the numbers from clear view.
