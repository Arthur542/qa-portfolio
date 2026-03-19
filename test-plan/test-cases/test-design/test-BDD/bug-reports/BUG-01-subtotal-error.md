# Bug Report: Subtotal Calculation Error

## Module Summary

This module validates the correctness of **price calculations during the checkout process**, ensuring that the subtotal accurately reflects the sum of selected products.

The validation focuses on detecting inconsistencies in financial calculations that may impact user trust and transaction accuracy.

---

## Business Rule

* The system must correctly calculate the **subtotal** based on the sum of all selected products
* The displayed subtotal must match the actual total value of items in the cart
* Any discrepancy in calculation must be prevented to ensure transactional integrity

---

## Bug Details

* **ID:** BUG-01
* **Title:** System calculates incorrect subtotal during checkout
* **Type:** Calculation Error
* **Module:** Checkout
* **Priority:** High
* **Severity:** High
* **Status:** Open

---

## Environment

* **Browser:** Google Chrome
* **Operating System:** Windows 11
* **Environment:** Test

---

## Precondition

* User is authenticated
* At least one product is added to the cart

---

## Steps to Reproduce

1. Access the website: https://demo.opencart.com;
2. Log in with valid credentials
3. Navigate to the products page
4. Select the product **"MacBook"**
5. Add the product to the cart
6. Open the cart
7. Proceed to checkout
8. Observe the subtotal value displayed

---

## Test Data

* Product: MacBook
* Product Price: $602.00

---

## Expected Result

The system must correctly calculate and display the subtotal based on the selected product(s).

---

## Actual Result

* Product price: $602.00
* Displayed subtotal: $500.00
* Observed difference: $102.00

---

## Impact

* Financial inconsistency in checkout process
* Potential loss of user trust
* Risk of incorrect transaction values

---
