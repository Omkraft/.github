# Omkraft Inc. — Brand Guidelines

This document defines the **official, locked brand assets and usage rules**
for **Omkraft Inc.**  

These guidelines exist to ensure **visual consistency, clarity, and long-term
brand integrity** across all repositories, applications, and documents.

> **Systems, Crafted.**

---

## 1. Brand Identity

- **Official Name:** Omkraft Inc.
- **Short Name (technical use):** Omkraft
- **Tagline:** *Systems, Crafted.*
- **Tone:** Calm, precise, engineered, intentional
- **Design Philosophy:** Minimal, functional, non-trendy

---

## 2. Canonical Logo Files

The following logo files are **authoritative** and must not be modified.

`logo-primary.svg`
`logo-secondary.svg`


### Logo Types

| File | Usage |
|----|----|
| `logo-primary.svg` | Default logo (light background) |
| `logo-secondary.svg` | Dark background / dark UI |

No other logo files should redefine geometry, text, or proportions.

---

## 3. Logo Construction (Locked)

The Omkraft logo consists of:
- The Omkraft icon (SVG path)
- Brand text: **Omkraft Inc.**
- Tagline: *Systems, Crafted.*

### Typography Rules (Strict)

| Text | Weight | Style |
|----|----|----|
| Omkraft | **Bold** | Normal |
| Inc. | Regular | Normal |
| Systems, Crafted. | Regular | *Italic* |

### Font Stack (Apple-first)

```css
-apple-system,
BlinkMacSystemFont,
"SF Pro Display",
"SF Pro Text",
"Helvetica Neue",
Arial,
sans-serif
```

No custom fonts are to be embedded in logo SVGs.

---

## 4. Color Palette (Locked)
### Primary Colors
| Name           | Hex       |
| -------------- | --------- |
| Primary Blue   | `#3A98F1` |
| Accent Mint    | `#4EF2C2` |
| Navy (Dark BG) | `#0B1C3D` |
| Text Navy      | `#0E2A4D` |
| White          | `#FFFFFF` |

### Usage Rules
- Icon colors **must not be altered**
- Text color:
    - Light background → Text Navy
    - Dark background → White
- No gradients, shadows, or opacity effects

---

## 5. Background Usage
| Background    | Logo                 |
| ------------- | -------------------- |
| Light / White | `logo-primary.svg`   |
| Dark / Navy   | `logo-secondary.svg` |

Do **not** place logos on:
- Busy images
- Low-contrast backgrounds
- Gradients

---

## 6. Spacing & Clear Space
- Maintain clear space around the logo equal to the **height of the icon**
- Logo must never touch edges of containers
- Do not crowd with UI elements or text

---

## 7. Scaling Rules
- SVG logos may be scaled **uniformly only**
- Do not stretch horizontally or vertically
- Minimum recommended widths:
    - Header: `200px`
    - Avatar: `64px`
    - Footer: `120px`

---

## 8. Do Not (Very Important)
❌ Do not redraw the icon
❌ Do not simplify or optimize SVG paths with lossy tools
❌ Do not change text wording or capitalization
❌ Do not alter spacing or proportions
❌ Do not add effects (shadow, glow, outline)
❌ Do not substitute fonts

If a new size or format is required, **wrap or scale the existing SVG**.

---

## 9. Repository Usage
Recommended structure:
```pgsql
.github/
├── logo-primary.svg
├── logo-secondary.svg
└── BRAND.md
```
All repositories should reference these assets instead of copying or redefining them.

---

## 10. Governance
Any change to:
- Logo geometry
- Typography
- Colors
- Tagline

**Requires explicit review and approval.**

The brand is considered **locked** by default.

---

## 11. Brand Statement
Omkraft Inc. builds systems with intent.
Every design choice favors clarity, structure, and long-term maintainability.

**Systems, Crafted.**