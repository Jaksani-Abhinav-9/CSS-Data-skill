# CSS Colors & Visual Effects: Custom Properties and Light/Dark Theming

## 1. CSS Custom Properties (Variables)
CSS Custom Properties inherit down the DOM tree and dynamically re-calculate in real-time when parent values change:

```css
:root {
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 16px;
  --radius-full: 9999px;
  --transition-fast: 0.15s ease;
  --transition-base: 0.25s cubic-bezier(0.4, 0, 0.2, 1);
}
```

### Accessing Custom Properties with Fallbacks
```css
.card {
  border-radius: var(--radius-md, 8px);
  background-color: var(--card-bg, #1e293b);
}
```

---

## 2. Complete Dual Theme Architecture (Light / Dark)

### Attribute-Based (`[data-theme]`) & System Media Query Synchronization
```css
/* Default: Dark Theme */
:root, [data-theme="dark"] {
  --bg-primary: #090a0d;
  --bg-secondary: #12141a;
  --bg-card: #181b24;
  --text-primary: #f8fafc;
  --text-secondary: #94a3b8;
  --border-color: #272a38;
  --card-shadow: 0 4px 20px -2px rgba(0, 0, 0, 0.5);
  color-scheme: dark;
}

/* Light Theme */
[data-theme="light"] {
  --bg-primary: #f8fafc;
  --bg-secondary: #f1f5f9;
  --bg-card: #ffffff;
  --text-primary: #0f172a;
  --text-secondary: #475569;
  --border-color: #e2e8f0;
  --card-shadow: 0 4px 20px -2px rgba(0, 0, 0, 0.08);
  color-scheme: light;
}

/* Automatic System Preference Sync (when no manual override is active) */
@media (prefers-color-scheme: light) {
  :root:not([data-theme="dark"]) {
    --bg-primary: #f8fafc;
    --bg-secondary: #f1f5f9;
    --bg-card: #ffffff;
    --text-primary: #0f172a;
    --text-secondary: #475569;
    --border-color: #e2e8f0;
    --card-shadow: 0 4px 20px -2px rgba(0, 0, 0, 0.08);
    color-scheme: light;
  }
}
```
