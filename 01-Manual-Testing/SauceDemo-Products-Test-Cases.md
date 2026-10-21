# SauceDemo — Products Test Cases

## Project Information

- **Application:** SauceDemo
- **Module:** Products / Inventory
- **Testing Type:** Manual, Functional
- **Test Environment:** Web browser
- **Tester:** Anoosh Salman

## TC-11: Verify Products Page After Login

| Field | Details |
|---|---|
| Test Case ID | TC-11 |
| Scenario | Verify that the Products page opens after successful login |
| Preconditions | User is on the login page |
| Test Data | Valid demo username and password |
| Steps | 1. Enter valid credentials. 2. Click Login. 3. Verify the Products page. |
| Expected Result | The Products page opens successfully, displaying product names, prices, and images. |
| Actual Result | The Products page opened successfully, and product names, prices, and images were visible. |
| Status | PASS |

## TC-12: Verify Product Names Are Displayed

| Field | Details |
|---|---|
| Test Case ID | TC-12 |
| Scenario | Verify that product names are displayed |
| Preconditions | User is logged in and on the Products page |
| Test Data | Products listed on the Products page |
| Steps | 1. Inspect the listed products. 2. Check that each product has a visible name. |
| Expected Result | Every listed product has a visible product name. |
| Actual Result | All product names were visible; no missing or blank names were observed. |
| Status | PASS |

## TC-13: Verify Product Prices Are Displayed

| Field | Details |
|---|---|
| Test Case ID | TC-13 |
| Scenario | Verify that product prices are displayed |
| Preconditions | User is logged in and on the Products page |
| Test Data | Prices of listed products |
| Steps | 1. Inspect the listed products. 2. Check that each product has a visible price. |
| Expected Result | Every listed product has a visible price. |
| Actual Result | All product prices were visible; no missing prices were observed. |
| Status | PASS |

## TC-14: Verify Product Images Are Displayed

| Field | Details |
|---|---|
| Test Case ID | TC-14 |
| Scenario | Verify that product images are displayed |
| Preconditions | User is logged in and on the Products page |
| Test Data | Images of listed products |
| Steps | 1. Inspect the listed products. 2. Check that each product image is visible. |
| Expected Result | Every listed product displays its product image without missing images. |
| Actual Result | All product images were visible; no missing images were observed. |
| Status | PASS |

## TC-15: Verify Products Can Be Sorted by Name (A to Z)

| Field | Details |
|---|---|
| Test Case ID | TC-15 |
| Scenario | Verify that products can be sorted alphabetically from A to Z |
| Preconditions | User is logged in and on the Products page |
| Test Data | Product names |
| Steps | 1. Open the sorting dropdown. 2. Select Name (A to Z). 3. Check the order of the products. |
| Expected Result | Products are displayed in alphabetical order from A to Z. |
| Actual Result | Products appeared in alphabetical order after selecting Name (A to Z). |
| Status | PASS |

## TC-16: Verify Products Can Be Sorted by Price (Low to High)

| Field | Details |
|---|---|
| Test Case ID | TC-16 |
| Scenario | Verify that products can be sorted by price in ascending order |
| Preconditions | User is logged in and on the Products page |
| Test Data | Prices of listed products |
| Steps | 1. Open the sorting dropdown. 2. Select Price (low to high). 3. Check the order of the product prices. |
| Expected Result | Products are displayed in ascending price order, from lowest to highest. |
| Actual Result | Products appeared in ascending price order after selecting Price (low to high). |
| Status | PASS |


## TC-17: Verify a Product Can Be Added to the Cart

| Field | Details |
|---|---|
| Test Case ID | TC-17 |
| Scenario | Verify that a user can add a product to the cart |
| Preconditions | User is logged in and on the Products page |
| Test Data | Product: Sauce Labs Backpack |
| Steps | 1. Locate Sauce Labs Backpack. 2. Click Add to cart. 3. Check the product button. |
| Expected Result | The product is added to the cart, and its button changes to Remove. |
| Actual Result | The button changed to Remove after adding the product. The product could also be removed. |
| Status | PASS |

## TC-18: Verify the Cart Badge Updates After Adding a Product

| Field | Details |
|---|---|
| Test Case ID | TC-18 |
| Scenario | Verify that the cart badge displays the correct item count |
| Preconditions | User is logged in and the cart is empty |
| Test Data | Product: Sauce Labs Backpack |
| Steps | 1. Add Sauce Labs Backpack to the cart. 2. Observe the cart badge. |
| Expected Result | The cart badge displays 1 after one product is added. |
| Actual Result | The cart badge updated to display the item count after adding the product. |
| Status | PASS |

## TC-19: Verify the Correct Product Appears in the Cart

| Field | Details |
|---|---|
| Test Case ID | TC-19 |
| Scenario | Verify that the selected product appears correctly in the cart |
| Preconditions | User is logged in and a product has been added to the cart |
| Test Data | Product: Sauce Labs Backpack |
| Steps | 1. Add Sauce Labs Backpack to the cart. 2. Open the cart. 3. Verify the product name, price, and quantity. |
| Expected Result | The cart displays Sauce Labs Backpack with its correct price and quantity of 1. |
| Actual Result | The product name, price, and quantity were displayed in the cart. |
| Status | PASS |

## TC-20: Verify a Product Can Be Removed from the Products Page

| Field | Details |
|---|---|
| Test Case ID | TC-20 |
| Scenario | Verify that a user can remove a product from the cart |
| Preconditions | User is logged in and Sauce Labs Backpack has been added to the cart |
| Test Data | Product: Sauce Labs Backpack |
| Steps | 1. Open the cart. 2. Remove the product. 3. Click Continue Shopping. 4. Check the product button on the Products page. |
| Expected Result | The product is removed from the cart, the cart badge updates, and the product button returns to Add to cart. |
| Actual Result | The cart badge disappeared after removal, and the product button displayed Add to cart after returning to the Products page. |
| Status | PASS |

## TC-21: Verify the Cart Is Empty After Removing All Products

| Field | Details |
|---|---|
| Test Case ID | TC-21 |
| Scenario | Verify that the cart displays no products after all products are removed |
| Preconditions | User is logged in and all products have been removed from the cart |
| Test Data | Empty shopping cart |
| Steps | 1. Remove all products from the cart. 2. Open the cart. 3. Check the cart contents and badge. |
| Expected Result | No products are listed in the cart, and the cart badge does not display an item count. |
| Actual Result | The cart was empty after the products were removed. |
| Status | PASS |

## Test Summary

- **Total test cases executed:** 11
- **Passed:** 11
- **Failed:** 0

*These results reflect personal practice testing on the public SauceDemo demo application, not professional QA employment.*




