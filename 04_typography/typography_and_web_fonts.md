# CSS Typography: Web Fonts, Font Metrics, and Text Styling

## 1. System Font Stacks
System font stacks provide zero network latency and native UI feel:

```css
:root {
  /* Modern Sans-Serif System Font Stack */
  --font-sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;

  /* Monospace / Code Font Stack */
  --font-mono: 'JetBrains Mono', 'Fira Code', ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;

  /* Editorial / Serif Font Stack */
  --font-serif: 'Playfair Display', Georgia, Cambria, 'Times New Roman', Times, serif;
}
```

---

## 2. Web Font Loading and Performance
- **`font-display: swap`**: Displays fallback system font immediately, swapping in custom web font when loaded to prevent invisible text (FOIT).
- **Preloading critical fonts**:
  ```html
  <link rel="preload" href="/fonts/inter.woff2" as="font" type="font/woff2" crossorigin>
  ```
- **`@font-face` Declaration**:
  ```css
  @font-face {
    font-family: 'CustomFont';
    src: url('/fonts/custom-font.woff2') format('woff2');
    font-weight: 100 900; /* Variable font weight range */
    font-style: normal;
    font-display: swap;
  }
  ```

---

## 3. Typography Properties & Best Practices

| Property | Recommended Values | Best Practice / Rationale |
|---|---|---|
| `font-size` | Use `rem` or fluid `clamp()` | Respects user browser zoom and OS accessibility font scaling |
| `line-height` | `1.5` to `1.7` (body), `1.1` to `1.25` (headings) | Use **unitless numbers** (e.g. `1.6`) so it scales proportionately |
| `font-weight` | `400` (Regular), `500` (Medium), `600` (SemiBold), `700` (Bold) | Stick to 3 distinct weights in a single interface to reduce visual noise |
| `letter-spacing` | `-0.02em` to `-0.01em` (large headings), `0` to `0.02em` (small body/caps) | Tighten tracking on large headings, loosen on small all-caps labels |
| `text-wrap` | `balance` (headings), `pretty` (paragraphs) | Prevents lonely single-word orphan lines on headings and paragraphs |
| `-webkit-font-smoothing` | `antialiased; -moz-osx-font-smoothing: grayscale;` | Ensures crisp, refined glyph rendering on macOS and dark backgrounds |
