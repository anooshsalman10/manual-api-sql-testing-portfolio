# SauceDemo Checkout Test Cases

## Project Information

| Field | Details |
|---|---|
| Application | SauceDemo |
| Module | Checkout |
| Testing Type | Manual Functional Testing |
| Test Environment | Web browser |
| Tester | Anoosh Salman |

---

## TC-22: Verify Checkout Can Be Started from Cart

| Field | Details |
|---|---|
| Test Case ID | TC-22 |
| Scenario | Verify that the user can start checkout from the shopping cart |
| Preconditions | User is logged in and has added a product to the cart |
| Test Steps | 1. Open the shopping cart. 2. Click Checkout. |
| Expected Result | The Checkout: Your Information page opens with First Name, Last Name, ZIP/Postal Code fields, and Continue and Cancel buttons. |
| Actual Result | The Checkout: Your Information page opened with the expected fields and buttons. |
| Status | PASS |

## TC-23: Verify Required Validation When All Fields Are Empty

| Field | Details |
|---|---|
| Test Case ID | TC-23 |
| Scenario | Verify validation when all customer information fields are empty |
| Preconditions | User is on the Checkout: Your Information page |
| Test Steps | 1. Leave First Name, Last Name, and ZIP/Postal Code empty. 2. Click Continue. |
| Expected Result | The form displays an error requiring the First Name field. |
| Actual Result | The error message displayed: `Error: First Name is required` |
| Status | PASS |

## TC-24: Verify Required Validation When Last Name Is Missing

| Field | Details |
|---|---|
| Test Case ID | TC-24 |
| Scenario | Verify validation when the Last Name field is empty |
| Preconditions | User is on the Checkout: Your Information page |
| Test Steps | 1. Enter a first name. 2. Leave Last Name empty. 3. Enter ZIP/Postal Code. 4. Click Continue. |
| Expected Result | The form displays an error requiring the Last Name field. |
| Actual Result | The error message displayed: `Error: Last Name is required` |
| Status | PASS |

## TC-25: Verify Required Validation When Postal Code Is Missing

| Field | Details |
|---|---|
| Test Case ID | TC-25 |
| Scenario | Verify validation when the ZIP/Postal Code field is empty |
| Preconditions | User is on the Checkout: Your Information page |
| Test Steps | 1. Enter First Name and Last Name. 2. Leave ZIP/Postal Code empty. 3. Click Continue. |
| Expected Result | The form displays an error requiring the Postal Code field. |
| Actual Result | The error message displayed: `Error: Postal Code is required` |
| Status | PASS |

## TC-26: Verify Checkout with Valid Customer Information

| Field | Details |
|---|---|
| Test Case ID | TC-26 |
| Scenario | Verify that valid customer information allows the user to proceed |
| Preconditions | User is on the Checkout: Your Information page |
| Test Steps | 1. Enter valid first name, last name, and postal code. 2. Click Continue. |
| Expected Result | The Checkout: Overview page opens. |
| Actual Result | The Checkout: Overview page opened successfully after valid information was entered. |
| Status | PASS |

## TC-27: Verify Order Details and Price Calculation

| Field | Details |
|---|---|
| Test Case ID | TC-27 |
| Scenario | Verify product details and checkout price calculations |
| Preconditions | User is on the Checkout: Overview page |
| Test Steps | 1. Review the product name and quantity. 2. Check the item total, tax, and final total. |
| Expected Result | The product details and price calculations match the displayed values. |
| Actual Result | Sauce Labs Backpack was displayed with quantity 1 and price $29.99. Item total was $29.99, tax was $2.40, and final total was $32.39. The calculation was correct: $29.99 + $2.40 = $32.39. |
| Status | PASS |

## TC-28: Verify Order Can Be Completed Successfully

| Field | Details |
|---|---|
| Test Case ID | TC-28 |
| Scenario | Verify that the user can successfully complete an order |
| Preconditions | User is on the Checkout: Overview page with valid order details |
| Test Steps | 1. Click Finish. 2. Observe the resulting page. |
| Expected Result | The order completes successfully and a confirmation page appears. |
| Actual Result | The order completed successfully, and the confirmation page appeared. |
| Status | PASS |

## TC-29: Verify Order Confirmation and Return to Products

| Field | Details |
|---|---|
| Test Case ID | TC-29 |
| Scenario | Verify the order confirmation message and return navigation |
| Preconditions | The order has been completed successfully |
| Test Steps | 1. Verify the confirmation heading and message. 2. Click Back Home. 3. Observe the resulting page. |
| Expected Result | A successful order confirmation appears, and clicking Back Home returns the user to the Products page. |
| Actual Result | The page displayed `Thank you for your order!` and the message `Your order has been dispatched, and will arrive just as fast as the pony can get there!` Clicking Back Home returned to the Products page. |
| Status | PASS |


## TC-30: Verify Checkout with an Empty Cart

| Field | Details |
|---|---|
| Test Case ID | TC-30 |
| Scenario | Verify that a user cannot complete checkout with an empty cart |
| Preconditions | User is logged in and the shopping cart is empty |
| Test Steps | 1. Open the empty cart. 2. Click Checkout. 3. Enter valid first name, last name, and postal code. 4. Click Continue. 5. Verify the overview page shows no products and a $0.00 total. 6. Click Finish. |
| Expected Result | The application should prevent the user from completing an order when the cart contains no products. |
| Actual Result | The Checkout: Overview page displayed no products, an item total of $0, and a final total of $0.00. After clicking Finish, the application displayed the order confirmation message: "Thank you for your order!" |
| Status | FAIL |
| Related Bug ID | BUG-01 |
| Notes | The behavior was reproduced twice during manual testing. See SauceDemo-Bug-Reports.md for the detailed bug report. |



---

## Test Summary

| Metric | Result |
|---|---|
| Total Test Cases | 9 |
| Executed | 9 |
| Passed | 8 |
| Failed | 1 |
| Blocked | 0 |

## Note

These test cases were executed as personal practice on the public SauceDemo demo application for learning and portfolio purposes. They do not represent professional QA employment experience.
