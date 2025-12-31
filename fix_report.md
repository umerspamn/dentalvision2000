**Issues Found & Fixed:**

*   **Mobile Menu:**
    *   **Issue:** Missing backdrop, no scroll lock, no close button inside panel, inconsistent z-indexing.
    *   **Fix:** Added `.menu-backdrop`, implemented body scroll lock in JS, added close button, set z-index hierarchy (Backdrop: 1500, Panel: 1501).
    *   **Issue:** Submenu was basic and lacked animation.
    *   **Fix:** Added smooth height transition, arrow rotation, and `aria-expanded` attributes.
*   **Doctors Cards:**
    *   **Issue:** Weak overlay, text hard to read on some images, old design.
    *   **Fix:** Redesigned with full-height background image and strong bottom gradient overlay for readability. Added hover lift effect.
*   **Layout & Spacing:**
    *   **Issue:** Extensive use of `<br>` tags for spacing; inconsistent margins.
    *   **Fix:** Removed all `<br>` layout hacks. Used CSS `gap`, `margin-bottom`, and utility classes.
*   **Consistency:**
    *   **Issue:** Service hours varied across sections (Top bar vs Footer).
    *   **Fix:** Standardized to "Mon–Fri 11:00 AM – 9:00 PM · Sat–Sun Closed".
*   **Accessibility:**
    *   **Issue:** Missing focus states, aria-labels.
    *   **Fix:** Added `:focus-visible` styles, `aria-label` for buttons, and `prefers-reduced-motion` support.
*   **Performance:**
    *   **Issue:** Potential layout thrashing.
    *   **Fix:** Used `will-change: transform` for mobile menu, `IntersectionObserver` for scroll animations.

**Manual Test Checklist:**

1.  **Mobile Menu Open:** Tap hamburger on mobile view. Verify backdrop appears and body does not scroll.
2.  **Mobile Menu Close:** Tap the "×" button inside the menu. Verify it closes smoothly.
3.  **Backdrop Close:** Open menu, then tap the dark background. Verify menu closes.
4.  **Submenu:** Tap "Services" in mobile menu. Verify it expands smoothly and arrow rotates.
5.  **Navigation:** Click a link in the mobile menu (e.g., "Meet the Doctors"). Verify menu closes and page navigates.
6.  **Doctors Cards:** Hover over a doctor card (desktop) or look at it (mobile). Verify text is readable against the photo background.
7.  **WhatsApp:** Tap the floating WhatsApp button. Verify it opens WhatsApp in a new tab.
8.  **FAQ:** Tap an FAQ item. Verify it expands and others collapse (if multiple open logic is set to exclusive, which it is).
9.  **Responsiveness:** Resize browser to 360px width. Verify no horizontal scrolling and content stacks correctly.
10. **Keyboard Nav:** Tab through the page. Verify focus ring is visible on all interactive elements.
