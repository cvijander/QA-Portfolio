# Bug Report: Application Navigates to Home Screen When Accessing a Hidden Chat

- **Application:** Viber for Android
- **Environment:**
    - Device: Samsung Galaxy S23 (SM-S911B)
    - Platform: Android 13
- **Severity:** Medium
- **Priority:** Medium

---

### Summary:
When attempting to open a chat that has been designated as "hidden", the Viber application does not open the chat screen. Instead, it abruptly closes the hidden chat list and returns the user to the main Viber home screen (the main chat list), preventing access to the conversation.

### Steps to Reproduce:
1.  Open the Viber application.
2.  Access the list of hidden chats (e.g., via the search bar and entering a PIN).
3.  Tap on any hidden chat in the list.

### Expected Result:
The chat screen for the selected hidden contact should open normally, allowing the user to view the conversation history and send messages.

### Actual Result:
Upon tapping the hidden contact, the application immediately navigates back to the main Viber home screen. The selected chat does not open, effectively blocking the user from accessing their hidden conversations.
