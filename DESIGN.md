# Design System Document: The Editorial Freight Experience

## 1. Overview & Creative North Star

**Creative North Star: The Invisible Architect**
In the heavy, often cluttered world of logistics and freight, this design system acts as a breath of clarity. We are moving away from the "industrial dashboard" aesthetic toward a **High-End Editorial** experience. The system is defined by extreme whitespace, light-as-air typography, and a rejection of traditional structural boundaries.

To break the "template" look, we utilize **Intentional Asymmetry**. Important data points or hero images should not always be centered or boxed; they should float with purpose. By using the `surface-container` tiers and varying text weights (300 to 400), we create a sense of depth that feels curated rather than manufactured. The goal is to make a complex freight platform feel as effortless as reading a premium design magazine.

---

## 2. Colors

The palette is a sophisticated study in monochrome, utilizing tonal shifts to create hierarchy without visual noise.

*   **The "No-Line" Rule:** We do not use 1px solid borders to section content. Boundaries are defined by background shifts. A section might transition from `surface` (#f9f9f9) to `surface-container-low` (#f3f3f4) to signal a new context.
*   **Surface Hierarchy & Nesting:** Think of the UI as layers of fine paper. 
    *   **Base:** `surface` (#f9f9f9).
    *   **Interactive Cards:** `surface-container-lowest` (#ffffff) to provide a subtle "lift" against the background.
    *   **Nested Content:** Use `surface-container-high` (#e8e8e8) for internal groupings within a white card.
*   **The Glass & Gradient Rule:** For floating navigation bars or premium modals, use `surface` with a 70% opacity and a `20px` backdrop-blur. To give the primary black CTA "soul," apply a subtle radial gradient from `primary` (#000000) to `primary-container` (#3b3b3b).

---

## 3. Typography

We use **Inter** as our typographic backbone. The core of this system's "premium" feel is the contrast between massive, light-weight display text and tiny, high-contrast labels.

*   **Display & Headline (The Statement):** Use `display-lg` (3.5rem) and `headline-lg` (2rem). These must be set at **Font Weight: 300 or 400**. The "Modern" feel comes from the scale, not the thickness.
*   **Title & Body (The Content):** `title-md` (1.125rem) handles sub-headers, while `body-md` (0.875rem) serves as the workhorse. Keep these at weight 400 for maximum legibility against the white space.
*   **Labels (The Detail):** Use `label-sm` (0.6875rem) in `primary-fixed` (#5e5e5e). These should be all-caps with a `0.05em` letter spacing to add an authoritative, architectural feel to data points.

---

## 4. Elevation & Depth

We eschew "Material" shadows in favor of **Tonal Layering** and **Ambient Light**.

*   **The Layering Principle:** Depth is achieved by placing a `surface-container-lowest` (#ffffff) element on top of a `surface` (#f9f9f9) background. The contrast is enough to define the shape without a line.
*   **Ambient Shadows:** If a floating element (like a dropdown) requires a shadow, it must be nearly invisible. 
    *   *Spec:* `0px 20px 40px rgba(26, 28, 28, 0.04)`. Use the `on-surface` color for the shadow tint.
*   **The "Ghost Border" Fallback:** If accessibility demands a border, use `outline-variant` (#c6c6c6) at 20% opacity. It should be a suggestion of a border, not a fence.
*   **Glassmorphism:** Use semi-transparent layers for navigation overlays. This integrates the freight data into the background, preventing the UI from feeling "pasted on."

---

## 5. Components

### Buttons
*   **Primary:** Background: `primary` (#000000), Text: `on-primary` (#e2e2e2). Corner radius: `full` (9999px). The pill shape is essential for the "modern" look.
*   **Secondary:** Background: `none`, Border: `outline-variant` at 20% opacity, Text: `primary`. 
*   **Tertiary:** Text: `primary`. No container. Hover state: `surface-container` (#eeeeee).

### Cards & Lists
*   **The Divider-Free Rule:** Never use horizontal lines. Use the **Spacing Scale** `8` (2.75rem) to separate list items. Use a `surface-container-low` background on hover to define the interactive area.

### Input Fields
*   Background: `surface-container-lowest` (#ffffff). 
*   Border: `none` or "Ghost Border" (20% opacity `outline-variant`).
*   Focus State: A subtle 1px "Ghost Border" becomes 100% opaque `primary`.

### Chips
*   **Selection:** Background `primary`, Text `on-primary`.
*   **Filter:** Background `surface-container-high`, Text `on-surface`. Corner radius: `sm` (0.5rem) for a slightly more technical look than buttons.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use extreme whitespace. If a section feels "finished," add another `3.5rem` (`spacing.10`) of padding.
*   **Do** use light font weights (300) for large headlines to maintain an air of sophistication.
*   **Do** rely on `surface` color shifts to define areas of the freight dashboard (e.g., Sidebar vs. Main Grid).

### Don't:
*   **Don't** use 1px solid black or grey borders. They kill the "Editorial" vibe immediately.
*   **Don't** use standard drop shadows (e.g., 2px blur, 50% opacity). They feel dated and heavy.
*   **Don't** crowd the interface. If a freight table has 20 columns, use a horizontal scroll on a `surface-container-lowest` layer rather than shrinking the text.
*   **Don't** use bold weights unless it is for a tiny `label-sm` to ensure it remains readable.

---

## 7. Spacing & Rhythm

All spacing must follow the defined scale to maintain the "Invisible Architect" feel.
*   **Hero Padding:** Use `spacing.20` (7rem) or `spacing.24` (8.5rem) for top/bottom margins.
*   **Component Internal Padding:** Use `spacing.4` (1.4rem) for card gutters.
*   **Micro-spacing:** Use `spacing.1` (0.35rem) between a label and its data point to create tight, functional clusters of information.