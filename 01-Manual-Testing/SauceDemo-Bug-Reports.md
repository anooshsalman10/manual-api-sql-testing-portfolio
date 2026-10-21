# SauceDemo Bug Reports

## Project Information

| Field | Details |
|---|---|
| Application | SauceDemo |
| Module | Checkout |
| Testing Type | Manual Functional Testing |
| Test Environment | Web browser |
| Report Type | Defect / Bug Report |
| Tester | Anoosh Salman |

---

## BUG-01: User Can Complete Checkout with an Empty Cart

| Field | Details |
|---|---|
| Bug ID | BUG-01 |
| Bug Title | User can complete checkout with an empty cart |
| Module | Checkout |
| Severity | Medium (provisional) |
| Priority | Medium (provisional) |
| Status | Reproduced |
| Test Type | Negative Testing |
| Related Test Case | TC-30 |

### Preconditions

1. The user is logged in to SauceDemo.
2. The shopping cart is empty.

### Steps to Reproduce

1. Open the shopping cart.
2. Click the Checkout button.
3. Enter valid information in the First Name, Last Name, and ZIP/Postal Code fields.
4. Click Continue.
5. Verify that the Checkout: Overview page opens.
6. Confirm that no products are listed and the item total and final total are both $0.00.
7. Click Finish.

### Expected Result

The application should prevent the user from completing checkout when the shopping cart contains no products. An appropriate message should be displayed, or the user should be prevented from proceeding.

### Actual Result

The application allows the user to proceed to the Checkout: Overview page with an empty cart and a total of $0.00. After clicking Finish, the application displays the following confirmation:

**Heading:** Thank you for your order!

**Message:** Your order has been dispatched, and will arrive just as fast as the pony can get there!

### Reproducibility

The issue was reproduced successfully twice during manual testing.

### Impact

A user can receive an order confirmation despite having no products in the cart. This may cause confusion about whether a valid order was placed and indicates that the checkout flow does not adequately prevent empty-cart order completion.

### Suggested Fix

Validate that the shopping cart contains at least one product before allowing the user to proceed with checkout or complete an order.

### Evidence

Observed during manual testing on the public SauceDemo demo application. The empty cart, $0.00 total, and successful order confirmation were verified.

---

## Note

This bug report documents a reproducible issue found during personal QA practice on the public SauceDemo demo application. It is a learning and portfolio exercise, not a report from professional QA employment.
