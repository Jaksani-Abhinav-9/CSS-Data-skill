# CSS Animations & Motion: Transitions and Hardware-Accelerated Transforms

## 1. CSS Transitions
Transitions smoothly interpolate property changes between two states:

```css
.interactive-element {
  /* transition: property duration timing-function delay */
  transition: transform 0.2s cubic-bezier(0.4, 0, 0.2, 1),
              box-shadow 0.2s cubic-bezier(0.4, 0, 0.2, 1),
              background-color 0.15s ease;
}
```

### High-Performance vs Low-Performance Properties
- **High-Performance (GPU Composite Only — 60/120 FPS)**:
  - `transform` (`translate`, `scale`, `rotate`, `skew`)
  - `opacity`
  - `filter` / `backdrop-filter`
- **Low-Performance (Triggers Layout / Paint Reflow — Avoid Animating)**:
  - `width`, `height`, `top`, `left`, `margin`, `padding`, `border-width`

---

## 2. 2D & 3D CSS Transforms

| Transform Function | Description | Example |
|---|---|---|
| `translate(x, y)` | Moves element along X and Y axes | `transform: translateY(-4px);` |
| `scale(factor)` | Resizes element visually without affecting document flow | `transform: scale(1.03);` |
| `rotate(deg)` | Rotates element clockwise | `transform: rotate(45deg);` |
| `translate3d(x, y, z)` | Forces GPU hardware acceleration | `transform: translate3d(0, 0, 0);` |

---

## 3. Production Easing Functions (Cubic-Bezier Curves)
```css
:root {
  /* Natural Spring / Snappy Hover */
  --ease-spring: cubic-bezier(0.175, 0.885, 0.32, 1.275);

  /* Standard Material Emphasized Easing */
  --ease-emphasized: cubic-bezier(0.2, 0, 0, 1);

  /* Smooth Exit */
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
}
```
