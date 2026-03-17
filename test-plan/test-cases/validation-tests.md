# Input Validation Test Cases

This document contains manual test cases designed to validate the system's input validation behavior.

## Business Rules

BR-VAL-01: The system must prevent login when an invalid password is provided.

BR-VAL-02: The system must prevent login when an invalid username is provided.

BR-VAL-03: The system must prevent form submission when required fields are empty.

## VAL-01 – Login with invalid password

**Type:** Negative  
**Priority:** High  
**Module:** Input Validation  
**Precondition:**  
User must be previously registered in the system.

**Test Steps:**

1. Access the login page  
2. Enter a valid username  
3. Enter an invalid password  
4. Click the login button  

**Test Data:**

Username: tomsmith  
Password: SuperSecretPassword123  

**Expected Result:**  
The system should prevent access to the secure page and display an "Invalid credentials" message.

**Actual Result:**  
The system prevented access to the secure page and displayed the invalid credentials message.

**Status:** Passed

---

## VAL-02 – Login with invalid username

**Type:** Negative  
**Priority:** High  
**Module:** Input Validation  
**Precondition:**  
The system must be accessible.

**Test Steps:**

1. Access the login page  
2. Enter an invalid username  
3. Enter a valid password  
4. Click the login button  

**Test Data:**

Username: tomsmith123  
Password: SuperSecretPassword!  

**Expected Result:**  
The system should prevent access to the secure page and display an "Invalid credentials" message.

**Actual Result:**  
The system prevented access to the secure page and displayed the invalid credentials message.

**Status:** Passed

---

## VAL-03 – Submit form with empty username field

**Type:** Negative  
**Priority:** High  
**Module:** Input Validation  
**Precondition:**  
User must be on the registration page with all other fields filled correctly.

**Test Steps:**

1. Access the registration page  
2. Fill all required fields correctly  
3. Leave the "Username" field empty  
4. Click the "Next" button  

**Test Data:**

Minimum characters allowed: 6  
Maximum characters allowed: 30  

**Expected Result:**  
The system should prevent form submission and display an error message.

**Actual Result:**  
The system prevented the submission and displayed the error message correctly.

**Status:** Passed

---
