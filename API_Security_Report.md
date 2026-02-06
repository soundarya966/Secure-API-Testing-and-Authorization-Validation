# API Security Testing Report

## Objective
To test REST API endpoints for authentication, authorization,
input validation, and rate limiting weaknesses.

---

## Target API
https://jsonplaceholder.typicode.com

---

## Tools Used
- Postman
- cURL

---

## HTTP Methods Tested
GET
POST
PUT
DELETE

---

## Test Case 1 — Authentication Testing

### Description
Requests were sent without authentication headers.

### Result
API allowed access without authentication.

### Risk
Broken Authentication (OWASP API2)

---

## Test Case 2 — Authorization Testing (IDOR)

### Description
Resource IDs were modified in requests.

Example:
GET /posts/1
GET /posts/2
GET /posts/10

### Result
API allowed access to all resources.

### Risk
Broken Object Level Authorization (OWASP API1)

---

## Test Case 3 — Input Validation Testing

### Description
Malformed JSON data was sent.

Example:
{
"title": 12345,
"body": null
}

### Result
API accepted invalid input.

### Risk
Improper Input Validation (OWASP API8)

---

## Test Case 4 — Rate Limiting Testing

### Description
Multiple rapid requests were sent using cURL loop.

### Result
No rate limiting observed.

### Risk
Lack of Resource & Rate Limiting (OWASP API4)

---

## HTTP Response Review

Observed Status Codes:
- 200 OK
- 201 Created

Error messages did not reveal sensitive data.

---

## Conclusion
The API testing exercise demonstrated how APIs can be tested for common
security weaknesses including authentication failures, authorization issues,
input validation problems, and missing rate limiting controls.

This task improved understanding of API security testing methodology.
