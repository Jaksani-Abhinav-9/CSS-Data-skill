# CSS Architecture: Methodologies, Naming Conventions, and Token Graphs

## 1. CSS Methodologies Comparison

| Methodology | Concept | Naming Convention | Primary Strengths |
|---|---|---|---|
| **BEM (Block Element Modifier)** | Strict component encapsulation | `.block__element--modifier` | Eliminates cascade conflicts, self-documenting markup |
| **Utility-First (Token-Driven)** | Single-purpose atomic utility classes | `.flex`, `.p-4`, `.text-center` | Rapid prototyping, zero dead CSS buildup |
| **Component-Scoped CSS** | Encapsulated styles per UI component | `.card`, `.card-title`, `.btn` | High maintainability, clean separation of concerns |

---

## 2. BEM Naming Pattern
```css
/* Block (Standalone Component) */
.card { ... }

/* Element (Child of Block) */
.card__header { ... }
.card__title { ... }
.card__body { ... }
.card__action-btn { ... }

/* Modifier (Variant or State) */
.card--featured { border-color: gold; }
.card--compact { padding: 0.75rem; }
```

---

## 3. Standard Production Stylesheet File Structure
```
styles/
├── 00_reset.css          (Universal box-sizing and margin resets)
├── 01_tokens.css         (Custom property color/spacing/type token dictionary)
├── 02_base.css           (HTML, body, typography, anchor defaults)
├── 03_layout.css         (Grid system, containers, navbar, sidebar)
├── 04_components.css     (Buttons, cards, inputs, badges, tables)
├── 05_animations.css     (Keyframes, transitions, reduced motion)
└── 06_utilities.css      (Screen reader text, flex helpers, spacing utilities)
```
