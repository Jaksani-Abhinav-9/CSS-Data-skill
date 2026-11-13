# CSS Colors & Visual Effects: Gradients, Box Shadows, and Glassmorphism

## 1. Linear & Radial Gradients

### Directional Linear Gradient
```css
.accent-gradient {
  background: linear-gradient(135deg, #ff5500 0%, #ff8800 100%);
}
```

### Text Gradient Fill (Masking)
```css
.gradient-heading {
  background: linear-gradient(135deg, #ff5500 0%, #ffaa00 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
```

### Ambient Radial Glow Backdrop
```css
.ambient-backdrop {
  background: radial-gradient(circle at 50% 0%, rgba(255, 85, 0, 0.15) 0%, transparent 70%);
}
```

---

## 2. Multi-Layered Elevation Box Shadows
Multi-layer shadows create natural atmospheric depth and avoid harsh black outlines:

```css
:root {
  /* Subtle Elevation (Cards, Inputs) */
  --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05);

  /* Medium Elevation (Dropdowns, Cards on Hover) */
  --shadow-md:
    0 4px 6px -1px rgba(0, 0, 0, 0.2),
    0 2px 4px -2px rgba(0, 0, 0, 0.2);

  /* High Elevation (Modals, Floating Panels) */
  --shadow-lg:
    0 10px 15px -3px rgba(0, 0, 0, 0.3),
    0 4px 6px -4px rgba(0, 0, 0, 0.3);

  /* Dramatic Glow */
  --shadow-glow:
    0 0 25px -5px rgba(255, 85, 0, 0.45);
}
```

---

## 3. Premium Glassmorphism
Combines semi-transparent background color with hardware-accelerated backdrop blur and subtle border highlight:

```css
.glass-panel {
  background: rgba(24, 27, 36, 0.7);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.37);
  border-radius: 16px;
}
```
