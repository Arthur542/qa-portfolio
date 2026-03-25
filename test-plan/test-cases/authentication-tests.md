# Authentication Test Cases

This document contains manual test cases created to validate the authentication functionality of the system.

The tests verify if users can successfully log into the system using valid credentials.
## Business Rules

BR-AUTH-01: System must allow login with valid credentials.

BR-AUTH-02: System must allow login using the Enter key.

## AUTH-01 – Login with valid credentials

**Type:** Positive  
**Priority:** High  
**Module:** Authentication  
**Precondition:**  
User must be previously registered in the system.

**Test Steps:**

1. Access the website: https://the-internet.herokuapp.com/login
2. Access the login page  
3. Enter a valid username  
4. Enter a valid password  
5. Click the "Login" button  

**Test Data:**

Username: tomsmith  
Password: SuperSecretPassword!

**Expected Result:**  
System should redirect to the secure page and display a success message.

**Actual Result:**  
System redirected to the secure page and displayed the success message.

**Status:** Passed

---
## AUTH-02 – Login using Enter key

**Type:** Positive  
**Priority:** High  
**Module:** Authentication  
**Precondition:**  
User must be previously registered in the system.

**Test Steps:**

1. Access the website: https://the-internet.herokuapp.com/login
2. Access the login page  
3. Enter a valid username  
4. Enter a valid password  
5. Press the "Enter" key  

**Test Data:**

Username: tomsmith  
Password: SuperSecretPassword!

**Expected Result:**  
System should redirect to the secure page and display a success message.

**Actual Result:**  
System redirected to the secure page and displayed the success message.

**Status:** Passed

---
