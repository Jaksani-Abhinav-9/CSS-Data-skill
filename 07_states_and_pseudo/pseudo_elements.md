# CSS Pseudo-Elements: Generated Content and Styling Hooks

## 1. Pseudo-Elements Syntax
Pseudo-elements target specific sub-parts of an element and use the double colon (`::`) syntax (CSS3 standard):

| Pseudo-Element | Purpose | Example |
|---|---|---|
| `::before` | Injects decorative generated content before element's children | Icon prefixes, custom bullets, gradient glows |
| `::after` | Injects decorative generated content after element's children | Active indicators, external link icons, badges |
| `::placeholder` | Styles placeholder text in inputs/textareas | `input::placeholder { color: #64748b; }` |
| `::selection` | Styles highlighted text selected by user | `::selection { background: #ff5500; color: white; }` |
| `::marker` | Styles list bullet points or numbers | `li::marker { color: var(--accent-primary); }` |
| `::file-selector-button` | Styles the file upload button on `<input type="file">` | Custom upload button styling |

---

## 2. Inset Glow Overlay Pattern with `::before`
```css
.glow-card {
  position: relative;
  background: var(--bg-card);
  border-radius: var(--radius-lg);
  overflow: hidden;
}

.glow-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--accent-primary), transparent);
  opacity: 0;
  transition: opacity var(--transition-base);
}

.glow-card:hover::before {
  opacity: 1;
}
```
