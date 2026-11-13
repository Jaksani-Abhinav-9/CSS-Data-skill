# Tactile Physics, Micro-Interactions & Transitions
Source Attribution: Emil Kowalski (Design Engineer Principles) & Radix UI

## 1. The Natural Easing Curve (Fast Out, Slow In)
Standard `ease` or `linear` feels robotic. Use cubic-bezier easing:
```css
--ease-out-quint: cubic-bezier(0.23, 1, 0.32, 1);
```

## 2. Physical Button Interaction States
Every interactive element should respond with tactile physics:
```css
.btn {
  transition: transform 160ms cubic-bezier(0.23, 1, 0.32, 1),
              background-color 160ms ease,
              box-shadow 160ms ease;
}

.btn:hover {
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(255, 85, 0, 0.25);
}

.btn:active {
  transform: scale(0.97);
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.15);
}
```

## 3. Motion Safety & Accessibility
Always include `@media (prefers-reduced-motion: reduce)`:
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
