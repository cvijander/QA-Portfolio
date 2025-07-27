# Test Design: Decision Table for New Employee Creation

This document uses a Decision Table to analyze the conditions required for creating a new employee and to identify the minimum set of required fields.

---

### Decision Table

| Conditions (Is field filled?) | R1 | R2 | R3 | R4 | R5 | R6 |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **Name** is filled? | **T** | **T** | **F** | **T** | **T** | **T** |
| **Surname** is filled? | **T** | **T** | **T** | **F** | **T** | **T** |
| **Email** is filled? | **T** | **T** | **T** | **T** | **F** | **T** |
| **Locations** is selected? | **T** | **T** | **T** | **T** | **T** | **F** |
| **Tier** is selected? | **T** | **F** | **T** | **T** | **T** | **T** |
| **Action: Member is Created**| **✔**| **✔** | **❌**| **❌**| **❌**| **❌**|

*(`T` = True, `F` = False, `✔` = Action happens, `❌` = Action does not happen)*

---

### Analysis and Conclusion

Based on the decision table rules and empirical testing within the application, the following conclusion was reached:

**A minimum of 5 fields are mandatory to create a new employee.**

- **Mandatory Fields:**
    1.  Name
    2.  Surname
    3.  Email
    4.  Locations
    5.  Tier

- **Optional Fields:** All other fields (Date of Birth, Contact, Team, etc.) are optional and do not block the creation of a new user.
- **Non-functional Field:** The "Branch code" field was identified as non-functional as it contained no selectable options.

This technique helped to efficiently identify the core requirements for the feature and optimize the testing effort by focusing on these key validation rules.
