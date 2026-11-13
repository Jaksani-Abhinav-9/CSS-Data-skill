# CSS Component Styling: Buttons, Interactive States, and Badges

## 1. Core Button Component Architecture

```css
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  font-family: inherit;
  font-size: 0.95rem;
  font-weight: 600;
  line-height: 1;
  border-radius: var(--radius-md);
  border: 1px solid transparent;
  cursor: pointer;
  text-decoration: none;
  user-select: none;
  white-space: nowrap;
  transition: all var(--transition-fast);
}

.btn:focus-visible {
  outline: 2px solid var(--accent-primary);
  outline-offset: 2px;
}

.btn:disabled, .btn[aria-disabled="true"] {
  opacity: 0.5;
  cursor: not-allowed;
  pointer-events: none;
}
```

---

## 2. Button Variant Hierarchy

### Primary Button (Solid Accent)
```css
.btn-primary {
  background-color: var(--accent-primary);
  color: #ffffff;
  box-shadow: var(--shadow-sm);
}

.btn-primary:hover {
  background-color: var(--accent-hover);
  transform: translateY(-1px);
  box-shadow: var(--shadow-md);
}

.btn-primary:active {
  transform: translateY(0);
}
```

### Secondary Button (Muted Surface)
```css
.btn-secondary {
  background-color: var(--bg-surface);
  color: var(--text-primary);
  border-color: var(--border-color);
}

.btn-secondary:hover {
  background-color: var(--bg-card);
  border-color: var(--border-focus);
}
```

### Ghost / Text Button
```css
.btn-ghost {
  background-color: transparent;
  color: var(--text-secondary);
}

.btn-ghost:hover {
  background-color: var(--accent-subtle);
  color: var(--accent-primary);
}
```

---

## 3. Status Badges & Pill Indicators
```css
.badge {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  padding: 0.25rem 0.65rem;
  font-size: 0.75rem;
  font-weight: 700;
  letter-spacing: 0.02em;
  border-radius: var(--radius-full);
  line-height: 1;
}

.badge-success {
  background-color: rgba(16, 185, 129, 0.15);
  color: #10b981;
  border: 1px solid rgba(16, 185, 129, 0.3);
}

.badge-warning {
  background-color: rgba(245, 158, 11, 0.15);
  color: #f59e0b;
  border: 1px solid rgba(245, 158, 11, 0.3);
}
```
