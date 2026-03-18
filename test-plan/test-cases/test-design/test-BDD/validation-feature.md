# Module Summary: User Authentication - Data Validation

## Overview

The **Data Validation module** within User Authentication ensures that all user inputs meet the defined business rules before allowing access to the system.

This module focuses on preventing invalid data from being processed, ensuring both **security** and **data integrity** during the login process.

---

## Business Rules

**BR-01**
The system must allow authentication only if the user's password length is between 8 and 30 characters.

**BR-02**
The system must allow authentication only if the username length is between 6 and 30 characters.

---

## Validation Constraints

### Username

* Minimum length: **6 characters**
* Maximum length: **30 characters**

| Condition                   | Expected Behavior                      |
| --------------------------- | -------------------------------------- |
| Less than 6 characters      | Reject input and display error message |
| Between 6 and 30 characters | Accept input                           |
| More than 30 characters     | Reject input and display error message |

---

### Password

* Minimum length: **8 characters**
* Maximum length: **30 characters**

| Condition                   | Expected Behavior                      |
| --------------------------- | -------------------------------------- |
| Less than 8 characters      | Reject input and display error message |
| Between 8 and 30 characters | Accept input                           |
| More than 30 characters     | Reject input and display error message |

---

# Feature: User Authentication - Data Validation

---

# BDD-01

## Scenario: Reject login with username shorter than 6 characters

Given the user is on the login page

When the user enters a username with 3 characters
And enters a valid password
And submits the login form

Then the system should display an error message
And the user should not be allowed to proceed

---

# BDD-02

## Scenario: Reject login with password shorter than 8 characters

Given the user is on the login page

When the user enters a valid username
And enters a password with 5 characters
And submits the login form

Then the system should display an error message
And the user should not be allowed to proceed

---

# BDD-03

## Scenario: Reject login with password longer than 30 characters

Given the user is on the login page

When the user enters a valid username
And enters a password with 35 characters
And submits the login form

Then the system should display an error message
And the user should not be allowed to proceed

