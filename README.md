# GoIT Markup Homework #6: Responsive Design

## Description of the Assignment

This repository contains the solution for GoIT Markup Homework #6. The primary goal of this assignment was to implement a fully responsive design for the webpage, converting the initial desktop-first layout to follow the **Mobile First methodology**. The adaptation targets three specific breakpoints: **320px** (mobile), **768px** (tablet), and **1158px** (desktop).

The work focused on restructuring the CSS using `min-width` media queries, ensuring correct layout and element visibility across different screen sizes, implementing a functional mobile menu, and optimizing images for high-resolution (Retina) displays.

---

## 🛠️ Key Technical Features

The following key technical solutions were implemented in this assignment:

### Mobile First CSS Structure
* **Base Styles:** The CSS was rewritten so that styles outside of media queries apply to the smallest screen size (320px+).
* **Media Queries (`min-width`):** Styles for tablet (768px+) and desktop (1158px+) were added progressively within `@media screen and (min-width: ...)` rules, overriding or extending the base mobile styles.
* **Breakpoint Adherence:** Layout adjustments strictly follow the specified breakpoints of 320px, 768px, and 1158px.

### Responsive Layout Adaptation
* **Flexbox Layouts:** `display: flex` (along with `flex-direction`, `gap`, `justify-content`, and `align-items`) was used extensively to manage the layout of elements within sections (e.g., Header, Footer, Team list, Portfolio list).
* **Conditional Display:** Elements like the desktop navigation/contacts and the mobile menu button are conditionally displayed or hidden using `display: none;` based on the active media query.
* **Calculated Widths (`calc()`):** For sections with flexible grid items (like Portfolio on desktop), the `calc()` function was used to determine item widths based on the container width and gap size.
* **Fixed Width Approach:** For sections with fixed-width items (like Team), `width` was set directly, and `justify-content: center` with `flex-wrap: wrap` was used on the container to manage arrangement.
* **Text Alignment:** `text-align` properties were adjusted within media queries to match the design requirements for different screen sizes.

### Mobile Menu Implementation
* **Full Viewport:** The `.mobile-menu-container` is styled with `position: fixed`, `width: 100%`, and `height: 100vh` to cover the entire viewport.
* **Initial State (Hidden):** By default, the menu is hidden off-screen using `transform: translateX(100%);` and `visibility: hidden;`.
* **Activation (`.is-open`):** An `.is-open` class selector is defined in CSS to transition the menu into view (`transform: translateX(0);`, `visibility: visible;`).
* **Internal Layout:** `display: flex`, `flex-direction: column`, and `justify-content: space-between` are used within `.mobile-menu-inner` to structure the navigation, contacts, and social links.

### Modal Window Adaptation
* **Responsive Sizing:** The `width`, `height`, and `padding` of the existing modal window (`.model`) are adjusted using media queries to fit smaller screens appropriately while maintaining the desktop layout on larger screens.

### Responsive Background Images (Retina Support)
* **CSS Backgrounds:** Different background images are applied to the `.hero` section for mobile, tablet, and desktop breakpoints using `background-image` within the respective base styles and media queries.
* **Retina Support:** `@media (min-resolution: 192dpi)` queries are used alongside the breakpoint media queries to serve high-resolution (`@2x`) background images to devices with high pixel density.

### Content Images (Retina Support)
* **`srcset` Attribute:** The `srcset` attribute is added to all `<img>` tags within the `.team` and `.portfolio` sections, providing paths to both `1x` and `2x` image versions. This allows the browser to automatically select and load the appropriate image.
* **`width` and `height` Attributes:** Explicit `width` and `height` attributes are set on `<img>` tags to improve rendering performance.

---

## 🚀 Live Page

The project is hosted on GitHub Pages. You can view the live result here:

**[https://idziamko.github.io/goit-markup-hw-06/]**
