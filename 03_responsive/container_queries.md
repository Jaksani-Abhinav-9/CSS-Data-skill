# CSS Responsive Design: Container Queries

## 1. Why Container Queries?
Traditional media queries evaluate the **entire viewport width**. When a component (like a product card) is placed inside a narrow sidebar or a wide hero section, viewport media queries fail to adapt it based on its immediate available container width.

**Container queries** allow components to adapt according to the width of their **direct parent container**.

---

## 2. Defining a Container
```css
.card-wrapper {
  container-type: inline-size; /* Tracks width */
  container-name: card-container;
}
```
- `container-type: inline-size`: Monitors horizontal dimension changes (most common).
- `container-type: size`: Monitors both horizontal and vertical dimension changes.
- `container-type: normal`: Creates a query container for style queries only.

---

## 3. Querying the Container
```css
/* Base: Single-column vertical stacked card */
.product-card {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

/* When the parent container is >= 500px wide, switch card to horizontal layout */
@container card-container (min-width: 500px) {
  .product-card {
    flex-direction: row;
    align-items: center;
  }

  .product-card img {
    width: 180px;
    height: 180px;
  }
}
```

---

## 4. Container Query Units
Container query units provide relative measurements based on container dimensions:
- `1cqw`: 1% of query container's width.
- `1cqh`: 1% of query container's height.
- `1cqi`: 1% of query container's inline size.
- `1cqb`: 1% of query container's block size.
- `1cqmin` / `1cqmax`: 1% of smaller / larger container dimension.

```css
.card-title {
  font-size: clamp(1rem, 4cqi, 1.75rem);
}
```
