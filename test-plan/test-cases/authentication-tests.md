# Authentication Test Cases

This document contains manual test cases created to validate the authentication functionality of the system.

The tests verify if users can successfully log into the system using valid credentials and how the system behaves when invalid login attempts are performed.

## AUTH-01 – Login with valid credentials

**Type:** Positive  
**Priority:** High  
**Module:** Authentication  
**Precondition:**  
User must be previously registered in the system.

**Test Steps:**

1. Access the login page  
2. Enter a valid username  
3. Enter a valid password  
4. Click the login button  

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

1. Access the login page  
2. Enter a valid username  
3. Enter a valid password  
4. Press the Enter key  

**Test Data:**

Username: tomsmith  
Password: SuperSecretPassword!

**Expected Result:**  
System should redirect to the secure page and display a success message.

**Actual Result:**  
System redirected to the secure page and displayed the success message.

**Status:** Passed

---
