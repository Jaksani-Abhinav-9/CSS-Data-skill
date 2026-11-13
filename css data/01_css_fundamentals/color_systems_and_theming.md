# Modern Color Systems, OKLCH, Dark Mode & Glassmorphism
Source Attribution: CSS Color Module Level 4 & Vercel Design Guidelines

## 1. Dark Mode Color Foundations
Avoid harsh pure black (`#000000`) for surfaces; use layered slate/zinc tones:
- **Base Background**: `#090a0d` (ultra deep slate)
- **Layer 1 Surface (Cards, Modals)**: `#181b24` or `rgba(24, 27, 36, 0.85)`
- **Layer 2 Input / Secondary**: `#12141a`
- **Subtle Borders**: `#272a38`
- **Brand Accent**: `#ff5500` (tactile flame orange)
- **Primary Text**: `#f8fafc` (high-contrast off-white)
- **Muted Text**: `#94a3b8` (WCAG AAA contrast compliant)

## 2. Proper Glassmorphism Pattern (Semi-Transparent Blur)
When applying `backdrop-filter: blur()`, background MUST be semi-transparent:
```css
.glass-card {
  background-color: rgba(24, 27, 36, 0.85);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  border: 1px solid #272a38;
}
```
