# Bug Report: Sticky Filter Menu Overlaps Navigation and Content on Scroll-Up

- **Application:** Fashion Store Website
- **Environment:**
    - OS: Windows 10
    - Browser: Chrome
- **Severity:** Low
- **Priority:** Medium

---

### Summary:
On product listing pages, when the user scrolls down, a sticky filter menu correctly stays at the top of the screen. However, when the user begins to slowly scroll back up, the main navigation menu reappears and momentarily overlaps with the sticky filter menu and the product grid, creating a visual glitch.

### Preconditions:
1.  The user is on any product listing page (e.g., Women, Men, Kids categories).
2.  The page has enough products to require scrolling.

---

### Steps to Reproduce:
1.  Navigate to a product category page.
2.  Scroll down the page until the main navigation disappears and the sticky filter menu is visible at the top.
3.  Slowly scroll back up.
4.  Observe the area at the top of the page as the main navigation reappears.

### Expected Result:
The main navigation and the sticky filter menu should have a smooth transition. They should not be visible at the same time in a way that causes them to overlap each other or cover the product content. For example, the filter menu should disappear cleanly as the main navigation scrolls into view.

### Actual Result:
For a brief moment during the scroll-up action, both menus are rendered on top of each other, and they both overlap the top row of products.
