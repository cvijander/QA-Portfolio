# Postman API Tests – Swagger Petstore

This collection contains API tests for the Swagger Petstore v2 API. It includes a variety of requests covering different endpoints and HTTP methods, with both positive and negative test scenarios.

The primary focus is on the `/pet` endpoint to demonstrate a complete CRUD (Create, Read, Update, Delete) workflow, including test scripts for validating responses.

---

### 📂 How to Use

1.  **Import Collection**: Import the `Swagger Petstore.postman_collection.json` file into your Postman application.
2.  **Set Base URL**: The collection uses a variable `{{baseUrl}}` which is pre-configured to `https://petstore.swagger.io/v2`.

---

### 🔁 Test Scenarios Overview

| Method | Endpoint | Description | Test Type |
| :--- | :--- | :--- | :--- |
| **POST** | `/pet` | Add a new pet with a valid body. | **Positive** |
| **POST** | `/pet` | Attempt to add a pet with an empty body. | **Negative** |
| **GET** | `/pet/{petId}` | Find the newly created pet by its ID. | **Positive** |
| **GET**| `/pet/{petId}` | Attempt to find a pet with a non-existent ID. | **Negative** |
| **PUT** | `/pet` | Update the status of the created pet to "sold". | **Positive** |
| **POST** | `/pet/{petId}` | Upload an image for the pet. | **Positive**|
| **DELETE** | `/pet/{petId}` | Delete the created pet. | **Positive** |
| **DELETE**| `/pet/{petId}` | Attempt to delete the same pet again (should fail). | **Negative** |

---

### 🛠️ Tools & Concepts Demonstrated

* **Tool**: Postman
* **API**: Swagger Petstore API (swagger.io)
* **Concepts**:
    * REST API testing (GET, POST, PUT, DELETE)
    * Positive and negative test paths
    * Chaining requests (using a variable from one request in another)
    * Postman scripting (JavaScript) for assertions
    * Status code and response body validation
