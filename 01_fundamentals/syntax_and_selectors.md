# CSS Fundamentals: Syntax and Selectors

## 1. CSS Syntax Structure
CSS rules consist of a **selector** and a **declaration block**:
```css
selector {
  property: value; /* Declaration */
}
```
- **Case Sensitivity**: Selectors and property names are ASCII case-insensitive, but values (like URL paths, custom property names, and class/id attributes in HTML) are case-sensitive.
- **Statement Types**: Rulesets, `@-rules` (`@media`, `@keyframes`, `@layer`, `@container`, `@font-face`, `@supports`).

---

## 2. Universal, Type, Class, and ID Selectors

| Selector Type | Syntax | Description | Example |
|---|---|---|---|
| **Universal** | `*` | Matches any element in the DOM | `* { box-sizing: border-box; }` |
| **Type (Element)** | `element` | Matches elements by HTML tag name | `h1 { font-size: 2rem; }` |
| **Class** | `.classname` | Matches elements having the specified class attribute | `.btn-primary { background: #ff5500; }` |
| **ID** | `#idname` | Matches an element with a unique `id` attribute | `#main-header { position: sticky; }` |

---

## 3. Combinators and Relationships

- **Descendant Combinator (` ` space)**: Matches any descendant node at any nesting depth.
  ```css
  .card p { color: #94a3b8; }
  ```
- **Child Combinator (`>`)**: Matches only direct children.
  ```css
  .nav-list > .nav-item { margin: 0; }
  ```
- **Adjacent Sibling (`+`)**: Matches the immediately following sibling.
  ```css
  h2 + p { margin-top: 0.5rem; }
  ```
- **General Sibling (`~`)**: Matches any sibling that follows anywhere in the same parent.
  ```css
  h2 ~ .article-text { line-height: 1.7; }
  ```

---

## 4. Attribute Selectors

| Attribute Selector | Match Rule | Use Case Example |
|---|---|---|
| `[attr]` | Element has attribute `attr` | `input[required] { border-left: 2px solid red; }` |
| `[attr="val"]` | Exact string match | `input[type="password"] { font-family: monospace; }` |
| `[attr~="val"]` | Space-separated word list contains `val` | `[data-tags~="featured"] { border: 1px solid gold; }` |
| `[attr^="val"]` | Starts with prefix `val` | `a[href^="https://"] { text-decoration: underline; }` |
| `[attr$="val"]` | Ends with suffix `val` | `a[href$=".pdf"]::after { content: " (PDF)"; }` |
| `[attr*="val"]` | Contains substring `val` | `button[class*="icon-"] { display: inline-flex; }` |

---

## 5. Modern Functional Pseudo-Classes

### `:is()` and `:where()`
- Groups selectors cleanly to avoid repetitive specificity chains:
  ```css
  /* Instead of: header h1, header h2, header h3, main h1, main h2, main h3 */
  :is(header, main) :is(h1, h2, h3) {
    line-height: 1.2;
  }
  ```
- **Specificity Difference**:
  - `:is()` takes the specificity of its **most specific** argument.
  - `:where()` **always has 0 specificity** `(0, 0, 0, 0)`, making it ideal for default styles that can be easily overridden.

### `:has()` (The Parent & Relational Selector)
- Selects an element based on its children or following siblings:
  ```css
  /* Style card differently if it contains an image */
  .card:has(img) {
    grid-template-rows: 200px auto;
  }

  /* Style form group when its child input is invalid */
  .form-group:has(input:invalid) {
    border-color: #ef4444;
  }
  ```

### `:not()`
- Negation pseudo-class:
  ```css
  button:not(.btn-disabled) {
    cursor: pointer;
  }
  ```
