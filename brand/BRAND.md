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

### Red ramp

```css
--omkraft-red-50:  #fdecec;
--omkraft-red-100: #f9d0d0;
--omkraft-red-200: #f1a3a3;
--omkraft-red-300: #e77676;
--omkraft-red-400: #df4c4c;
--omkraft-red-500: #dc2626;
--omkraft-red-600: #c41f1f;
--omkraft-red-700: #a01818;
--omkraft-red-800: #7d1212;
--omkraft-red-900: #5a0c0c;
```

### Amber ramp

```css
--omkraft-amber-50:  #fffbeb;
--omkraft-amber-100: #fef3c7;
--omkraft-amber-200: #fde68a;
--omkraft-amber-300: #fcd34d;
--omkraft-amber-400: #fbbf24;
--omkraft-amber-500: #f59e0b;
--omkraft-amber-600: #d97706;
--omkraft-amber-700: #b45309;
--omkraft-amber-800: #92400e;
--omkraft-amber-900: #78350f;
```

### Yellow ramp

```css
--omkraft-yellow-50:  #fefce8;
--omkraft-yellow-100: #fef9c3;
--omkraft-yellow-200: #fef08a;
--omkraft-yellow-300: #fde047;
--omkraft-yellow-400: #facc15;
--omkraft-yellow-500: #eab308;
--omkraft-yellow-600: #ca8a04;
--omkraft-yellow-700: #a16207;
--omkraft-yellow-800: #854d0e;
--omkraft-yellow-900: #713f12;
```

### Orange ramp

```css
--omkraft-orange-50:  #fff7ed;
--omkraft-orange-100: #ffedd5;
--omkraft-orange-200: #fed7aa;
--omkraft-orange-300: #fdba74;
--omkraft-orange-400: #fb923c;
--omkraft-orange-500: #f97316;
--omkraft-orange-600: #ea580c;
--omkraft-orange-700: #c2410c;
--omkraft-orange-800: #9a3412;
--omkraft-orange-900: #7c2d12;
```

### Indigo ramp

```css
--omkraft-indigo-50:  #eef2ff;
--omkraft-indigo-100: #e0e7ff;
--omkraft-indigo-200: #c7d2fe;
--omkraft-indigo-300: #a5b4fc;
--omkraft-indigo-400: #818cf8;
--omkraft-indigo-500: #6366f1;
--omkraft-indigo-600: #4f46e5;
--omkraft-indigo-700: #4338ca;
--omkraft-indigo-800: #3730a3;
--omkraft-indigo-900: #312e81;
```

---

## 7. Surface and Status Colors

```css
--omkraft-surface-1: rgba(255, 255, 255, 0.04);
--omkraft-surface-2: rgba(255, 255, 255, 0.06);
--omkraft-surface-3: rgba(255, 255, 255, 0.08);
--omkraft-surface-4: rgba(255, 255, 255, 0.12);

--omkraft-border-subtle: rgba(255, 255, 255, 0.16);
--omkraft-border-default: rgba(255, 255, 255, 0.22);
--omkraft-border-strong: rgba(255, 255, 255, 0.32);

--destructive: var(--omkraft-red-500);
--destructive-bg: var(--omkraft-red-500);
--destructive-hover: var(--omkraft-red-600);
--destructive-foreground: #ffffff;

--info-bg: var(--omkraft-blue-100);
--info-border: var(--omkraft-blue-800);
--info-foreground: var(--omkraft-blue-800);

--warning-bg: var(--omkraft-amber-100);
--warning-border: var(--omkraft-amber-800);
--warning-foreground: var(--omkraft-amber-800);

--success-bg: var(--omkraft-mint-100);
--success-border: var(--omkraft-mint-800);
--success-foreground: var(--omkraft-mint-800);
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
