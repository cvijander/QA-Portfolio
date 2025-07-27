# Bug Report: Misleading Security Policy Warning During Viber Setup

- **Application:** Viber for Android
- **Environment:**
    - Device: Samsung Galaxy S23 (SM-S911B)
    - Platform: Android 13
    - Context: Samsung Remote Test Lab
- **Severity:** Low
- **Priority:** Medium

---

### Summary:
During the initial setup of the Viber application, a toast message appears at the bottom of the screen stating "Security policy restricts the use of device administrators". This message is confusing for the end-user, as it appears without context and suggests a problem or limitation, even though the app setup completes successfully.

### Steps to Reproduce:
1.  Install the Viber application from the Google Play Store.
2.  Launch the application for the first time.
3.  Proceed through the welcome screens and grant the required permissions.
4.  Enter a phone number to begin profile setup.
5.  Observe the bottom area of the screen during the setup process.

### Expected Result:
The application setup should complete without displaying any ambiguous or potentially alarming security warnings, unless a specific, critical permission is actually being blocked and a feature will not work.

### Actual Result:
A toast message "Security policy restricts the use of device administrators. Some Viber functionality may be limited" is displayed. This can cause user concern and confusion, as it is not clear what functionality is limited or why the warning is shown. This might be specific to the secure environment of the Remote Test Lab, but it is still unexpected behavior.
