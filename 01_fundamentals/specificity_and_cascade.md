# CSS Fundamentals: Specificity, Cascade, and Inheritance

## 1. Specificity Weight Calculation

Specificity is represented as a 4-part tuple `(Inline, ID, Class/Attribute/Pseudo-class, Type/Pseudo-element)`:

| Component | Weight Position | What Counts | Examples |
|---|---|---|---|
| **Inline Styles** | `(1, 0, 0, 0)` | `style="..."` attribute | `<div style="color: red;">` |
| **ID Selectors** | `(0, 1, 0, 0)` | `#id` | `#nav-header`, `#auth-form` |
| **Classes / Attributes / Pseudo-classes** | `(0, 0, 1, 0)` | `.class`, `[attr]`, `:hover`, `:focus` | `.btn`, `[type="text"]`, `:focus-visible` |
| **Type / Pseudo-elements** | `(0, 0, 0, 1)` | `element`, `::before`, `::after` | `p`, `div`, `h1`, `::placeholder` |
| **Universal / Zero** | `(0, 0, 0, 0)` | `*`, `:where()` | `*`, `:where(.btn)` |

### Specificity Comparison Examples
```css
/* (0, 0, 0, 1) */  p                       { color: #333; }
/* (0, 0, 1, 0) */  .text-body              { color: #444; }
/* (0, 0, 1, 1) */  p.text-body             { color: #555; }
/* (0, 0, 2, 1) */  article.card p.text     { color: #666; }
/* (0, 1, 1, 0) */  #sidebar .nav-item      { color: #777; }
/* (0, 2, 0, 0) */  #main #sidebar          { color: #888; }
```

---

## 2. The 6-Step Cascade Algorithm
When multiple declarations target the same property on the same element, the cascade resolves the conflict using this exact order:

1. **Origin & Importance**:
   - Transition declarations (`transition`)
   - `!important` User-Agent declarations
   - `!important` User declarations
   - `!important` Author declarations
   - Animation declarations (`@keyframes`)
   - Normal Author declarations
   - Normal User declarations
   - Normal User-Agent declarations (browser defaults)
2. **Context (Shadow DOM / Light DOM)**: Inner shadow tree vs outer document.
3. **Cascade Layers (`@layer`)**: Unlayered styles override layered styles. Within layers, later defined layers win.
4. **Specificity**: Highest `(A, B, C, D)` tuple wins.
5. **Scope Proximity**: Styles defined closer to the target scope take precedence.
6. **Order of Appearance**: Last declared rule in the source stylesheet wins.

---

## 3. Cascade Layers (`@layer`)
Modern CSS allows explicit prioritization of style layers independent of specificity:
```css
@layer reset, base, components, utilities;

@layer reset {
  * { box-sizing: border-box; margin: 0; }
}

@layer base {
  body { font-family: 'Inter', sans-serif; line-height: 1.6; }
}

@layer components {
  .btn { padding: 0.75rem 1.5rem; border-radius: 8px; }
}

@layer utilities {
  .hidden { display: none !important; }
}
```

---

## 4. Property Inheritance
- **Inherited by default**: Typography and text properties (`font-family`, `font-size`, `font-weight`, `line-height`, `color`, `letter-spacing`, `text-align`, `visibility`).
- **Not inherited by default**: Box model, background, and layout properties (`margin`, `padding`, `border`, `background`, `display`, `position`, `width`, `height`, `z-index`, `overflow`).

### Explicit Inheritance Keywords
- `inherit`: Forces the property to take the computed value from its parent.
- `initial`: Resets the property to its initial specification default.
- `unset`: Acts as `inherit` for inherited properties, and `initial` for non-inherited properties.
- `revert`: Rolls back the cascade value to the user-agent / browser default.
- `all: unset`: Resets all properties on the element.
