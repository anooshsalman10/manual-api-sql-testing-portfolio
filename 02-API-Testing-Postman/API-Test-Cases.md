# API Testing Portfolio — Postman

## Project Information

| Field | Details |
|---|---|
| API | JSONPlaceholder |
| Tool | Postman |
| Testing Type | API Functional Testing |
| Tester | Anoosh Salman |

---

## API-TC-01: Verify GET Request for an Existing Post

| Field | Details |
|---|---|
| Test Case ID | API-TC-01 |
| Scenario | Verify that the API returns an existing post successfully |
| HTTP Method | GET |
| Endpoint | `https://jsonplaceholder.typicode.com/posts/1` |
| Preconditions | API endpoint is accessible |
| Test Steps | 1. Open Postman. 2. Select GET. 3. Enter the endpoint. 4. Click Send. |
| Expected Result | The API returns HTTP status `200 OK` and a response containing the requested post with valid fields. |
| Actual Result | The API returned `200 OK`. The response contained post data, including `id: 1`. |
| Status | PASS |


