# Bug Report: Lack of Clear Tooltip for Disabled "Add to Cart" Button

- **Application:** Online Drugstore Website
- **Environment:**
    - OS: Windows 10
    - Browser: Chrome
- **Severity:** Low
- **Priority:** Low

---

### Summary:
For products that are unavailable for online purchase, the "Add to Cart" button is correctly disabled. However, there is no direct tooltip on hover to explain *why* the button is disabled, which can lead to user confusion. The information about unavailability is present on the product card but is visually disconnected from the button itself.

### Preconditions:
1.  The user is viewing a product listing page (e.g., "Sales" page).
2.  The page contains products that are available and products that are unavailable for online purchase.

---

### Steps to Reproduce:
1.  Navigate to a product listing page.
2.  Scroll down to find a product that is marked as unavailable (e.g., a product with a greyed-out "Add to Cart" button and a label "Trenutno nije dostupno").
3.  Hover the mouse cursor over the disabled, grey "Add to Cart" button.

### Expected Result:
When hovering over the disabled button, a clear and contextual tooltip should appear, stating something like "This product is currently unavailable for online purchase" to immediately inform the user why they cannot add the item to their cart.

### Actual Result:
The mouse cursor changes to a "not allowed" symbol, but no explanatory tooltip appears on the button itself. The user must find the "unavailable" text elsewhere on the product card, which is less intuitive.
