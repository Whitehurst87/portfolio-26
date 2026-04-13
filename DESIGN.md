# Design System Specification: Nocturnal Luminescence

## 1. Overview & Creative North Star
**Creative North Star: "The Celestial Architect"**
This design system moves away from the "flat" web by embracing the depth of a midnight sky illuminated by a distant sun. It is designed for premium digital experiences that require a sense of quiet authority and precision. By utilizing intentional asymmetry, expansive negative space, and overlapping layers, we break the predictable "boxed" layout in favor of a high-end editorial feel.

The aesthetic isn't just "dark mode"—it is a curated environment where light is used sparingly and intentionally to guide the eye. We leverage the tension between the cold, deep navy abyss and the heat of the vibrant orange accents to create a rhythmic, sophisticated user journey.

---

## 2. Colors & Tonal Depth

### The "No-Line" Rule
To maintain a high-end, seamless feel, **1px solid borders are strictly prohibited for sectioning.** Boundaries must be defined through background color shifts or tonal transitions. Use `surface-container-low` to distinguish a section from the base `surface`.

### Surface Hierarchy & Nesting
Think of the UI as a series of physical layers. Use the following tiers to create a "stacked" hierarchy:
*   **Base Layer:** `surface` (#010e23) for the main canvas.
*   **Sunken Elements:** `surface-container-low` (#02132b) for secondary content or sidebars.
*   **Raised Elements:** `surface-container-high` (#0a203c) for cards and interactive modules.
*   **Floating Elements:** `surface-container-highest` (#0f2644) for modals or popovers.

### The "Glass & Gradient" Rule
Standard flat colors feel static. To inject "soul," use:
*   **Signature Gradient:** A linear transition from `primary` (#ff9064) to `primary-container` (#ff7941) at a 135-degree angle for hero CTAs and primary actions.
*   **Glassmorphism:** For navigation bars or floating menus, use `surface-variant` (#0f2644) at 70% opacity with a `20px` backdrop-blur. This allows the navy background to bleed through, softening the UI.

---

## 3. Typography: The Manrope Scale
We use **Manrope** exclusively. Its geometric yet humanist qualities provide the "Editorial" weight needed for this system.

*   **Display (lg/md/sm):** Use for hero moments. Set with tight letter-spacing (-0.02em) and `Font-Weight: 800`.
*   **Headlines:** Use `headline-lg` for section starts. Place them asymmetrically (e.g., offset to the left) to break the grid.
*   **Body:** `body-lg` is your workhorse. Use `Font-Weight: 400` with a generous line-height (1.6) to ensure readability against the dark background.
*   **Labels:** `label-md` should always be `Uppercase` with `Letter-spacing: 0.1em` to denote technical or metadata status.

---

## 4. Elevation & Depth

### The Layering Principle
Avoid "Drop Shadows" in the traditional sense. Depth is achieved by placing a `surface-container-lowest` card on a `surface-container-low` section. This "negative elevation" feels more modern and grounded.

### Ambient Shadows
If an object must float (e.g., a Modal), use an **Ambient Tinted Shadow**:
*   **Y:** 20px, **Blur:** 40px
*   **Color:** `#000000` at 25% opacity, layered with a secondary shadow of `primary` (#ff9064) at 5% opacity to mimic light bounce.

### The "Ghost Border" Fallback
Where separation is functionally required (e.g., input fields), use a **Ghost Border**: `outline-variant` (#3a4860) at 20% opacity. Never use 100% opaque lines.

---

## 5. Components

### Buttons
*   **Primary:** A gradient fill (`primary` to `primary-container`). Text color: `on-primary` (#571a00). Border-radius: `md` (0.375rem).
*   **Secondary:** Ghost style. No fill, `Ghost Border` (20% opacity), text in `primary`.
*   **Tertiary:** Text-only, `label-md` styling, with a subtle underline that appears on hover.

### Cards & Lists
*   **Forbid Divider Lines.** Separate list items using `16px` of vertical white space or by alternating background tones between `surface` and `surface-container-low`.
*   **Cards:** Use `surface-container-high` with a `lg` (0.5rem) corner radius. Elements inside the card should be padded by at least `24px`.

### Input Fields
*   **Default:** `surface-container-highest` background with a subtle `Ghost Border`.
*   **Focus:** The border transitions to 100% opacity `primary` (#ff9064) with a tiny `2px` outer glow of the same color.

### Signature Component: The "Ember" Indicator
A small, `2px` tall horizontal line using the `tertiary` (#fd894f) color placed above active navigation items or as a prefix to "Headline-sm" titles to signal focus.

---

## 6. Do’s and Don’ts

### Do:
*   **Do use asymmetrical margins.** Allow headlines to hang into the left margin to create an editorial feel.
*   **Do use "On-Surface-Variant" (#9dacc7)** for secondary text to maintain a soft contrast ratio that reduces eye strain.
*   **Do lean into Roundedness.** Use the `xl` (0.75rem) scale for large containers to soften the professional navy tone.

### Don't:
*   **Don't use pure White (#FFFFFF) for long-form body text.** Use `on-surface` (#dae6ff) for a more comfortable reading experience.
*   **Don't use the Accent Orange for large areas.** The `primary` color is like fire; it’s meant to warm the room, not burn it down. Use it only for interactive elements and highlights.
*   **Don't use standard "Grey" shadows.** Shadows must be tinted with the deep navy of the `surface` to look natural.

---