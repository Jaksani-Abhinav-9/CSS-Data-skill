# Tooltips & Popovers Component Anatomy
Source Attribution: Radix Tooltip, shadcn/ui Tooltip

## 1. What is a Tooltip Component?
A floating micro-container providing brief context or information when hovering or focusing an interactive trigger.

## 2. Standard Parts & DOM Anatomy:
- `.tooltip-container`: Relative positioning anchor.
- `.tooltip-trigger`: Interactive target element.
- `.tooltip-bubble`: Floating text capsule with 6px radius, dark background (#181b24), 1px border (#272a38), 0.8rem font size.

## 3. Scoped Pure CSS:
```css
.tooltip-container {
  position: relative;
  display: inline-flex;
  align-items: center;
}

.tooltip-trigger {
  cursor: pointer;
  color: #94a3b8;
  transition: color 150ms ease;
}

.tooltip-trigger:hover {
  color: #f8fafc;
}

.tooltip-bubble {
  position: absolute;
  bottom: calc(100% + 8px);
  left: 50%;
  transform: translateX(-50%);
  background-color: #181b24;
  color: #f8fafc;
  border: 1px solid #272a38;
  border-radius: 6px;
  padding: 0.35rem 0.75rem;
  font-size: 0.8rem;
  white-space: nowrap;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.4);
  pointer-events: none;
  z-index: 100;
}
```
