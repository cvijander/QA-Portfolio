# Test Case: Successfully create a new employee with valid data

- **Test Case ID:** TC-01
- **Feature:** Employee Management
- **Priority:** High

---

### Summary:
This test case verifies that a user with HR permissions can successfully create a new employee by filling in all required fields with valid data.

### Preconditions:
1.  The user is logged in with an HR account.
2.  The user is on the main Employee page: `https://demo.hrapp.com/#/employees`

---

### Test Steps:

| Step | Action | Expected Result |
| :--- | :--- | :--- |
| 1. | Click on the **"+ Add Employee"** button. | The user is redirected to the "Add Employee" page. |
| 2. | Fill in the **Name** field with "Borivoje". | The "Name" field displays "Borivoje". The avatar shows "B". |
| 3. | Fill in the **Surname** field with "Vu***c". | The "Surname" field displays "Vu***ic". The avatar shows "BV".|
| 4. | Select a **Date of Birth** (e.g., 11/04/1977). | The selected date is correctly displayed in the field. |
| 5. | Fill in the **Email** field with a valid email. | The "Email" field displays the entered email. |
| 6. | Select an **Enrollment Date** (e.g., 28/05/2025). | The selected date is correctly displayed in the field. |
| 7. | Fill in all other required fields (**Locations**, **Tier**, etc.) with valid data. | All fields are populated correctly. |
| 8. | Click the **"Add"** button. | - The system redirects the user to the Employee list page. <br>- An info message "Employee successfully created" is displayed. <br>- The new employee "Borivoje Vu***c" appears in the employee list. |
