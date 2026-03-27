# Design System Document

## 1. Overview & Creative North Star: "The Editorial Lens"

This design system is built to transform a standard service-based interface into a high-end digital gallery. The Creative North Star is **"The Editorial Lens"**—a philosophy that treats every screen as a curated magazine spread rather than a software dashboard. 

To break the "template" look common in school photography, this system prioritizes **intentional asymmetry**. We reject the rigid, centered grid in favor of layouts where large-scale imagery anchors the composition, and typography "breathes" through expansive whitespace. By overlapping text elements across image boundaries and using sophisticated tonal layering, we create a sense of depth that feels professional, trustworthy, and modern.

---

## 2. Colors & Surface Philosophy

The palette moves away from flat, "web-safe" aesthetics toward a high-contrast, sophisticated atmosphere.

### The Palette
*   **Primary (`#00535b`):** Our signature deep teal. Used for moments of high intent.
*   **Surface Tones:** A range from `surface_container_lowest` (`#ffffff`) to `surface_dim` (`#d9dadb`). 
*   **Accents:** `tertiary` (`#713d10`) is used sparingly for "warmth" in calls to action, mimicking the organic tones of high-end photography.

### The "No-Line" Rule
**Standard 1px borders are strictly prohibited for sectioning.** 
Structural boundaries must be defined solely through background color shifts. To separate a testimonial section from a gallery, transition from `surface` (`#f8f9fa`) to `surface_container_low` (`#f3f4f5`). This creates a seamless, "liquid" flow that feels more premium than a boxed-in layout.

### Glass & Gradient Rule
To provide "visual soul," use linear gradients for primary actions, transitioning from `primary` (`#00535b`) to `primary_container` (`#006d77`). For floating navigation or over-image overlays, apply **Glassmorphism**:
*   **Background:** `surface` at 70% opacity.
*   **Effect:** `backdrop-blur: 20px`.
*   **Result:** A frosted-glass effect that keeps the focus on the photography while maintaining legibility.

---

## 3. Typography: Authority Through Scale

We utilize two distinct typefaces to balance modern utility with editorial flair.

*   **Display & Headlines (Manrope):** Chosen for its geometric precision. Use `display-lg` (3.5rem) with tight letter-spacing for hero headers to command authority.
*   **Body & Labels (Inter):** The workhorse. Inter provides exceptional legibility at smaller scales.

**Hierarchy Strategy:**
*   **The Power Gap:** Create a significant size jump between `headline-lg` and `body-lg`. This "High-Contrast Scale" makes the typography feel intentional and curated.
*   **Tonal Type:** Use `on_surface_variant` (`#3e494a`) for secondary body text to reduce visual noise and lead the eye toward the primary headlines.

---

## 4. Elevation & Depth: Tonal Layering

We convey hierarchy through physical stacking rather than artificial shadows.

*   **The Layering Principle:** Treat the UI as sheets of fine paper. A card (`surface_container_lowest`) sitting on a section background (`surface_container_low`) creates a "Soft Lift" that feels natural.
*   **Ambient Shadows:** If an element must float (e.g., a modal or floating action button), use an extra-diffused shadow: `box-shadow: 0 20px 40px rgba(25, 28, 29, 0.05)`. The shadow color must be a low-opacity version of `on_surface`, never pure black.
*   **The Ghost Border Fallback:** For input fields or essential containment, use the `outline_variant` token at **20% opacity**. It should be barely felt, not seen.

---

## 5. Components

### Buttons
*   **Primary:** Uses the `primary` to `primary_container` gradient. Roundedness: `md` (0.375rem). Use `title-sm` for button labels.
*   **Secondary:** Ghost-style with a `primary` label and no background. Use for "Learn More" actions.
*   **Haptic Sizing:** All buttons must have a minimum height of `10` (3.5rem) on mobile to ensure accessibility.

### Cards & Lists
*   **The Divider Ban:** Never use horizontal lines to separate list items. Use the spacing scale `6` (2rem) to create clear breathing room, or alternate background shades between `surface_container_low` and `surface_container_lowest`.
*   **Image Cards:** Use `xl` (0.75rem) rounded corners. Imagery should always feature a subtle `primary` tint in the shadows to unify the brand.

### Input Fields
*   **Style:** Minimalist. No solid borders; only a bottom-weighted `outline_variant` at 20% opacity. 
*   **State:** When focused, the bottom border transitions to `primary` with a 2px stroke.

### Featured Gallery Slider (Custom Component)
*   An asymmetrical horizontal scroller where images "bleed" off the edge of the screen. 
*   Captions use `label-md` in all-caps with `0.1rem` letter spacing, positioned vertically against the image edge.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use `20` (7rem) or `24` (8.5rem) spacing between major sections to emphasize the "High-End" feel.
*   **Do** overlap typography on top of images (using the Glassmorphism rule) to create a sense of depth.
*   **Do** use `surface_bright` for highlight containers to draw the eye to "Special Offers."

### Don’t:
*   **Don’t** use the `error` color (`#ba1a1a`) for anything other than critical system failures; use `tertiary` for soft warnings.
*   **Don’t** center-align long blocks of body text. Maintain a strong left-aligned axis to keep the editorial "grid" intact.
*   **Don’t** use high-contrast shadows. If the depth isn't clear, adjust the `surface_container` tier instead.

---

## 7. Spacing & Rhythm

All layouts must adhere to the spacing scale. 
*   **Standard Padding:** `6` (2rem) for internal container padding.
*   **Hero Margin:** `16` (5.5rem) for bottom margins on hero titles to ensure the "Editorial" breathing room.
*   **Tight Grouping:** `2` (0.7rem) for label-to-input relationships. 

By strictly adhering to these tonal shifts and typographic hierarchies, we ensure this design system remains sophisticated, avoids the "standard" UI traps, and presents the studio as a premium creative partner.