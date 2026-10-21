# SauceDemo — Login Test Cases

## Project Information

- **Application:** SauceDemo
- **Module:** Login
- **Testing Type:** Manual, Functional
- **Test Environment:** Web browser
- **Tester:** Anoosh Salman

## TC-01: Login with Valid Credentials

| Field | Details |
|---|---|
| Test Case ID | TC-01 |
| Scenario | Verify login with valid credentials |
| Preconditions | User is on the login page |
| Test Data | Valid username and password provided by the application |
| Steps | 1. Enter a valid username. 2. Enter the provided password. 3. Click Login. |
| Expected Result | User logs in successfully and reaches the Products page. |
| Actual Result | The Products page opened successfully. |
| Status | PASS |

## TC-02: Login with an Incorrect Password

| Field | Details |
|---|---|
| Test Case ID | TC-02 |
| Scenario | Verify login with an incorrect password |
| Preconditions | User is on the login page |
| Test Data | Username: `standard_user`; Password: `WrongPass123` |
| Steps | 1. Enter the username. 2. Enter an incorrect password. 3. Click Login. |
| Expected Result | Login is rejected and an appropriate error message is displayed. |
| Actual Result | The application displayed: "Username and password do not match any user in this service." |
| Status | PASS |

## TC-03: Login with Both Fields Empty

| Field | Details |
|---|---|
| Test Case ID | TC-03 |
| Scenario | Verify login with both username and password fields empty |
| Preconditions | User is on the login page |
| Test Data | Username: Empty; Password: Empty |
| Steps | 1. Leave the username field empty. 2. Leave the password field empty. 3. Click Login. |
| Expected Result | Login is prevented, and a validation message indicates that the username is required. |
| Actual Result | The application displayed "Username is required." |
| Status | PASS |

## TC-04: Login with Username Only

| Field | Details |
|---|---|
| Test Case ID | TC-04 |
| Scenario | Verify login when the username is provided but the password is empty |
| Preconditions | User is on the login page |
| Test Data | Username: `standard_user`; Password: Empty |
| Steps | 1. Enter `standard_user` as the username. 2. Leave the password field empty. 3. Click Login. |
| Expected Result | Login is prevented, and a validation message indicates that the password is required. |
| Actual Result | The application displayed "Password is required." |
| Status | PASS |

## TC-05: Login with Password Only

| Field | Details |
|---|---|
| Test Case ID | TC-05 |
| Scenario | Verify login when the password is provided but the username is empty |
| Preconditions | User is on the login page |
| Test Data | Username: Empty; Password: Valid shared password displayed on the application |
| Steps | 1. Leave the username field empty. 2. Enter the valid shared password. 3. Click Login. |
| Expected Result | Login is prevented, and a validation message indicates that the username is required. |
| Actual Result | The application displayed "Epic sadface: Username is required". |
| Status | PASS |

## TC-06: Login with an Invalid Username

| Field | Details |
|---|---|
| Test Case ID | TC-06 |
| Scenario | Verify login with an invalid username |
| Preconditions | User is on the login page |
| Test Data | Username: `invalid_user_123`; Password: valid shared password |
| Steps | 1. Enter an invalid username. 2. Enter the valid shared password. 3. Click Login. |
| Expected Result | Login is rejected and an appropriate error message is displayed. |
| Actual Result | The application displayed: "Epic sadface: Username and password do not match any user in this service." |
| Status | PASS |

## TC-07: Login with a Leading Space in the Username

| Field | Details |
|---|---|
| Test Case ID | TC-07 |
| Scenario | Verify login behavior when the username contains a leading space |
| Preconditions | User is on the login page |
| Test Data | Username: ` standard_user` (leading space); Password: valid shared password |
| Steps | 1. Enter the username with a leading space. 2. Enter the valid shared password. 3. Click Login. |
| Expected Result | Login is rejected if the application treats the username with a leading space as invalid. |
| Actual Result | The application displayed: "Epic sadface: Username and password do not match any user in this service." |
| Status | PASS |

## TC-08: Logout Successfully

| Field | Details |
|---|---|
| Test Case ID | TC-08 |
| Scenario | Verify that a logged-in user can log out |
| Preconditions | User is logged in and on the Products page |
| Test Data | Valid user session |
| Steps | 1. Open the menu. 2. Click Logout. |
| Expected Result | The user is logged out and returned to the login page. |
| Actual Result | The application returned to the login page. |
| Status | PASS |

## TC-09: Use Browser Back After Logout

| Field | Details |
|---|---|
| Test Case ID | TC-09 |
| Scenario | Verify that a logged-out user cannot access the protected Products page using the browser Back button |
| Preconditions | User has logged in and then logged out |
| Test Data | Existing browser session after logout |
| Steps | 1. Log in successfully. 2. Click Logout. 3. Click the browser Back button. |
| Expected Result | The application should prevent access to the protected page while the user is logged out. |
| Actual Result | The application displayed: "Epic sadface: You can only access '/inventory.html' when you are logged in." |
| Status | PASS |

## TC-10: Verify Error Message for Invalid Credentials

| Field | Details |
|---|---|
| Test Case ID | TC-10 |
| Scenario | Verify the error message displayed when both username and password are invalid |
| Preconditions | User is on the login page |
| Test Data | Username: `invalid_user_123`; Password: `WrongPass123` |
| Steps | 1. Enter an invalid username. 2. Enter an invalid password. 3. Click Login. 4. Verify the error message. |
| Expected Result | Login is rejected and a clear error message is displayed. |
| Actual Result | The application displayed: "Epic sadface: Username and password do not match any user in this service." |
| Status | PASS |

## Updated Test Summary

- Total test cases executed: 10
- Passed: 10
- Failed: 0

*These results reflect personal practice testing on the public SauceDemo demo application, not professional QA employment.*

