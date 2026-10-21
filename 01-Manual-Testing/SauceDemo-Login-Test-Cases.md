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
## Test Summary

- Total test cases executed: 5
- Passed: 5
- Failed: 0

*These results reflect personal practice testing on the public SauceDemo demo application, not professional QA employment.*
