# CSS Accessibility: WCAG 2.1 AA Compliance and Accessible Styling

## 1. WCAG 2.1 Contrast Standards

| Level | Normal Text (< 18pt / < 14pt bold) | Large Text (>= 18pt / >= 14pt bold) | UI Components & Graphical Objects |
|---|---|---|---|
| **AA (Standard Compliance)** | **4.5 : 1** | **3.0 : 1** | **3.0 : 1** |
| **AAA (Enhanced Compliance)** | **7.0 : 1** | **4.5 : 1** | **4.5 : 1** |

---

## 2. Touch Target Minimum Sizes (Mobile & Coarse Pointer)
WCAG 2.5.5 and Apple/Google HIG dictate that all interactive elements must provide a minimum clickable/tappable bounding box:

- **Minimum Size**: **44px $\times$ 44px** (or 48px $\times$ 48px for Android).

```css
.btn-icon, .touch-target {
  min-width: 44px;
  min-height: 44px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
}
```

---

## 3. Visually Hidden Screen Reader Pattern (`.sr-only`)
Hides content visually from sighted users while keeping it fully accessible to screen readers:

```css
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}
```

---

## 4. Skip to Main Content Link
Essential for keyboard and screen reader accessibility:

```css
.skip-link {
  position: absolute;
  top: -999px;
  left: 1rem;
  z-index: 1000;
  background: var(--accent-primary);
  color: #ffffff;
  padding: 0.75rem 1.5rem;
  border-radius: var(--radius-md);
  text-decoration: none;
  font-weight: 700;
}

.skip-link:focus {
  top: 1rem;
}
```
