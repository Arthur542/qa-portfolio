# Bug Report: Name Field Validation Failure

## Module Summary

This module validates **text input fields**, ensuring that user-provided data meets minimum requirements before form submission.

Special attention is given to fields like **Full Name**, which must contain sufficient and meaningful input to ensure data quality.

---

## Business Rule

* The **Full Name field must require a valid and complete input**
* The system must reject inputs that are too short or incomplete
* The field must enforce a **minimum number of characters**
* The system must display an error message when validation fails

---

## Bug Details

* **ID:** BUG-03
* **Title:** Full Name field accepts invalid input (single character)
* **Type:** Input Validation Error
* **Module:** Text Input
* **Priority:** High
* **Severity:** High
* **Status:** Open

---

## Environment

* **Browser:** Google Chrome
* **Operating System:** Windows 11
* **Environment:** Test

---

## Precondition

* User is on the **"Text Box" form page**

---

## Steps to Reproduce

1. Access the website: https://demoqa.com
2. Navigate to the **"Forms"** section
3. Fill in all required fields with valid data
4. Enter only **1 character** in the "Full Name" field
5. Click on **"Submit"**

---

## Test Data

* **Full Name:** "A"

---

## Expected Result

The system must prevent form submission and display an error message indicating that the full name is invalid or incomplete.

---

## Actual Result

The system allows form submission even when the "Full Name" field contains only 1 character.

---

## Impact

* Invalid user data is accepted
* Data quality is compromised
* Potential issues in user identification
* Lack of proper input validation

---
