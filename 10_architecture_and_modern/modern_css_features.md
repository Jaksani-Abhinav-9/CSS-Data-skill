# Modern CSS: Native Nesting, Cascade Layers, and Modern Functions

## 1. Native CSS Nesting (CSS Nesting Module Level 1)
Modern CSS supports native nesting directly in all evergreen browsers without preprocessors (Sass/Less):

```css
.card {
  background: var(--bg-card);
  padding: 1.5rem;
  border-radius: var(--radius-lg);

  /* Direct child nesting */
  h3 {
    font-size: 1.25rem;
    margin-bottom: 0.5rem;
  }

  /* Ampersand for pseudo-classes */
  &:hover {
    transform: translateY(-2px);
    box-shadow: var(--shadow-md);
  }

  /* Ampersand for BEM modifiers */
  &.is-active {
    border-color: var(--accent-primary);
  }

  /* Media query nesting */
  @media (min-width: 768px) {
    padding: 2.5rem;
  }
}
```

---

## 2. `@property` Rule (CSS Typed OM & Animatable Custom Properties)
Allows explicit type definitions for custom properties so they can be smoothly animated in keyframes:

```css
@property --gradient-angle {
  syntax: '<angle>';
  initial-value: 0deg;
  inherits: false;
}

@keyframes rotateGradient {
  to {
    --gradient-angle: 360deg;
  }
}

.animated-border {
  background: conic-gradient(from var(--gradient-angle), #ff5500, #38bdf8, #ff5500);
  animation: rotateGradient 4s linear infinite;
}
```

---

## 3. CSS Logical Properties (Internationalization / RTL Support)
Replaces physical directional properties (`left`/`right`/`top`/`bottom`) with writing-mode-aware logical properties:

| Physical Property | Modern Logical Equivalent |
|---|---|
| `margin-left` / `margin-right` | `margin-inline-start` / `margin-inline-end` (or `margin-inline`) |
| `margin-top` / `margin-bottom` | `margin-block-start` / `margin-block-end` (or `margin-block`) |
| `padding-left` / `padding-right` | `padding-inline` |
| `padding-top` / `padding-bottom` | `padding-block` |
| `width` / `height` | `inline-size` / `block-size` |
| `border-left` | `border-inline-start` |
