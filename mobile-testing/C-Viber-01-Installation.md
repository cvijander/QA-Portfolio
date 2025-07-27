# Test Case: Viber Installation and Initial Setup

- **Test Case ID:** TC-Viber-01
- **Feature:** Application Installation & First-Time Setup
- **Priority:** High

---

### Summary:
This test case verifies that the Viber application can be successfully installed from the Google Play Store and that the initial user profile setup can be completed without errors.

### Environment:
- **Device:** Samsung Galaxy S23 (SM-S911B)
- **Platform:** Android 13
- **Testing Tool:** Samsung Remote Test Lab

### Preconditions:
1.  A valid Google account is logged into on the device.
2.  The Google Play Store is accessible and functional.

---

### Test Steps:

| Step | Action | Expected Result |
| :--- | :--- | :--- |
| 1. | Open the Google Play Store application. | The Play Store homepage loads successfully. |
| 2. | Use the search bar to search for "Viber". | The official Viber application appears in the search results. |
| 3. | Tap the "Install" button. | The installation process begins, showing a progress bar. |
| 4. | Once installed, tap the "Open" button. | The Viber application launches and displays its welcome screen. |
| 5. | Accept the initial terms and required permissions. | The application proceeds to the profile setup screen. |
| 6. | Enter a valid phone number, name, and other required data to set up a profile. | The data is accepted, and the profile is successfully created. |
| 7. | **(Final Verification)** | **The user is taken to the Viber home screen, with the main chat interface displayed.**|

### Postconditions:
- The Viber application is installed and configured.
- The user is logged into their account.
