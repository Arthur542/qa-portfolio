# Session Control Test Cases

This document contains manual test cases designed to validate session management behavior in the system.

The tests verify whether the system properly maintains authenticated sessions, handles logout correctly, and prevents unauthorized access to protected pages.

## Business Rules

BR-SESSION-01: The system must maintain the user session while the user is authenticated.

BR-SESSION-02: The system must allow the user to log in again after performing logout.

BR-SESSION-03: The system must prevent access to protected pages when the user is not authenticated.

BR-SESSION-04: The system must prevent access to protected pages after the user performs logout.

## SESSION-01 – Refresh secure page while authenticated

**Type:** Positive  
**Priority:** High  
**Module:** Session Control  
**Precondition:**  
User must be authenticated and currently on the secure page.

**Test Steps:**

1. While on the secure page, press "F5" or click the browser "refresh" button.

**Expected Result:**  
The system should maintain the active session and keep the user on the secure page.

**Actual Result:**  
The system maintained the active session and remained on the secure page.

**Status:** Passed

---

## SESSION-02 – Login again immediately after logout

**Type:** Positive  
**Priority:** High  
**Module:** Session Control  
**Precondition:**  
User must be previously registered in the system.

**Test Steps:**

1. Access the website: https://the-internet.herokuapp.com/login
2. Access the login page  
3. Enter a valid username and password  
4. Click the "Login" button  
5. On the secure page, click "Logout"  
6. On the login page, enter valid credentials again  
7. Click the "Login" button

**Test Data:**

Username: tomsmith  
Password: SuperSecretPassword!

**Expected Result:**  
The system should authenticate the user again, redirect to the secure page, and display a success message.

**Actual Result:**  
The system authenticated the user again, redirected to the secure page, and displayed the success message.

**Status:** Passed

---

## SESSION-03 – Attempt to access secure page via URL without authentication

**Type:** Negative  
**Priority:** High  
**Module:** Session Control  
**Precondition:**  
User must not be authenticated in the system.

**Test Steps:**

1. Open the browser in incognito mode  
2. Enter the URL directly in the browser: https://the-internet.herokuapp.com/secure  
3. Press "Enter"  

**Expected Result:**  
The system should block access to the secure page and redirect the user to the login page.

**Actual Result:**  
The system blocked access to the secure page and redirected to the login page.

**Status:** Passed

---

## SESSION-04 – Attempt to access secure page via URL after logout

**Type:** Negative  
**Priority:** High  
**Module:** Session Control  
**Precondition:**  
User must be authenticated and then perform logout.

**Test Steps:**

1. Login with valid credentials  
2. On the secure page, click "Logout"  
3. In the same browser tab, type the URL directly: https://the-internet.herokuapp.com/secure  
4. Press "Enter"

**Test Data:**

Username: tomsmith  
Password: SuperSecretPassword!

**Expected Result:**  
The system should prevent access to the secure page and redirect to the login page.

**Actual Result:**  
The system redirected to the login page successfully.

**Status:** Passed

---
