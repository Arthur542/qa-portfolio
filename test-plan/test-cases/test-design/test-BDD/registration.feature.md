# Module Summary: User Authentication

## Overview

The **User Authentication module** ensures that only users with valid credentials can access secure areas of the system.
This module verifies both **username** and **password** according to business rules, preventing unauthorized access and enforcing proper data validation.

---

# Feature: User Authentication

## Business Rule

**BR-01**
The system must allow authentication only for users with valid credentials.

**BR-02**
The system should only allow authentication if the user's password is between 8 and 30 characters long.


**BR-03**
The system must allow authentication only for users whose username contains between 6 and 30 characters.

---

# BDD-01

## Scenario: Successful login with valid credentials

Given the user is on the login page

When the user enters valid credentials
And submits the login form

Then the system should grant access to the secure page

---

# BDD-02

## Scenario: Successful login with a valid password

Given that the user is on the login page

When the user enters a valid username
And enters a password between 8 and 30 characters
And submits the login form

Then the system should grant access to the secure page

---

# BDD-03

## Scenario: Successful login with username between 6 and 30 characters

Given the user is on the login page

When the user enters a username between 6 and 30 characters
And enters a valid password
And submits the login form

Then the system should grant access to the secure page
