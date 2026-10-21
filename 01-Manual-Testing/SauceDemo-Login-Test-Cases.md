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

## Test Summary

- Total test cases executed: 2
- Passed: 2
- Failed: 0

*These results reflect personal practice testing on the public SauceDemo demo application, not professional QA employment.*
