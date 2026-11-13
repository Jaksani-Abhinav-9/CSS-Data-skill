# Flexbox & CSS Grid Mastery
Source Attribution: MDN Layout Specifications & Modern Web UI Standards

## 1. When to Use Flexbox vs CSS Grid
- **Use Flexbox**: 1-Dimensional layouts (navbars, button groups, icon + text rows, vertical form stacks, centered items).
- **Use CSS Grid**: 2-Dimensional layouts (pricing cards, product catalogs, dashboard KPI stats, image galleries).

## 2. Essential Flexbox Patterns
### A. Perfect Centering (Auth & Modal backdrops)
```css
.center-container {
  display: flex;
  align-items: center;
  justify-content: center;
}
```
### B. Navigation Split Bar (Brand on left, Menu on right)
```css
.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
```
### C. Auto-Push Flexbox Utilities (`margin-left: auto` / `margin-top: auto`)
```css
.card-body {
  display: flex;
  flex-direction: column;
}
.card-price-row {
  margin-top: auto; /* Pushes price/button to bottom regardless of variable description length */
}
```

## 3. Essential CSS Grid Patterns
### A. Responsive Auto-Fitting Grid (Zero Media Queries Needed)
```css
.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
}
```
### B. Dashboard 240px Fixed Sidebar + 1fr Fluid Content
```css
.dashboard-layout {
  display: grid;
  grid-template-columns: 260px 1fr;
  min-height: 100svh;
}
@media (max-width: 768px) {
  .dashboard-layout {
    grid-template-columns: 1fr;
  }
}
```
