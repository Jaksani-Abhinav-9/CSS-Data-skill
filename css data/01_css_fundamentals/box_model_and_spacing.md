# CSS Box Model, Spacing Scales & Modern Units
Source Attribution: MDN Web Docs & Modern CSS Design Systems

## 1. Box Model Foundation
```css
*, *::before, *::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
```
With `box-sizing: border-box`, `width` and `height` include padding and borders, preventing layout overflow breakage.

## 2. Modern Viewport Units (Avoid Mobile Jump)
- `100vh`: Classic viewport height (fails on mobile browsers when URL bar collapses).
- `100svh`: **Small Viewport Height** (accounts for visible URL bar on mobile).
- `100dvh`: **Dynamic Viewport Height** (smoothly scales with mobile URL bar expand/collapse).
- **Production Pattern**:
```css
.fullscreen-wrapper {
  min-height: 100vh;
  min-height: 100svh;
}
```

## 3. Systematic 4px/8px Spacing Scale
- `0.25rem` (4px): Micro gaps (icons, badges).
- `0.5rem` (8px): Compact element spacing (input labels, button gaps).
- `0.75rem` (12px): Standard inner padding (inputs, chips).
- `1rem` (16px): Component base padding (cards, list items).
- `1.5rem` (24px): Card layout padding, form group separation.
- `2rem` (32px): Section headers, modal padding.
- `3rem` (48px) - `5rem` (80px): Hero section page padding.
