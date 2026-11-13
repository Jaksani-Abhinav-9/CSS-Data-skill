# CSS Animations: Keyframes, Loaders, and Micro-Interactions

## 1. Keyframe Animations Syntax
```css
@keyframes pulseGlow {
  0%, 100% {
    transform: scale(1);
    box-shadow: 0 0 0 0 rgba(255, 85, 0, 0.4);
  }
  50% {
    transform: scale(1.02);
    box-shadow: 0 0 20px 4px rgba(255, 85, 0, 0.2);
  }
}

.live-indicator {
  animation: pulseGlow 2s infinite ease-in-out;
}
```

---

## 2. Essential Micro-Interaction Patterns

### A. Spinner Loading Animation
```css
@keyframes spin {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

.spinner {
  width: 20px;
  height: 20px;
  border: 2px solid rgba(255, 255, 255, 0.2);
  border-top-color: var(--accent-primary);
  border-radius: 50%;
  animation: spin 0.75s linear infinite;
}
```

### B. Skeleton Shimmer Wave
```css
@keyframes skeletonShimmer {
  0% { background-position: -200% 0; }
  100% { background-position: 200% 0; }
}

.skeleton {
  background: linear-gradient(90deg, #181b24 25%, #242838 50%, #181b24 75%);
  background-size: 200% 100%;
  animation: skeletonShimmer 1.5s infinite;
  border-radius: var(--radius-sm);
}
```

### C. Fade-In Slide-Up Entrance
```css
@keyframes slideUpFade {
  from {
    opacity: 0;
    transform: translateY(12px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-entrance {
  animation: slideUpFade 0.35s var(--ease-out) forwards;
}
```
