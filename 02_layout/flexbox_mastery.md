# CSS Layout: Flexbox Mastery

## 1. Flex Container vs Flex Items
When `display: flex` or `display: inline-flex` is applied to a parent, all direct children become **flex items**.

```
             MAIN AXIS (flex-direction: row)
   ---------------------------------------------------->
  +-----------------------------------------------------+ ^
  |  +------------+   +------------+   +------------+  | | CROSS
  |  |  Item 1    |   |  Item 2    |   |  Item 3    |  | | AXIS
  |  +------------+   +------------+   +------------+  | |
  +-----------------------------------------------------+ v
```

---

## 2. Container Properties

| Property | Values | Purpose |
|---|---|---|
| `flex-direction` | `row` (default) \| `row-reverse` \| `column` \| `column-reverse` | Sets the direction of the main axis |
| `flex-wrap` | `nowrap` (default) \| `wrap` \| `wrap-reverse` | Controls whether items wrap onto multiple lines |
| `justify-content` | `flex-start` \| `center` \| `flex-end` \| `space-between` \| `space-around` \| `space-evenly` | Aligns items along the **main axis** |
| `align-items` | `stretch` (default) \| `flex-start` \| `center` \| `flex-end` \| `baseline` | Aligns items along the **cross axis** |
| `align-content` | `stretch` \| `flex-start` \| `center` \| `flex-end` \| `space-between` | Aligns multi-line tracks when wrap occurs |
| `gap` | `<length>` (e.g. `1rem`, `16px 24px`) | Sets gutters between items without margins |

---

## 3. Item Properties

| Property | Values | Purpose |
|---|---|---|
| `flex-grow` | `<number>` (default `0`) | Ability for an item to grow if extra space is available |
| `flex-shrink` | `<number>` (default `1`) | Ability for an item to shrink if space is insufficient |
| `flex-basis` | `<length>` \| `auto` (default `auto`) | Default size of an item before space distribution |
| `flex` (shorthand) | `flex: grow shrink basis;` | Common presets: `flex: 1` (1 1 0%), `flex: auto` (1 1 auto), `flex: none` (0 0 auto) |
| `align-self` | `auto` \| `flex-start` \| `center` \| `flex-end` \| `stretch` | Overrides container `align-items` for a specific item |
| `order` | `<integer>` (default `0`) | Controls visual presentation order without modifying DOM |

---

## 4. Common Production Recipes

### A. Perfect Centering (Horizontal & Vertical)
```css
.center-box {
  display: flex;
  align-items: center;
  justify-content: center;
}
```

### B. Navbar / App Header
```css
.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 2rem;
  gap: 1.5rem;
}
```

### C. Sticky Footer Card
```css
.card {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.card-body {
  flex: 1; /* Pushes footer to bottom */
}
```
