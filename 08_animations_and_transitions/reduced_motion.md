# CSS Animations: Accessibility and Reduced Motion Compliance

## 1. Respecting User Motion Sensitivity
Vestibular disorders and motion sickness can be triggered by aggressive parallax scrolling, large spinning elements, or continuous sliding animations.

Modern operating systems (macOS, Windows, iOS, Android) provide a system-level "Reduce Motion" setting that CSS detects via `@media (prefers-reduced-motion: reduce)`.

---

## 2. Universal Reduced-Motion Reset Pattern
```css
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

---

## 3. Graceful Degradation Pattern (Fades Instead of Slides)
```css
/* Normal: Slide and Fade */
.dialog {
  transition: transform 0.3s ease, opacity 0.3s ease;
  transform: translateY(0);
  opacity: 1;
}

/* Reduced Motion: Instant Fade Only (Zero Spatial Displacement) */
@media (prefers-reduced-motion: reduce) {
  .dialog {
    transition: opacity 0.15s linear;
    transform: none !important;
  }
}
```
