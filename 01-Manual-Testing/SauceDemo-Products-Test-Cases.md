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

## Test Summary

- **Total test cases executed:** 6
- **Passed:** 6
- **Failed:** 0

*These results reflect personal practice testing on the public SauceDemo demo application, not professional QA employment.*

