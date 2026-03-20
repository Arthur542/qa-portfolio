# Functional Testing – Positive Scenarios

## Authentication Module

---

### Scenario: Valid Login

User logs in using valid credentials and successfully accesses the secure area of the system.

**Expected Behavior:**
The system should authenticate the user and redirect to the secure page.

**Evidence:**

![Valid Login](../images.md/auth-login.png)

---

### Scenario: Login After Logout

User logs out from the system and then performs a new login using valid credentials.

**Expected Behavior:**
The system should allow the user to log in again and access the secure area normally.

**Evidence:**

![Login After Logout](../image.md/auth-valid-login.png)

---

