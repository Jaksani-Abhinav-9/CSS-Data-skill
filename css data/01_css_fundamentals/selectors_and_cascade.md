# CSS Selectors, Cascade & Specificity Guide
Source Attribution: MDN Web Docs (CSS Selectors & Cascade Specifications)

## 1. Core Selector Hierarchy & Specificity Weight
CSS Specificity is calculated as a 3-tuple `(A, B, C)`:
- **A (IDs)**: `#header` -> `(1, 0, 0)` = 100
- **B (Classes, Attributes, Pseudo-classes)**: `.btn`, `[type="email"]`, `:hover`, `:focus-visible` -> `(0, 1, 0)` = 10
- **C (Elements, Pseudo-elements)**: `button`, `div`, `::before`, `::after` -> `(0, 0, 1)` = 1
- **Universal / Combinators**: `*`, `>`, `+`, `~`, `:where()` -> `(0, 0, 0)` = 0

### Golden Rules for Clean Architecture:
1. **Never use IDs for styling**: Use class-based BEM/Utility selectors (`.card-header` not `#card-header`) to avoid specificity wars.
2. **Avoid deep nesting**: Keep selector depth <= 2 levels (`.auth-card .btn-submit` instead of `body div.main-wrapper div.auth-card form.auth-form button.btn-submit`).
3. **Use `:is()` and `:where()` for grouping**:
   - `:is(.btn, .link):hover` retains the highest specificity inside.
   - `:where(.btn, .link):hover` resets specificity to 0, ideal for resets.
4. **Use `:has()` for Parent Relational Selectors**:
   - `.form-group:has(:user-invalid)` styles the container when an inner input fails validation.
   - `.card:has(.badge-popular)` applies border glow when a popular badge is present.
