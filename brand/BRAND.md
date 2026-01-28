# Omkraft Inc. — Brand Guidelines

This document defines the **official, locked brand assets and design tokens**
for **Omkraft** Inc.

These guidelines exist to ensure **visual consistency, accessibility, and
long-term brand integrity** across all repositories, applications, and
documents.

> _Systems, Crafted._

---

## 1. Brand Identity

- **Official Name: Omkraft** Inc.
- **Short Name (technical use):** Omkraft
- **Tagline:** *Systems, Crafted.*
- **Tone:** Calm, precise, engineered, intentional
- **Design Philosophy:** Minimal, functional, non-trendy, durable

---

## 2. Canonical Logo Files (Locked)

The following logo files are **authoritative** and must not be modified.

```yaml
logo-primary.svg
logo-secondary.svg
logo-small.svg
```


### Logo Types

<table>
  <thead>
    <tr>
      <th align="left">File</th>
      <th align="left">Usage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>logo-primary.svg</code></td>
      <td>Light backgrounds</td>
    </tr>
    <tr>
      <td><code>logo-secondary.svg</code></td>
      <td>Dark backgrounds / dark UI</td>
    </tr>
    <tr>
      <td><code>logo-small.svg</code></td>
      <td>Favicons, compact headers</td>
    </tr>
  </tbody>
</table>

No logo may redefine geometry, text, spacing, or proportions.

---

## 3. Logo Construction (Strictly Locked)

The Omkraft logo consists of:
- Omkraft icon (SVG paths)
- Brand text: **Omkraft Inc.**
- Tagline: *Systems, Crafted.*

### Typography Rules (Logo Only)

<table>
  <thead>
    <tr>
      <th align="left">Element</th>
      <th align="left">Weight</th>
      <th align="left">Style</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Omkraft</td>
      <td><strong>Bold</strong></td>
      <td>Normal</td>
    </tr>
    <tr>
      <td>Inc.</td>
      <td>Regular</td>
      <td>Normal</td>
    </tr>
    <tr>
      <td>Systems, Crafted.</td>
      <td>Regular</td>
      <td><em>Italic</em></td>
    </tr>
  </tbody>
</table>

⚠️ Logo SVGs must **not embed custom fonts**.

---

## 4. Typography System (UI & Product)

### Primary UI Typeface

**Inter** is the official Omkraft UI font.

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

- Inter is used for **all UI, dashboards, apps, and documentation**
- System fonts act only as fallbacks
- Logo typography remains font-agnostic

---

## 5. Brand Color Palette (Authoritative)

### Core Brand Colors (Locked)

<table>
  <thead>
    <tr>
      <th align="left">Token</th>
      <th align="left">Hex</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Omkraft Blue (Primary)</td>
      <td><code>#305AF3</code></td>
    </tr>
    <tr>
      <td>Omkraft Mint (Accent)</td>
      <td><code>#00AD97</code></td>
    </tr>
    <tr>
      <td>Omkraft Navy (Background)</td>
      <td><code>#041459</code></td>
    </tr>
    <tr>
      <td>Omkraft White</td>
      <td><code>#FFFFFF</code></td>
    </tr>
  </tbody>
</table>

These values define **brand identity** and must not be altered without review.

---

## 6. Extended Color Palette (UI System)

Approved tonal ramps derived from core brand colors.

Used for accessibility, hover states, elevation, and UI hierarchy.

### Blue (Primary Ramp)

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

### Mint (Accent Ramp)

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

### Navy (Background Ramp)

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

## 7. Neutral & Surface Colors

Used for cards, inputs, borders, overlays, and elevation.

```css
--surface-1: rgba(255, 255, 255, 0.04);
--surface-2: rgba(255, 255, 255, 0.06);
--surface-3: rgba(255, 255, 255, 0.08);
--surface-4: rgba(255, 255, 255, 0.12);

--border-subtle: rgba(255, 255, 255, 0.16);
--border-default: rgba(255, 255, 255, 0.22);
--border-strong: rgba(255, 255, 255, 0.32);
```

---

## 8. Destructive & Status Colors

Calm, non-alarming, and accessible.

```css
--destructive: #dc2626;
--destructive-bg: rgba(220, 38, 38, 0.12);
--destructive-hover: rgba(220, 38, 38, 0.18);
```

---

## 9. Logo Background Usage

<table>
  <thead>
    <tr>
      <th align="left">Background</th>
      <th align="left">Logo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Light / White</td>
      <td><code>logo-primary.svg</code></td>
    </tr>
    <tr>
      <td>Dark / Navy</td>
      <td><code>logo-secondary.svg</code></td>
    </tr>
  </tbody>
</table>

❌ Do not place logos on:

- Gradients
- Busy imagery
- Low-contrast surfaces

---

## 10. Spacing & Clear Space

- Minimum clear space = **height of the icon**
- Logos must never touch container edges
- Do not crowd with UI elements

---

## 11. Scaling Rules

- SVG logos may be scaled **uniformly only**
- No stretching or distortion
- Minimum widths:
    - Header: 200px
    - Avatar: 64px
    - Footer: 120px

---

## 12. Do Not (Strict)

❌ Redraw or simplify SVG paths

❌ Change proportions or spacing

❌ Alter colors inside logo SVGs

❌ Add gradients, shadows, or effects

❌ Substitute typography

If a new size is required, **wrap or scale the existing SVG**.

---

## 13. Repository Usage

Recommended structure:

```text
.github/
├── brand/
│   ├── logo-primary.svg
│   ├── logo-secondary.svg
│   ├── logo-small.svg
│   └── BRAND.md
```

All repositories must reference these assets instead of redefining them.

---

## 14. Governance

Any change to:
- Logos
- Typography
- Core colors
- Tagline

Requires **explicit review and approval**.

The Omkraft brand is **locked by default**.

---

## 15. Brand Statement

**Omkraft** Inc. builds systems with intent.

Every design choice favors clarity, structure, and long-term maintainability.

_Systems, Crafted._