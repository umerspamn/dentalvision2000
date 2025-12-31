# Manual Test Checklist for DentalVision2000

Please perform these 10 steps on a mobile device (ideally a low-end Android or in Chrome DevTools mobile view) to verify the fixes.

1.  **Mobile Menu Open:** Tap the hamburger menu icon.
    *   *Pass Criteria:* Menu slides in smoothly from the right. The background page is covered by a dark overlay. You cannot scroll the background page.
2.  **Submenu Toggle:** Inside the menu, tap "Services".
    *   *Pass Criteria:* The submenu expands smoothly to reveal service links. The arrow icon rotates. The menu remains open.
3.  **Navigation:** Tap "Root Canal Treatment" inside the submenu.
    *   *Pass Criteria:* The menu closes automatically. The page scrolls to the "Services" or "Treatments" section.
4.  **Backdrop Close:** Open the menu again, then tap the dark overlay (outside the menu panel).
    *   *Pass Criteria:* The menu closes smoothly.
5.  **Sticky Header:** Scroll down the page.
    *   *Pass Criteria:* The top navigation bar sticks to the top of the screen. It does not obscure the content awkwardly.
6.  **Doctor Cards:** Scroll to the "Meet the Doctors" section.
    *   *Pass Criteria:* Cards have full photo backgrounds (even if placeholder/blue for now). Text is readable against a dark gradient at the bottom.
7.  **Floating WhatsApp:** Scroll to the very bottom (Footer).
    *   *Pass Criteria:* The green floating WhatsApp button stays visible in the bottom-right corner but does not cover the "Quick Links" or copyright text too badly (some overlap is okay, but it should be tappable).
8.  **CTA Links:** Tap "Schedule Appointment" or "Online Consultation".
    *   *Pass Criteria:* A new tab opens with the WhatsApp API URL (`wa.me/...`).
9.  **Horizontal Scroll Check:** Swipe left/right on the page.
    *   *Pass Criteria:* The page does *not* move sideways. There is no horizontal scrollbar.
10. **Performance/Smoothness:** Scroll up and down quickly.
    *   *Pass Criteria:* The scrolling feels smooth, no major "jank" or stuttering, especially on images.
