# Boundary Value Analysis (BVA)

## Module Summary

This module validates the **username field constraints during user registration**.

The purpose of these tests is to verify how the system behaves when the **input values are at the boundaries of the allowed range**, including values **just below, equal to, and just above the limits**.

Boundary Value Analysis helps ensure that the system correctly enforces validation rules at critical input limits.

---

# Business Rule

The system must allow user registration **only if the username contains between 6 and 30 valid characters**.

Values outside this range must be rejected and the user must be notified with an appropriate validation message.

---

# Boundary Values

| Boundary Type | Value         | Expected Behavior |
| ------------- | ------------- | ----------------- |
| Minimum -1    | 5 characters  | Invalid           |
| Minimum       | 6 characters  | Valid             |
| Minimum +1    | 7 characters  | Valid             |
| Maximum -1    | 29 characters | Valid             |
| Maximum       | 30 characters | Valid             |
| Maximum +1    | 31 characters | Invalid           |

---

# Test Cases

---

## TC_BVA_01

**Title:** Validate username with 5 characters (Minimum -1)

**Type:** Functional - Boundary Value Analysis (Negative)

**Module:** Registration

**Priority:** High

**ID:** BVA-01

**Precondition:**
User must be on the registration page with all other fields filled with valid values.

### Steps

1. Access the register page
2. Fill all valid fields correctly
3. Enter a value with **5 valid characters** in the "Username" field
4. Click the **Next** button

### Test Data

Minimum allowed characters: 6
Maximum allowed characters: 30

### Expected Result

The system must prevent the user from proceeding and display a message indicating that the field has not reached the minimum number of allowed characters.

### Actual Result

The system prevented the action and displayed the correct validation message.

### Status

Approved

---

## TC_BVA_02

**Title:** Validate username with 6 valid characters

**Type:** Functional - Boundary Value Analysis (Positive)

**Module:** Registration

**Priority:** High

**ID:** BVA-02

**Precondition:**
User must be on the registration page with all other fields filled with valid values.

### Steps

1. Access the register page
2. Fill all valid fields correctly
3. Enter a value with **6 valid characters** in the "Username" field
4. Click the **Next** button

### Test Data

Minimum allowed characters: 6
Maximum allowed characters: 30

### Expected Result

The system should allow the user to proceed without displaying an error message.

### Actual Result

The system allowed the user to proceed and no error message was displayed.

### Status

Approved

---

## TC_BVA_03

**Title:** Validate username with 31 characters (Maximum +1)

**Type:** Functional - Boundary Value Analysis (Negative)

**Module:** Registration

**Priority:** High

**ID:** BVA-03

**Precondition:**
User must be on the registration page with all other fields filled with valid values.

### Steps

1. Access the register page
2. Fill all valid fields correctly
3. Enter a value with **31 valid characters** in the "Username" field
4. Click the **Next** button

### Test Data

Minimum allowed characters: 6
Maximum allowed characters: 30

### Expected Result

The system must prevent the user from proceeding and display an error message indicating the character limit for that field.

### Actual Result

The system prevented the action and displayed the correct error message.

### Status

Approved

---

## TC_BVA_04

**Title:** Validate username with 7 characters (Minimum +1)

**Type:** Functional - Boundary Value Analysis (Positive)

**Module:** Registration

**Priority:** High

**ID:** BVA-04

**Precondition:**
User must be on the registration page with all other fields filled with valid values.

### Steps

1. Access the register page
2. Fill all valid fields correctly
3. Enter a value with **7 valid characters** in the "Username" field
4. Click the **Next** button

### Test Data

Minimum allowed characters: 6
Maximum allowed characters: 30

### Expected Result

The system should allow the user to proceed without displaying an error message.

### Actual Result

The system allowed the user to proceed without displaying any error message.

### Status

Approved

---

## TC_BVA_05

**Title:** Validate username with 29 characters (Maximum -1)

**Type:** Functional - Boundary Value Analysis (Positive)

**Module:** Registration

**Priority:** High

**ID:** BVA-05

**Precondition:**
User must be on the registration page with all other fields filled with valid values.

### Steps

1. Access the register page
2. Fill all valid fields correctly
3. Enter a value with **29 valid characters** in the "Username" field
4. Click the **Next** button

### Test Data

Minimum allowed characters: 6
Maximum allowed characters: 30

### Expected Result

The system should allow the user to proceed without displaying an error message.

### Actual Result

The system allowed the user to proceed without displaying any error message.

### Status

Approved

---

## TC_BVA_06

**Title:** Validate username with 30 valid characters

**Type:** Functional - Boundary Value Analysis (Positive)

**Module:** Registration

**Priority:** High

**ID:** BVA-06

**Precondition:**
User must be on the registration page with all other fields filled with valid values.

### Steps

1. Access the register page
2. Fill all valid fields correctly
3. Enter a value with **30 valid characters** in the "Username" field
4. Click the **Next** button

### Test Data

Minimum allowed characters: 6
Maximum allowed characters: 30

### Expected Result

The system should allow the user to proceed without displaying an error message.

### Actual Result

The system allowed the user to proceed without displaying any error message.

### Status

Approved
