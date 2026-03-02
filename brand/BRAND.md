# Omkraft Inc. - Brand Guidelines

This document defines the official, locked brand assets and design tokens for Omkraft Inc.

These guidelines ensure visual consistency, accessibility, and long-term brand integrity across repositories, apps, and documentation.

> _Systems, Crafted._

---

## 1. Brand Identity

- Official Name: Omkraft Inc.
- Short Name (technical use): Omkraft
- Tagline: _Systems, Crafted._
- Tone: Calm, precise, engineered, intentional
- Design Philosophy: Minimal, functional, durable

---

## 2. Canonical Logo Files (Locked)

### Source logos (`brand/`)

```text
brand/logo-primary.svg
brand/logo-secondary.svg
brand/logo-small.svg
```

### Distribution logos (`assets/`)

```text
assets/logo-primary-horizontal.svg
assets/logo-primary-square.svg
assets/logo-secondary-horizontal.svg
assets/logo-secondary-square.svg
assets/logo-small.svg
```

The brand files above are authoritative and must not be modified without explicit approval.

---

## 3. Logo Usage

| File | Usage |
| --- | --- |
| `logo-primary.svg` / `logo-primary-horizontal.svg` | Light backgrounds |
| `logo-secondary.svg` / `logo-secondary-horizontal.svg` | Dark backgrounds |
| `logo-small.svg` | Favicon, compact headers, badges |
| `*-square.svg` | Avatars, cards, social previews |

No logo may redefine geometry, text, spacing, or proportions.

---

## 4. Typography System

### UI Typeface

Inter is the official Omkraft UI font.

```css
font-family:
  'Inter',
  system-ui,
  -apple-system,
  BlinkMacSystemFont,
  'Segoe UI',
  Roboto,
  Arial,
  sans-serif;
```

- Use Inter across UI and docs.
- System fonts are fallback only.
- Logo typography stays locked in the SVG assets.

---

## 5. Core Brand Colors (Locked)

| Token | Hex |
| --- | --- |
| Omkraft Blue (Primary) | `#305AF3` |
| Omkraft Mint (Accent) | `#00AD97` |
| Omkraft Navy (Background) | `#041459` |
| Omkraft White | `#FFFFFF` |

---

## 6. Extended Color Palette

### Blue ramp

```css
--omkraft-blue-50:  #eef2ff;
--omkraft-blue-100: #dfe6ff;
--omkraft-blue-200: #bcc9ff;
--omkraft-blue-300: #91a6ff;
--omkraft-blue-400: #5e7df8;
--omkraft-blue-500: #305af3;
--omkraft-blue-600: #274bda;
--omkraft-blue-700: #203eb6;
--omkraft-blue-800: #1c348f;
--omkraft-blue-900: #16286b;
```

### Mint ramp

```css
--omkraft-mint-50:  #e6fbf7;
--omkraft-mint-100: #c9f3eb;
--omkraft-mint-200: #9be6d8;
--omkraft-mint-300: #63d5c3;
--omkraft-mint-400: #2fc0ad;
--omkraft-mint-500: #00ad97;
--omkraft-mint-600: #00937f;
--omkraft-mint-700: #007768;
--omkraft-mint-800: #005c50;
--omkraft-mint-900: #00453c;
```

### Navy ramp

```css
--omkraft-navy-50:  #e9ecf5;
--omkraft-navy-100: #cfd6ea;
--omkraft-navy-200: #a3afd8;
--omkraft-navy-300: #7387c3;
--omkraft-navy-400: #4b63a8;
--omkraft-navy-500: #041459;
--omkraft-navy-600: #03124e;
--omkraft-navy-700: #020f41;
--omkraft-navy-800: #020c35;
--omkraft-navy-900: #010826;
```

---

## 7. Surface and Status Colors

```css
--surface-1: rgba(255, 255, 255, 0.04);
--surface-2: rgba(255, 255, 255, 0.06);
--surface-3: rgba(255, 255, 255, 0.08);
--surface-4: rgba(255, 255, 255, 0.12);

--border-subtle: rgba(255, 255, 255, 0.16);
--border-default: rgba(255, 255, 255, 0.22);
--border-strong: rgba(255, 255, 255, 0.32);

--destructive: #dc2626;
--destructive-bg: rgba(220, 38, 38, 0.12);
--destructive-hover: rgba(220, 38, 38, 0.18);
```

---

## 8. Do Not (Strict)

❌ Redraw or simplify SVG paths

❌ Change proportions or spacing

❌ Alter colors inside logo SVGs

❌ Add gradients/shadows/effects to logo files

❌ Substitute typography inside logo assets

If a different size is needed, scale existing SVGs uniformly.

---

## 9. Repository Usage

```text
.github/
|-- brand/
|   |-- logo-primary.svg
|   |-- logo-secondary.svg
|   |-- logo-small.svg
|   `-- BRAND.md
|-- assets/
|   |-- logo-primary-horizontal.svg
|   |-- logo-primary-square.svg
|   |-- logo-secondary-horizontal.svg
|   |-- logo-secondary-square.svg
|   `-- logo-small.svg
```

---

## 10. Governance

Changes to logos, typography, core colors, or tagline require explicit review and approval.

The Omkraft brand is locked by default.

---

## 11. Brand Statement

Omkraft Inc. builds systems with intent.

Every design choice favors clarity, structure, and long-term maintainability.

_Systems, Crafted._
