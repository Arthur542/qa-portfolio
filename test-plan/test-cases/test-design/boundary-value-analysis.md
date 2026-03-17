# Boundary Value Analysis (BVA)

## Module Summary

This document contains test cases created using the Boundary Value Analysis technique to validate the username field limits in the registration form.

The tests verify how the system behaves when values are inserted at the minimum and maximum boundaries of the allowed input range.

## Business Rules

BR-BVA-01: The system must enforce the minimum character limit for the username field.

BR-BVA-02: The system must enforce the maximum character limit for the username field.

BR-BVA-03: The system must allow usernames that fall within the valid character range.

## Field Information

Field: Username

Minimum allowed length: 6 characters  
Maximum allowed length: 30 characters

## BVA-01 – Username with 5 characters (Minimum -1)

**Type:** Boundary Value Analysis – Negative  
**Priority:** High  
**Module:** Registration  
**Precondition:**  
User must be on the registration page with all other required fields filled correctly.

**Test Steps:**

1. Access the register page  
2. Fill all required fields correctly  
3. Enter a username containing 5 characters valid 
4. Click the "Next" button  

**Test Data**

Minimum allowed: 6 characters  
Maximum allowed: 30 characters  

**Expected Result**

The system should display a validation message informing that the username does not meet the minimum character requirement.

**Obtained Result**

The system displayed the message correctly.

**Status:** Passed

---

## BVA-02 – Username with 6 characters (Minimum)

**Type:** Boundary Value Analysis – Positive  
**Priority:** High  
**Module:** Registration  
**Precondition:**  
User must be on the registration page with all other required fields filled correctly.

**Test Steps**

1. Access the register page  
2. Fill all required fields correctly  
3. Enter a username containing 6 characters valid  
4. Click the "Next" button  

**Expected Result**

The system should accept the username and allow the user to proceed to the next step of the registration process.

**Obtained Result**

The system accepted the username and allowed the user to proceed.


**Status:** Passed

---

## BVA-03 – Username with 31 characters (Maximum +1)

**Type:** Boundary Value Analysis – Negative  
**Priority:** High  
**Module:** Registration  
**Precondition:**  
User must be on the registration page with all required fields filled correctly.

**Test Steps**

1. Access the register page  
2. Fill all required fields correctly  
3. Enter a username containing 31 characters valid
4. Click the "Next" button  

**Expected Result**

The system should display a validation message informing that the username exceeded the maximum character limit.

**Obtained Result**

The system displayed the message correctly.

**Status:** Passed

---

## BVA-04 – Username with 7 characters (Minimum +1)

**Type:** Boundary Value Analysis – Positive  
**Priority:** High  
**Module:** Registration  
**Precondition:**  
User must be on the registration page with all required fields filled correctly.

**Test Steps**

1. Access the register page  
2. Fill all required fields correctly  
3. Enter a username containing 7 characters valid 
4. Click the "Next" button  

**Expected Result**

The system should accept the username and allow the user to proceed.

**Obtained Result**

The system accepted the username and allowed the user to proceed.

**Status:** Passed

---

## BVA-05 – Username with 29 characters (Maximum -1)

**Type:** Boundary Value Analysis – Positive  
**Priority:** High  
**Module:** Registration  
**Precondition:**  
User must be on the registration page with all required fields filled correctly.

**Test Steps**

1. Access the register page  
2. Fill all required fields correctly  
3. Enter a username containing 29 characters valid
4. Click the "Next" button  

**Expected Result**

The system should accept the username and allow the user to proceed.

**Obtained Result**

The system accepted the username and allowed the user to proceed.

**Status:** Passed

---

## BVA-06 – Username with 30 characters (Maximum)

**Type:** Boundary Value Analysis – Positive  
**Priority:** High  
**Module:** Registration  
**Precondition:**  
User must be on the registration page with all required fields filled correctly.

**Test Steps**

1. Access the register page  
2. Fill all required fields correctly  
3. Enter a username containing 30 characters valid
4. Click the "Next" button  

**Expected Result**

The system should accept the username and allow the user to proceed to the next step.

**Obtained Result**

The system accepted the username and allowed the user to proceed.

**Status:** Passed

---
