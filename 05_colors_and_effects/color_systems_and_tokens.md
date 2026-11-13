# CSS Colors & Visual Effects: Color Systems and Semantic Tokens

## 1. CSS Color Formats

| Format | Syntax | Best Use Case |
|---|---|---|
| **Hex** | `#ff5500`, `#0f172a` | Static legacy color definitions |
| **RGB / RGBA** | `rgb(255 85 0 / 0.8)` | Alpha transparency with RGB channels |
| **HSL** | `hsl(215 25% 15% / 0.9)` | Predictable saturation and lightness adjustments |
| **OKLCH (Modern)** | `oklch(0.65 0.24 35)` | Perceptually uniform color spaces (prevents muddy gradient transitions) |
| **`color-mix()`** | `color-mix(in srgb, var(--primary) 80%, black)` | Dynamic tinting and shading directly in CSS |

---

## 2. 3-Tier Semantic Token Architecture

```
[Primitive Tokens]       [Semantic Tokens]           [Component Tokens]
--color-slate-900  --->  --bg-primary           --->  --card-bg
--color-orange-500 --->  --accent-primary       --->  --btn-primary-bg
--color-slate-400  --->  --text-muted           --->  --input-placeholder
```

### Semantic Token Scale
```css
:root {
  /* Surface & Backgrounds */
  --bg-app: #090a0d;
  --bg-surface: #12141a;
  --bg-card: #181b24;
  --bg-elevated: #222634;

  /* Text & Content */
  --text-primary: #f8fafc;
  --text-secondary: #94a3b8;
  --text-muted: #64748b;
  --text-inverse: #090a0d;

  /* Brand Accents */
  --accent-primary: #ff5500;
  --accent-hover: #ff6a00;
  --accent-subtle: rgba(255, 85, 0, 0.12);
  --accent-glow: rgba(255, 85, 0, 0.35);

  /* Status Colors */
  --status-success: #10b981;
  --status-warning: #f59e0b;
  --status-error: #ef4444;
  --status-info: #3b82f6;

  /* Borders & Dividers */
  --border-subtle: rgba(255, 255, 255, 0.08);
  --border-default: #2a2e3d;
  --border-focus: #ff5500;
}
```
