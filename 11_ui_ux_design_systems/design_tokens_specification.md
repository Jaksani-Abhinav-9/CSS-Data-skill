# UI/UX & Design Systems: Token Hierarchy and Architecture

## 1. The 3 Levels of Design Tokens

```
[1. Global / Primitive Tokens]
  - Raw color values, fixed pixel/rem measurements, base font family strings.
  - Example: `--color-orange-500: #ff5500;`, `--space-4: 1rem;`

          |
          v

[2. Semantic / Contextual Tokens]
  - Meaning-driven abstraction layer that connects to design intentions (theme-aware).
  - Example: `--accent-primary: var(--color-orange-500);`, `--bg-card: var(--color-slate-900);`

          |
          v

[3. Component / Scoped Tokens]
  - Scoped directly to individual component specifications.
  - Example: `--btn-primary-bg: var(--accent-primary);`, `--card-padding: var(--space-6);`
```

---

## 2. Complete Design Token Specification Schema

```css
:root {
  /* 1. Typography Tokens */
  --font-family-sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  --font-family-mono: 'JetBrains Mono', Consolas, monospace;

  /* 2. Color Tokens */
  --bg-primary: #090a0d;
  --bg-secondary: #12141a;
  --bg-card: #181b24;
  --text-primary: #f8fafc;
  --text-secondary: #94a3b8;
  --text-muted: #64748b;
  --accent-primary: #ff5500;
  --accent-hover: #ff6a00;
  --accent-gradient: linear-gradient(135deg, #ff5500 0%, #ff8800 100%);
  --border-color: #272a38;

  /* 3. Radius Tokens */
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-xl: 16px;
  --radius-2xl: 24px;
  --radius-full: 9999px;

  /* 4. Shadow Tokens */
  --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
  --shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.2), 0 2px 4px -2px rgba(0, 0, 0, 0.2);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.3), 0 4px 6px -4px rgba(0, 0, 0, 0.3);

  /* 5. Motion Tokens */
  --transition-fast: 0.15s cubic-bezier(0.4, 0, 0.2, 1);
  --transition-base: 0.25s cubic-bezier(0.4, 0, 0.2, 1);
  --transition-slow: 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}
```
