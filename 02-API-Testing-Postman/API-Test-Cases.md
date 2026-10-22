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

---

## API-TC-02: Verify GET Request for All Posts

| Field | Details |
|---|---|
| Test Case ID | API-TC-02 |
| Scenario | Verify that the API returns a list of all posts |
| HTTP Method | GET |
| Endpoint | `https://jsonplaceholder.typicode.com/posts` |
| Preconditions | API endpoint is accessible |
| Test Steps | 1. Open Postman. 2. Select GET. 3. Enter the endpoint. 4. Click Send. 5. Verify the response status, structure, and number of posts. |
| Expected Result | The API returns HTTP status `200 OK` and a JSON array containing 100 posts. Each post contains the fields `userId`, `id`, `title`, and `body`. |
| Actual Result | The API returned `200 OK`. The response contained a JSON array of 100 posts with the expected fields. |
| Status | PASS |

---

## API-TC-03: Verify GET Request for a Non-Existing Post

| Field | Details |
|---|---|
| Test Case ID | API-TC-03 |
| Scenario | Verify the API response when requesting a post that does not exist |
| HTTP Method | GET |
| Endpoint | `https://jsonplaceholder.typicode.com/posts/9999` |
| Preconditions | API endpoint is accessible |
| Test Steps | 1. Open Postman. 2. Select GET. 3. Enter the endpoint. 4. Click Send. 5. Verify the response status and body. |
| Expected Result | The API returns HTTP status `404 Not Found` with an empty response body because the requested post does not exist. |
| Actual Result | The API returned `404 Not Found` with an empty response body. |
| Status | PASS |

---

## API-TC-04: Verify POST Request for Creating a New Post

| Field | Details |
|---|---|
| Test Case ID | API-TC-04 |
| Scenario | Verify that the API accepts a request to create a new post |
| HTTP Method | POST |
| Endpoint | `https://jsonplaceholder.typicode.com/posts` |
| Preconditions | API endpoint is accessible |
| Test Steps | 1. Open Postman. 2. Select POST. 3. Enter the endpoint. 4. Select Body, then raw, then JSON. 5. Enter the request body. 6. Click Send. 7. Verify the status code and response data. |
| Request Body | `{ "title": "QA Portfolio API Test", "body": "Testing POST request using Postman", "userId": 1 }` |
| Expected Result | The API returns HTTP status `201 Created`. The response contains the submitted title, body, and userId, along with a generated post ID. |
| Actual Result | The API returned `201 Created`. The response contained the submitted data. |
| Status | PASS |

---

## Test Summary

| Metric | Result |
|---|---|
| Total Test Cases Executed | 4 |
| Passed | 4 |
| Failed | 0 |

**Note:** These tests were performed as part of a personal API testing practice portfolio using the public JSONPlaceholder API and Postman. JSONPlaceholder simulates write operations; created data is not permanently persisted.
