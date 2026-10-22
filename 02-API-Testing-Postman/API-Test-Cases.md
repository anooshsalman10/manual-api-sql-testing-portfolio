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
| Expected Result | The API returns HTTP status `200 OK` and a JSON array containing 100 posts. Each post contains `userId`, `id`, `title`, and `body`. |
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

## API-TC-05: Verify PUT Request for Updating an Existing Post

| Field | Details |
|---|---|
| Test Case ID | API-TC-05 |
| Scenario | Verify that the API accepts a request to update an existing post |
| HTTP Method | PUT |
| Endpoint | `https://jsonplaceholder.typicode.com/posts/1` |
| Preconditions | API endpoint is accessible |
| Test Steps | 1. Open Postman. 2. Select PUT. 3. Enter the endpoint. 4. Select Body, then raw, then JSON. 5. Enter the updated post data. 6. Click Send. 7. Verify the response status and fields. |
| Request Body | `{ "id": 1, "title": "Updated QA Portfolio Test", "body": "Testing PUT request using Postman", "userId": 1 }` |
| Expected Result | The API returns HTTP status `200 OK` and a response containing the submitted id, title, body, and userId. |
| Actual Result | The API returned `200 OK`. The response contained `id: 1`, the title `Updated QA Portfolio Test`, the body `Testing PUT request using Postman`, and `userId: 1`. |
| Status | PASS |

---

## API-TC-06: Verify PATCH Request for Updating Part of a Post

| Field | Details |
|---|---|
| Test Case ID | API-TC-06 |
| Scenario | Verify that the API accepts a request to update a specific field of an existing post |
| HTTP Method | PATCH |
| Endpoint | `https://jsonplaceholder.typicode.com/posts/1` |
| Preconditions | API endpoint is accessible |
| Test Steps | 1. Open Postman. 2. Select PATCH. 3. Enter the endpoint. 4. Select Body, then raw, then JSON. 5. Submit only the title field. 6. Click Send. 7. Verify the status code and response data. |
| Request Body | `{ "title": "PATCH Updated QA Title" }` |
| Expected Result | The API returns HTTP status `200 OK` and a response containing the updated title and the existing post's other fields. |
| Actual Result | The API returned `200 OK`. The response contained `id: 1`, the updated title `PATCH Updated QA Title`, `userId: 1`, and the post body. |
| Status | PASS |

---

## API-TC-07: Verify DELETE Request for an Existing Post

| Field | Details |
|---|---|
| Test Case ID | API-TC-07 |
| Scenario | Verify that the API accepts a request to delete an existing post |
| HTTP Method | DELETE |
| Endpoint | `https://jsonplaceholder.typicode.com/posts/1` |
| Preconditions | API endpoint is accessible |
| Test Steps | 1. Open Postman. 2. Select DELETE. 3. Enter the endpoint. 4. Leave the request body empty. 5. Click Send. 6. Verify the response status and body. |
| Expected Result | The API returns HTTP status `200 OK` and an empty JSON object `{}`. |
| Actual Result | The API returned `200 OK`. The response body was `{}`. |
| Status | PASS |

---

## API-TC-08: Verify GET Request With a Query That Matches No Records

| Field | Details |
|---|---|
| Test Case ID | API-TC-08 |
| Scenario | Verify the API response when a valid query parameter matches no posts |
| HTTP Method | GET |
| Endpoint | `https://jsonplaceholder.typicode.com/posts?userId=999` |
| Preconditions | API endpoint is accessible |
| Test Steps | 1. Open Postman. 2. Select GET. 3. Enter the endpoint with the query parameter. 4. Click Send. 5. Verify the response status and body. |
| Expected Result | The API returns HTTP status `200 OK` with an empty JSON array `[]` because no posts match the specified userId. |
| Actual Result | The API returned `200 OK`. The response body was an empty JSON array `[]`. |
| Status | PASS |

---

## API-TC-09: Verify Response Headers and JSON Content Type

| Field | Details |
|---|---|
| Test Case ID | API-TC-09 |
| Scenario | Verify that the API response includes the expected JSON content type |
| HTTP Method | GET |
| Endpoint | `https://jsonplaceholder.typicode.com/posts/1` |
| Preconditions | API endpoint is accessible |
| Test Steps | 1. Open Postman. 2. Select GET. 3. Enter the endpoint. 4. Click Send. 5. Open the response Headers tab. 6. Verify the Content-Type header. |
| Expected Result | The API returns HTTP status `200 OK` and a Content-Type header indicating JSON, such as `application/json; charset=utf-8`. |
| Actual Result | The API returned `200 OK`. The Content-Type header was `application/json; charset=utf-8`. |
| Status | PASS |

---

## API-TC-10: Verify API Response Time

| Field | Details |
|---|---|
| Test Case ID | API-TC-10 |
| Scenario | Verify that the API responds within the defined response-time threshold |
| HTTP Method | GET |
| Endpoint | `https://jsonplaceholder.typicode.com/posts/1` |
| Preconditions | API endpoint is accessible |
| Test Steps | 1. Open Postman. 2. Select GET. 3. Enter the endpoint. 4. Click Send. 5. Record the response time displayed by Postman. |
| Expected Result | The API returns HTTP status `200 OK` and responds in less than 2,000 milliseconds. |
| Actual Result | The API returned `200 OK`. Postman displayed a response time of 45 milliseconds. |
| Status | PASS |

---

## Test Summary

| Metric | Result |
|---|---|
| Total Test Cases Executed | 10 |
| Passed | 10 |
| Failed | 0 |

## Notes

- These tests were performed as part of a personal API testing practice portfolio using the public JSONPlaceholder API and Postman.
- JSONPlaceholder simulates write operations. POST, PUT, PATCH, and DELETE responses do not mean that changes are permanently saved to the server.
- The response time recorded in API-TC-10 reflects one request during this test session. Response times can vary depending on network conditions and server load.
- The 2,000-millisecond response-time threshold is the criterion selected for this practice test.
