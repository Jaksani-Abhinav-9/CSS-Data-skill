# CSS Frameworks & Libraries: Pure CSS vs Tailwind vs shadcn/ui

## 1. Separation of General CSS from Framework-Specific Conventions

For the STYLUS CSS Specialist, general CSS fundamentals must remain completely independent and primary. Frameworks are an optional layer on top.

```
+-------------------------------------------------------------+
|                      GENERAL CSS                            |
| (Selectors, Cascade, Box Model, Flexbox, Grid, Tokens)      |
+-------------------------------------------------------------+
                              |
         +--------------------+--------------------+
         |                                         |
         v                                         v
+-----------------------------+       +-----------------------------+
|     TAILWIND UTILITIES      |       |      SHADCN / RADIX UI      |
| (Utility class mapping)     |       | (Accessible Component Specs)|
+-----------------------------+       +-----------------------------+
```

---

## 2. General CSS vs Tailwind Equivalence Matrix

| Requirement | General Standard CSS | Tailwind CSS Utility |
|---|---|---|
| Flex Center | `display: flex; align-items: center; justify-content: center;` | `flex items-center justify-center` |
| Responsive Grid | `display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1rem;` | `grid grid-cols-1 md:grid-cols-3 gap-4` |
| Fluid Padding | `padding-inline: clamp(1rem, 4vw, 2.5rem);` | `px-4 md:px-8 lg:px-10` |
| Smooth Transition | `transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);` | `transition-all duration-200 ease-out` |
| Card Border & Shadow | `border: 1px solid var(--border-color); box-shadow: var(--shadow-md);` | `border border-border shadow-md` |
| Focus Ring | `:focus-visible { outline: 2px solid #ff5500; outline-offset: 2px; }` | `focus-visible:ring-2 focus-visible:ring-primary` |

---

## 3. Framework Boundary Rule
- **Standard CSS Mode**: When the user requests clean HTML & CSS or modern web styling, STYLUS writes **pure, framework-agnostic CSS** using semantic classes and CSS custom properties.
- **Tailwind Mode**: Activated only when the user explicitly requests Tailwind styling in the prompt.
- **shadcn Mode**: Used for React/TypeScript component tree implementations requiring Radix primitives and Tailwind styling.
