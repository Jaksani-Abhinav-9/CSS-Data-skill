# CSS Responsive Design: Media Queries and Breakpoints

## 1. Mobile-First vs Desktop-First Strategy

- **Mobile-First (`min-width`) — Recommended Best Practice**:
  Base styles target mobile devices; media queries progressively enhance the layout for larger viewports.
  ```css
  /* Base: Mobile (1 column) */
  .grid-layout {
    display: grid;
    grid-template-columns: 1fr;
    gap: 1rem;
  }

  /* Tablet: >= 768px (2 columns) */
  @media (min-width: 768px) {
    .grid-layout {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  /* Desktop: >= 1024px (3 columns) */
  @media (min-width: 1024px) {
    .grid-layout {
      grid-template-columns: repeat(3, 1fr);
    }
  }
  ```

---

## 2. Standard Industry Breakpoint Matrix

| Token | Min Width | Target Device Category |
|---|---|---|
| `sm` | `640px` | Large phones / Landscape orientation |
| `md` | `768px` | Tablets (portrait) |
| `lg` | `1024px` | Tablets (landscape) / Laptops |
| `xl` | `1280px` | Standard Desktops |
| `2xl` | `1536px` | Wide Displays / High-res monitors |

---

## 3. Media Features Beyond Viewport Width

### Dark / Light Mode Detection
```css
@media (prefers-color-scheme: dark) {
  :root {
    --bg-primary: #0f172a;
    --text-primary: #f8fafc;
  }
}
```

### Accessibility: Reduced Motion
```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

### Pointer Precision & Hover Capability
```css
/* Touch devices with no hover */
@media (hover: none) and (pointer: coarse) {
  .btn, .nav-link {
    min-height: 48px; /* Enforce touch target size */
  }
}
```

### Print Stylesheet
```css
@media print {
  body { background: white; color: black; }
  .no-print, .nav, .sidebar { display: none !important; }
}
```
