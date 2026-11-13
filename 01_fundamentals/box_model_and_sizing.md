# CSS Fundamentals: Box Model and Sizing

## 1. Standard Box Model Architecture
Every rendered HTML element is treated as a rectangular box comprising 4 concentric zones:

```
+-------------------------------------------------+
|                   MARGIN                        |
|  +-------------------------------------------+  |
|  |                BORDER                     |  |
|  |  +-------------------------------------+  |  |
|  |  |             PADDING                 |  |  |
|  |  |  +-------------------------------+  |  |  |
|  |  |  |           CONTENT             |  |  |  |
|  |  |  |    (width x height)           |  |  |  |
|  |  |  +-------------------------------+  |  |  |
|  |  +-------------------------------------+  |  |
|  +-------------------------------------------+  |
+-------------------------------------------------+
```

---

## 2. `box-sizing: border-box` vs `content-box`

| Box Model Type | Formula for Total Rendered Width | Production Usage |
|---|---|---|
| `content-box` (Browser default) | `width + padding-left + padding-right + border-left + border-right` | Causes unexpected element overflows when padding is added |
| `border-box` (**Standard Best Practice**) | `width` (Padding and border are absorbed inside the declared width) | Universal standard for predictable, responsive layouts |

### Universal Box-Sizing Reset
```css
*, *::before, *::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
```

---

## 3. Margin Collapsing
Vertical margins between adjacent sibling block elements collapse into a single margin equal to the larger of the two margins:
- `elementA { margin-bottom: 30px; }`
- `elementB { margin-top: 20px; }`
- **Resulting rendered vertical gap**: `30px` (NOT `50px`).

### How to Prevent Unwanted Margin Collapsing:
1. Use **Flexbox** or **Grid** with the `gap` property (modern best practice).
2. Add `padding: 1px 0` or a border to the parent container.
3. Set `display: flow-root` on the parent to create a new Block Formatting Context (BFC).

---

## 4. Sizing Properties and Constraints

- **`width` / `height`**: Absolute or relative base dimensions.
- **`min-width` / `max-width`**: Prevents elements from shrinking below or expanding beyond specified thresholds (e.g. `max-width: 1200px; margin: 0 auto;`).
- **`min-height` / `max-height`**: Ensures vertical containers accommodate dynamic content while establishing viewport bounds (e.g. `min-height: 100vh;`).
- **`aspect-ratio`**: Enforces strict aspect ratio constraints without requiring padding hacks:
  ```css
  .video-card {
    width: 100%;
    aspect-ratio: 16 / 9;
    object-fit: cover;
  }
  ```
- **`overflow`**: Controls content clipping and scrolling (`visible`, `hidden`, `scroll`, `auto`, `clip`).
  - `overflow-x: hidden; overflow-y: auto;`
