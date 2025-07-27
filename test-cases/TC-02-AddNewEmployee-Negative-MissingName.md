# Test Case: Attempt to create a new employee without a name

- **Test Case ID:** TC-02
- **Feature:** Employee Management
- **Priority:** High

---

### Summary:
This test case verifies that the system prevents the creation of a new employee if the mandatory "Name" field is left empty.

### Preconditions:
1.  The user is logged in with an HR account.
2.  The user is on the "Add Employee" page.

---

### Test Steps:

| Step | Action | Expected Result |
| :--- | :--- | :--- |
| 1. | Leave the **Name** field empty. | - |
| 2. | Fill in all other mandatory fields (Surname, Email, etc.) with valid data. | All other fields are populated correctly. |
| 3. | Click the **"Add"** button. | - The new employee is **not** created. <br>- The user remains on the "Add Employee" page. <br>- A validation error message, such as "*Required*", is displayed below the "Name" field. |
