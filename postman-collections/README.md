# Postman API Tests – Swagger Petstore

This collection contains 9 API test requests for the Swagger Petstore API, covering both positive and negative test scenarios.

---

##  Overview of Requests

| Method | Description                                      | Type        |
|--------|--------------------------------------------------|-------------|
| POST   | Add a new pet to the store (happy path)          | Positive    |
| POST   | Add a new pet to the store (empty body)          | Negative    |
| PUT    | Update an existing pet                           | Positive    |
| PUT    | Update Vucko info (happy path)                   | Positive    |
| PUT    | Update non-Vucko info (server error)             | Negative    |
| GET    | Find Vucko by ID (happy path)                    | Positive    |
| GET    | Find Vucko by ID (not found)                     | Negative    |
| DELETE | Remove Vucko (happy path)                        | Positive    |
| DELETE | Remove Vucko (non-existing ID)                   | Negative    |

---

##  Features and Scripts

Each request may include:
- Status code assertions (e.g., `200 OK`, `404 Not Found`, `500 Server Error`)
- Body content validations (e.g., name, tag, category)
- Variable extraction (`pet_ID`)
- Postman test scripts written in JavaScript

---

##  Tools Used

- Postman
- JavaScript for testing
- Swagger Petstore API ([swagger.io](https://swagger.io))

---

##  Files

This folder contains:

- `Swagger Petstore.postman_collection.json` – exported collection file
- `README.md` – this file

---

##  Notes

This test collection is part of a QA learning project. It demonstrates knowledge of REST API testing, test automation, and scripting within Postman.


## 🔍 Test Request Details

---

### 1. Add a New Pet (Happy Path)

- **Method**: POST  
- **Endpoint**: `/pet/262626`  
- **Type**: Happy Path

**Request Body:**
```json
{
  "id": 262626,
  "category": {
    "id": 0,
    "name": "dogs"
  },
  "name": "Vucko",
  "photoUrls": [
    "https://scontent.fbeg10-1.fna.fbcdn.net/v/t39.30808-6/464265904_8718019838258636_2868834979414991522_n.jpg"
  ],
  "tags": [
    {
      "id": 0,
      "name": "friendly"
    }
  ],
  "status": "available"
}

Test Scripts:


 Status is 200

 id is a number

 status is "available"

 category.name is "dogs"

 tags.name is "friendly"

 imageUrl is a string


2. Find Pet by ID (Happy Path)
Method: GET

Endpoint: /pet/:petId

Type: Happy Path

Description:
Fetches the pet with a specific ID (e.g. the one created in previous test).

Test Scripts:

 Status is 200

 Returned pet has correct id

 status is "available"


Test Scripts:

✅ Status is 200

✅ id is a number

✅ status is "available"

✅ category.name is "dogs"

✅ tags.name is "friendly"

✅ imageUrl is a string

2. Find Pet by ID (Happy Path)
Method: GET

Endpoint: /pet/:petId

Type: Happy Path

Description:
Fetches pet created in previous request.

Test Scripts:

✅ Status is 200

✅ Correct id returned

✅ status is "available"

3. Add a New Pet (Negative – Empty Body)
Method: POST

Endpoint: /pet

Type: Negative Path

Request Body: (Empty)

Expected Result:

❌ Status is 405 Method Not Allowed or similar

❌ Body returns validation error or missing data

4. Update Existing Pet (Positive)
Method: PUT

Endpoint: /pet

Type: Positive Path

Request Body:

json
Copy
Edit
{
  "id": 262626,
  "category": { "id": 0, "name": "dogs" },
  "name": "VuckoUpdated",
  "photoUrls": [],
  "tags": [],
  "status": "sold"
}
Test Scripts:

✅ Status is 200

✅ name is "VuckoUpdated"

✅ status is "sold"

5. Update Pet by Form (Happy Path)
Method: POST

Endpoint: /pet/:petId

Type: Happy Path

Form Data:

name=VuckoUpdated2

status=available

Test Scripts:

✅ Status is 200

✅ Successful update

6. Update Pet by Form (Negative – Wrong ID)
Method: POST

Endpoint: /pet/999999999

Type: Negative Path

Form Data:

name=Ghost

status=sold

Expected Result:

❌ Status is 404 Not Found or similar

❌ Response shows error

7. Delete Pet (Happy Path)
Method: DELETE

Endpoint: /pet/:petId

Type: Positive Path

Description:
Deletes existing pet (Vucko).

Test Scripts:

✅ Status is 200

✅ Pet removed successfully

8. Delete Pet (Negative – Invalid ID)
Method: DELETE

Endpoint: /pet/999999999

Type: Negative Path

Expected Result:

❌ Status is 404 Not Found

❌ Error message returned

9. Upload Pet Image
Method: POST

Endpoint: /pet/:petId/uploadImage

Type: Positive Path

Form Data:

file: sample image

Test Scripts:

✅ Status is 200

✅ Response includes message with image file name
