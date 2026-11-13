# CSS Fundamentals: Units and Mathematical Functions

## 1. CSS Measurement Units

### Absolute Units
- **`px` (Pixels)**: 1px = 1/96th of an inch. Precise for borders, shadows, and fine-grained icons. Avoid for root typography.

### Relative Units
| Unit | Relative To | Primary Use Case |
|---|---|---|
| **`rem`** | Root font size (`<html>` element default 16px) | Typography, component spacing, padding, margins |
| **`em`** | Direct parent element font size | Contextual button padding (scales with button font size) |
| **`%`** | Parent container's corresponding dimension | Flexible column widths, progress bars |
| **`ch`** | Width of the character '0' in the current font | Optimal body paragraph line-length (`max-width: 65ch;`) |
| **`vw` / `vh`** | 1% of viewport width / height | Fullscreen hero layouts, overlay backdrops |
| **`dvh` / `dvw`** | Dynamic viewport (accounts for mobile browser address bars) | Mobile full-height screens (`min-height: 100dvh;`) |
| **`cqw` / `cqh`** | 1% of query container width / height | Container-query responsive components |

---

## 2. Mathematical Functions

### `calc()`
Performs dynamic arithmetic calculations across mixed unit types:
```css
.sidebar-layout {
  width: calc(100% - 280px);
  margin-left: 280px;
}
```

### `min()` and `max()`
- `min(value1, value2, ...)`: Chooses the smallest value.
  ```css
  /* Width is 100% on small screens, but caps at 600px on desktop */
  .modal-dialog {
    width: min(100% - 2rem, 600px);
  }
  ```
- `max(value1, value2, ...)`: Chooses the largest value.
  ```css
  /* Ensures padding is at least 1rem even on narrow devices */
  .container {
    padding: max(1rem, 4vw);
  }
  ```

### `clamp()` (Fluid Typography & Fluid Spacing)
Syntax: `clamp(MIN, PREFERRED, MAX)`
```css
/* Fluid heading: min 1.75rem (28px), scales with 4vw, max 3.5rem (56px) */
h1 {
  font-size: clamp(1.75rem, 1rem + 3.5vw, 3.5rem);
}

/* Fluid responsive section padding */
.section {
  padding-block: clamp(2.5rem, 5vw, 6rem);
}
```
