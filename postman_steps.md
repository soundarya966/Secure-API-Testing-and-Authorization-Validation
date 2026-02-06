# Postman API Testing Steps

## Step 1 — GET Request
Method: GET
URL:
https://jsonplaceholder.typicode.com/posts/1

Click Send and observe response.

---

## Step 2 — POST Request
Method: POST
URL:
https://jsonplaceholder.typicode.com/posts

Body → raw → JSON

{
"title": "demo",
"body": "testing",
"userId": 1
}

---

## Step 3 — PUT Request
Method: PUT
URL:
https://jsonplaceholder.typicode.com/posts/1

Body:
{
"id": 1,
"title": "update",
"body": "data",
"userId": 1
}

---

## Step 4 — DELETE Request
Method: DELETE
URL:
https://jsonplaceholder.typicode.com/posts/1

---

## Step 5 — Authorization Test
Change resource ID:
posts/1 → posts/2 → posts/3

---

## Step 6 — Input Validation Test
Send invalid JSON values.

---

## Step 7 — Rate Limiting Observation
Send multiple requests quickly.

