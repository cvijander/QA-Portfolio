# Test Design: Boundary Value Analysis (BVA) for "Name" Field

This document demonstrates the application of the Boundary Value Analysis (BVA) technique for validating the "Name" input field.

- **Feature:** Add New Employee - "Name" Field
- **Requirement:** The "Name" field must accept strings between **1** and **30** characters.

---

### BVA Test Cases

The following test cases are designed based on the boundaries (min=1, max=30).

| Test Case ID | Description | Input Value (Length) | Expected Result |
| :--- | :--- | :--- | :--- |
| **BVA-NAME-01** | Below minimum | "" (0 chars) | Invalid. Error message "*Required" should be displayed. |
| **BVA-NAME-02** | Minimum | "B" (1 char) | Valid. The input is accepted. |
| **BVA-NAME-03** | Above minimum | "Bo" (2 chars) | Valid. The input is accepted. |
| **BVA-NAME-04** | Below maximum| "abcdefghijklmnopqrstuvwxyABCD" (29 chars) | Valid. The input is accepted. |
| **BVA-NAME-05** | Maximum | "abcdefghijklmnopqrstuvwxyABCDE" (30 chars) | Valid. The input is accepted. |
| **BVA-NAME-06** | Above maximum | "abcdefghijklmnopqrstuvwxyABCDEF" (31 chars) | Invalid. The system should prevent saving and display an error. |

---

### Observation & Suggestion

During testing, it was observed that the front-end allows entry of more than 30 characters. The validation error only appears **after** clicking "Add" (server-side validation).

**Improvement Suggestion:**
Implement front-end validation by adding the `maxlength="30"` attribute to the HTML input field. This would provide immediate feedback to the user and prevent them from entering more than 30 characters, improving the user experience and reducing unnecessary server requests.
