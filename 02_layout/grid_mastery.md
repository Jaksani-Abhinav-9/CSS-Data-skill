# CSS Layout: CSS Grid Mastery

## 1. 2D Layout Model
CSS Grid provides a two-dimensional grid-based layout system with rows and columns simultaneously.

```
       Column 1        Column 2        Column 3
   +---------------+---------------+---------------+
   |               |               |               |  Row 1
   +---------------+---------------+---------------+
   |               |               |               |  Row 2
   +---------------+---------------+---------------+
```

---

## 2. Container Properties

| Property | Values | Purpose |
|---|---|---|
| `display` | `grid` \| `inline-grid` | Activates grid formatting context |
| `grid-template-columns` | `<track-size>+` (e.g. `250px 1fr 1fr`, `repeat(3, 1fr)`) | Defines column track sizes |
| `grid-template-rows` | `<track-size>+` (e.g. `auto 1fr auto`) | Defines row track sizes |
| `grid-template-areas` | Strings naming cell areas | Visually maps semantic layout areas |
| `gap` | `row-gap [column-gap]` | Sets gutters between rows and columns |
| `justify-items` | `start` \| `center` \| `end` \| `stretch` | Horizontal alignment of cell items |
| `align-items` | `start` \| `center` \| `end` \| `stretch` | Vertical alignment of cell items |

---

## 3. Essential Grid Functions and Keywords

### Fractional Unit (`fr`)
Represents a fraction of the available free space:
```css
/* Sidebar 260px, Content takes remaining space */
.app-layout {
  display: grid;
  grid-template-columns: 260px 1fr;
}
```

### `repeat()` with `minmax()` and `auto-fit` (The Holy Grail Responsive Grid)
Creates a fully responsive grid **without media queries**:
```css
.responsive-cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
}
```
- `auto-fit`: Stretches existing items to fill the row when space permits.
- `auto-fill`: Keeps empty column tracks when space is available.

---

## 4. Named Grid Areas Architecture
```css
.dashboard-layout {
  display: grid;
  grid-template-columns: 240px 1fr;
  grid-template-rows: 60px 1fr 50px;
  grid-template-areas:
    "sidebar header"
    "sidebar main"
    "sidebar footer";
  min-height: 100vh;
}

.sidebar { grid-area: sidebar; }
.header  { grid-area: header; }
.main    { grid-area: main; }
.footer  { grid-area: footer; }
```

---

## 5. CSS Subgrid
Allows child grid items to inherit and align directly to their parent grid tracks:
```css
.card {
  display: grid;
  grid-row: span 3;
  grid-template-rows: subgrid; /* Header, Body, Footer align across all sibling cards */
}
```
