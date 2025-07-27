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
