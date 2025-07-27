# Postman API Tests – Swagger Petstore

This collection contains 9 API test requests for the Swagger Petstore API, covering both positive and negative test scenarios.

---

## 🔁 Overview of Requests

| Method | Description                                      | Type        |
|--------|--------------------------------------------------|-------------|
| POST   | Add a new pet to the store (happy path)          | Positive    |
| POST   | Add a new pet to the store (empty body)          | Negative    |
| PUT    | Update an existing pet                           | Positive    |
| POST   | Update pet by form (happy path)                  | Positive    |
| POST   | Update pet by form (non-existing ID)             | Negative    |
| GET    | Find pet by ID (happy path)                      | Positive    |
| GET    | Find pet by ID (not found)                       | Negative    |
| DELETE | Remove pet (happy path)                          | Positive    |
| DELETE | Remove pet (non-existing ID)                     | Negative    |
| POST   | Upload pet image                                 | Positive    |

---

## 🛠️ Tools Used

- Postman
- JavaScript (for test scripts)
- Swagger Petstore API – [swagger.io](https://swagger.io)

---

## 📁 Files Included

- `Swagger Petstore.postman_collection.json` – Exported Postman collection
- `README.md` – This file

---

## 📌 Notes

This test collection is part of a QA learning project. It demonstrates knowledge of:
- REST API concepts
- Positive and negative test paths
- Postman scripting and assertions
- Status code validation
- Request body and response handling

---

## 🔍 Test Case Details

---

### 1. Add a New Pet (Happy Path)

**Method**: POST  
**Endpoint**: `/pet`  
**Type**: Positive

**Request Body**:
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
