# Equivalence Partitioning (EP)

## Module Summary

This module covers **user registration validation and promotional discount rules** within the system.

The first part validates **input constraints for username and password fields during user registration**, ensuring that only values within the allowed ranges are accepted.

The second part verifies the **promotion system**, where discounts are applied based on the **number of years a user has been actively registered in the system**.

The objective of these tests is to ensure that the system correctly handles **valid and invalid equivalence classes** and applies the correct promotional rules.

---

# Business Rules

### User Registration

* The system allows user registration only if:

  * **Username length is between 6 and 30 valid characters**
  * **Password length is between 8 and 100 valid characters**

### Promotion System

Discounts are applied according to the **user's active registration time**:

| Active Registration Time | Discount     |
| ------------------------ | ------------ |
| Less than 5 years        | 10% discount |
| Between 5 and 10 years   | 20% discount |
| More than 10 years       | 50% discount |

The discount is applied to the **next two products purchased**.

---

# Equivalence Classes

## Username Field

| Class | Description                           | Type    |
| ----- | ------------------------------------- | ------- |
| EC1   | Username with less than 6 characters  | Invalid |
| EC2   | Username between 6 and 30 characters  | Valid   |
| EC3   | Username with more than 30 characters | Invalid |

## Password Field

| Class | Description                            | Type    |
| ----- | -------------------------------------- | ------- |
| EC4   | Password with less than 8 characters   | Invalid |
| EC5   | Password between 8 and 100 characters  | Valid   |
| EC6   | Password with more than 100 characters | Invalid |

## Promotion System

| Class | Description                                         | Type  |
| ----- | --------------------------------------------------- | ----- |
| EC7   | User with less than 5 years of active registration  | Valid |
| EC8   | User with 5 to 10 years of active registration      | Valid |
| EC9   | User with more than 10 years of active registration | Valid |

---

# Test Cases

---

## TC_EP_01

**Title:** Validate username with less than 6 valid characters  
**Type:** Functional - Equivalence Partitioning (Negative)  
**Module:** Registration  
**Priority:** High  
**ID:** EP-01  
**Precondition:**
User must be on the registration page with all other fields filled with valid values.

### Steps

1. Access website: https://accounts.google.com/lifecycle/steps/signup/username?TL=AHU8sQsvP3J5xkWIYArXuQNXyiodDh_kIXZ9-LHDw2SOoyPblilGhuK5eV1-kwbA&continue=https%3A%2F%2Fmyaccount.google.com%3Futm_source%3Daccount-marketing-page%26utm_medium%3Dcreate-account-button&dsh=S1275079143%3A1774029772256352&flowEntry=SignUp&flowName=GlifWebSignIn
2. Access the registration page
3. Fill all valid fields correctly
4. Enter a value with **3 valid characters** in the "Username" field
5. Click the **Next** button

### Test Data

Username: admin1234567890admin1234567890a  
Minimum allowed characters: 6  
Maximum allowed characters: 30

### Expected Result

The system must prevent the user from proceeding and display the error message:

"Your username must contain between 6 and 30 characters."

### Actual Result

The system prevented the action and displayed the correct error message.

### Status

Approved

---

## TC_EP_02

**Title:** Validate username with 10 valid characters  
**Type:** Functional - Equivalence Partitioning (Positive)  
**Module:** Registration  
**Priority:** High  
**ID:** EP-02  
**Precondition:**
User must be on the registration page with all other fields filled with valid values.

### Steps

1. Access website: https://accounts.google.com/lifecycle/steps/signup/username?TL=AHU8sQsvP3J5xkWIYArXuQNXyiodDh_kIXZ9-LHDw2SOoyPblilGhuK5eV1-kwbA&continue=https%3A%2F%2Fmyaccount.google.com%3Futm_source%3Daccount-marketing-page%26utm_medium%3Dcreate-account-button&dsh=S1275079143%3A1774029772256352&flowEntry=SignUp&flowName=GlifWebSignIn
2. Access the registration page
3. Fill all valid fields correctly
4. Enter a value with **10 valid characters** in the "Username" field
5. Click the **Next** button

### Test Data

Username: admin12345  
Minimum allowed characters: 6  
Maximum allowed characters: 30

### Expected Result

The system should allow the user to proceed without displaying an error message.

### Actual Result

The system allowed the user to proceed correctly.

### Status

Approved

---

## TC_EP_03

**Title:** Validate username with more than 30 valid characters  
**Type:** Functional - Equivalence Partitioning (Negative)  
**Module:** Registration  
**Priority:** High  
**ID:** EP-03  
**Precondition:**
User must be on the registration page with all other fields filled with valid values.

### Steps

1. Access website: https://accounts.google.com/lifecycle/steps/signup/username?TL=AHU8sQsvP3J5xkWIYArXuQNXyiodDh_kIXZ9-LHDw2SOoyPblilGhuK5eV1-kwbA&continue=https%3A%2F%2Fmyaccount.google.com%3Futm_source%3Daccount-marketing-page%26utm_medium%3Dcreate-account-button&dsh=S1275079143%3A1774029772256352&flowEntry=SignUp&flowName=GlifWebSignIn
2. Access the registration page
3. Fill all valid fields correctly
4. Enter a value with **35 valid characters** in the "Username" field
5. Click the **Next** button

### Test Data

Username: admin1234567890admin1234567890admin  
Minimum allowed characters: 6  
Maximum allowed characters: 30

### Expected Result

The system must prevent the user from proceeding and display the error message:

"Your username must contain between 6 and 30 characters."

### Actual Result

The system prevented the action and displayed the correct error message.

### Status

Approved

---

## TC_EP_04

**Title:** Validate password with less than 8 valid characters  
**Type:** Functional - Equivalence Partitioning (Negative)  
**Module:** Registration  
**Priority:** High  
**ID:** EP-04  
**Precondition:**
User must be on the registration page with all other fields filled with valid values.

### Steps

1. Access website: https://accounts.google.com/lifecycle/steps/signup/password?TL=AHU8sQsvP3J5xkWIYArXuQNXyiodDh_kIXZ9-LHDw2SOoyPblilGhuK5eV1-kwbA&continue=https%3A%2F%2Fmyaccount.google.com%3Futm_source%3Daccount-marketing-page%26utm_medium%3Dcreate-account-button&dsh=S1275079143%3A1774029772256352&flowEntry=SignUp&flowName=GlifWebSignIn
2. Access the registration page
3. Fill all valid fields correctly
4. Enter a value with **3 valid characters** in the "Password" field
5. Click the **Next** button

### Test Data

Password: pas  
Minimum allowed characters: 8
Maximum allowed characters: 100

### Expected Result

The system must prevent the user from proceeding and display the message:

"Your password must contain 8 or more characters."

### Actual Result

The system prevented the action and displayed the correct message.

### Status

Approved

---

## TC_EP_05

**Title:** Validate password with 50 valid characters  
**Type:** Functional - Equivalence Partitioning (Positive)  
**Module:** Registration  
**Priority:** High  
**ID:** EP-05  
**Precondition:**
User must be on the registration page with all other fields filled with valid values.

### Steps

1. Access website: https://accounts.google.com/lifecycle/steps/signup/password?TL=AHU8sQsvP3J5xkWIYArXuQNXyiodDh_kIXZ9-LHDw2SOoyPblilGhuK5eV1-kwbA&continue=https%3A%2F%2Fmyaccount.google.com%3Futm_source%3Daccount-marketing-page%26utm_medium%3Dcreate-account-button&dsh=S1275079143%3A1774029772256352&flowEntry=SignUp&flowName=GlifWebSignIn
2. Access the registration page
3. Fill all valid fields correctly
4. Enter a value with **50 valid characters** in the "Password" field
5. Click the **Next** button

### Test Data

Password: passwordpasswordpasswordpasswordpasswordpasswordpa  
Minimum allowed characters: 8  
Maximum allowed characters: 100

### Expected Result

The system should allow the user to proceed without displaying an error message.

### Actual Result

The system allowed the action without displaying any error message.

### Status

Approved

---

## TC_EP_06

**Title:** Validate password with more than 100 valid characters  
**Type:** Functional - Equivalence Partitioning (Negative)  
**Module:** Registration  
**Priority:** High  
**ID:** EP-06  
**Precondition:**
User must be on the registration page with all other fields filled with valid values.

### Steps

1. Access website: https://accounts.google.com/lifecycle/steps/signup/password?TL=AHU8sQsvP3J5xkWIYArXuQNXyiodDh_kIXZ9-LHDw2SOoyPblilGhuK5eV1-kwbA&continue=https%3A%2F%2Fmyaccount.google.com%3Futm_source%3Daccount-marketing-page%26utm_medium%3Dcreate-account-button&dsh=S1275079143%3A1774029772256352&flowEntry=SignUp&flowName=GlifWebSignIn
2. Access the registration page
3. Fill all valid fields correctly
4. Enter a value with **180 valid characters** in the "Password" field
5. Click the **Next** button

### Test Data

Password: passwordpasswordpasswordpasswordpasswordpasswordpapasswordpasswordpasswordpasswordpasswordpasswordpapasswordpasswordpasswordpasswordpasswordpasswordpapasswordpasswordpasswordpasswo  
Minimum allowed characters: 8  
Maximum allowed characters: 100

### Expected Result

The system must prevent the user from proceeding and display the message:

"Your password must contain 100 or fewer characters."

### Actual Result

The system prevented the action and displayed the correct message.

### Status

Approved

---

## TC_EP_07

**Title:** Validate user with less than 5 years of active registration
**Type:** Functional - Equivalence Partitioning (Positive)
**Module:** Promotion System
**Priority:** High
**ID:** EP-07
**Precondition:**
User registered in the system with **2 years of active registration**.

### Steps

1. Log in to the system
2. Access the product page
3. Select two products and add them to the cart
4. Proceed to checkout

### Test Data

Registration time: 2 years

### Expected Result

The system must apply a **10% discount** to the two selected products.

### Actual Result

The system correctly applied the 10% discount to both products.

### Status

Approved

---

## TC_EP_08

**Title:** Validate user between 5 and 10 years of active registration
**Type:** Functional - Equivalence Partitioning (Positive)
**Module:** Promotion System
**Priority:** High
**ID:** EP-08
**Precondition:**
User registered in the system with **7 years of active registration**.

### Steps

1. Log in to the system
2. Access the product page
3. Select two products and add them to the cart
4. Proceed to checkout

### Test Data

Registration time: 7 years

### Expected Result

The system must apply a **20% discount** to the two selected products.

### Actual Result

The system correctly applied the 20% discount to both products.

### Status

Approved

---

## TC_EP_09

**Title:** Validate user with more than 10 years of active registration
**Type:** Functional - Equivalence Partitioning (Positive)
**Module:** Promotion System
**Priority:** High
**ID:** EP-09
**Precondition:**
User registered in the system with **15 years of active registration**.

### Steps

1. Log in to the system
2. Access the product page
3. Select two products and add them to the cart
4. Proceed to checkout

### Test Data

Registration time: 15 years

### Expected Result

The system must apply a **50% discount** to the two selected products.

### Actual Result

The system correctly applied the 50% discount to both products.

### Status

Approved
