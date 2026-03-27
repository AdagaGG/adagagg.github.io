# Design System Document

## 1. Overview & Creative North Star
### Creative North Star: "The Architectural Console"
This design system is built to reflect the precision of AI systems engineering through an editorial, high-density lens. It rejects the "softness" of consumer web apps in favor of a brutalist, terminal-inspired aesthetic that feels authoritative and enterprise-grade. 

The system breaks away from standard templates by utilizing a **Bento Box grid**—an intentional arrangement of varying rectangular volumes—and **Terminal-style containers**. By combining the raw, technical feel of a code editor with the sophisticated hierarchy of a high-end data dashboard, we create a "Digital Curator" persona: clean, structured, and profoundly technical.

## 2. Colors
The palette is a "Deep Dark" configuration, utilizing monochromatic depth punctuated by high-energy amber accents.

*   **Primary Accent (`#ffc965`):** Used sparingly for interactive elements and critical data points. It represents the "glow" of a terminal line.
*   **Surface Hierarchy:**
    *   **Base:** `surface` (`#0e0e0e`) is the foundation.
    *   **Nesting:** To create depth, use `surface-container-low` (`#131313`) for large section blocks and `surface-container-high` (`#201f1f`) for terminal cards.
*   **The "No-Line" Rule:** Sectioning must never be achieved with 1px solid borders. Use the shift from `surface` to `surface-container-low` to define global regions. The only allowed "lines" are functional terminal window borders (see Elevation).
*   **The "Glass & Gradient" Rule:** For floating navigation or action menus, use `surface-variant` (`#262626`) at 70% opacity with a `20px` backdrop-blur. Apply a subtle linear gradient (from `primary` to `primary-container`) on high-level CTAs to add a "liquid gold" finish.

## 3. Typography
The system uses a high-contrast pairing: **Space Grotesk** for technical structure and **Manrope** for readability.

*   **Display & Headlines (Space Grotesk):** These should be treated as architectural elements. `display-lg` (3.5rem) is reserved for the Hero Name. Use tight letter-spacing (-0.02em) to maintain a "blocky," high-end editorial feel.
*   **Titles & Body (Manrope):** `title-md` and `body-lg` provide a functional contrast. Manrope’s geometric clarity ensures that dense data engineering descriptions remain legible.
*   **Labels (Space Grotesk):** `label-md` (0.75rem) should be used for "Metadata" (e.g., timestamps, tags, or file paths in terminal headers), often in ALL CAPS with increased tracking (+0.05em).

## 4. Elevation & Depth
Depth in this system is not about "floating"; it is about "stacking" technical layers.

*   **Tonal Layering:** Instead of shadows, use the surface scale. A card (`surface-container-highest`) sitting on a section (`surface-container-low`) creates a natural, sharp lift.
*   **The Layering Principle:** Treat the portfolio as a series of nested terminal windows. Each window uses a slightly brighter surface token than its parent to indicate focus.
*   **The "Ghost Border" Fallback:** For Terminal Containers, use the `outline-variant` token (`#484847`) at 20% opacity. This creates a "hairline" effect that defines the shape without cluttering the dark mode environment.
*   **Ambient Shadows:** When a card must overlap another (e.g., a "Project Detail" modal), use a massive blur (40px+) at 8% opacity using the `on-surface` color to create a dark, atmospheric glow rather than a harsh drop shadow.

## 5. Components

### Terminal Containers (Cards)
*   **Geometry:** Sharp 0px corners across all scales.
*   **Top Bar:** Every card must feature a defined "Title Bar" using `surface-container-highest`. Inside, place three window controls (close/min/max) as 8px circles in `secondary-container` and the file path/title in `label-sm`.
*   **Grid:** Use the Bento Box layout. Projects should occupy larger spans (e.g., 2x2 or 3x2), while technical skills occupy 1x1 tiles.

### Interactive Elements
*   **Buttons:**
    *   **Primary:** Solid `primary` (`#ffc965`) background with `on-primary` text. No rounded corners.
    *   **Secondary:** Ghost style. `outline` border (Ghost Border rule applies) with `primary` text.
*   **Chips (Data Tags):** Small, sharp rectangles using `surface-variant`. Use `label-sm` for text. These should look like code snippets or terminal flags (e.g., `--v:1.0`).
*   **Input Fields:** Strictly rectangular. Use `surface-container-lowest` for the field background to create an "inset" look. The active state is signaled by a `primary` Ghost Border.

### Lists & Data
*   **Data Lists:** Forbid horizontal dividers. Use `3.5rem` (Spacing 10) of vertical space to separate items.
*   **Icons:** Use thin-stroke, technical iconography. Icons should be `primary` or `on-surface-variant`.

## 6. Do's and Don'ts

### Do:
*   **Do** use intentional asymmetry. A 3-column Bento grid should have one column significantly wider than the others to create an editorial focus.
*   **Do** use `primary` sparingly. It is a "laser pointer"—only use it where the eye *must* go first.
*   **Do** leverage the Spacing Scale strictly. Every gap must be a multiple of the system's core units to maintain the "engineered" feel.

### Don't:
*   **Don't** use any rounded corners. Even a 2px radius breaks the "Terminal" immersion.
*   **Don't** use 100% white (`#ffffff`) for body text. Use `on-surface-variant` (`#adaaaa`) to reduce eye strain and maintain a premium, subdued atmosphere.
*   **Don't** use standard "Drop Shadows." If the surface color change isn't enough, your hierarchy needs restructuring, not a shadow.