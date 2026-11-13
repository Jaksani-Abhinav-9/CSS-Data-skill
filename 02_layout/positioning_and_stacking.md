# CSS Layout: Positioning, Insets, and Stacking Contexts

## 1. The 5 Position Values

| Value | Document Flow | Offset Reference Point | Primary Use Case |
|---|---|---|---|
| **`static`** (default) | Normal document flow | Inset properties (`top/left/etc.`) have no effect | Default elements |
| **`relative`** | In normal flow (leaves space occupied) | Its own normal position in flow | Anchor container for `absolute` children, subtle offset nudges |
| **`absolute`** | Removed from document flow | Nearest **positioned ancestor** (non-static) | Badges, tooltips, dropdown menus, overlay modal close buttons |
| **`fixed`** | Removed from document flow | **Viewport** (stays in place during scrolling) | Sticky navigation bars, floating action buttons (FAB), modals |
| **`sticky`** | In flow until scroll threshold | Scroll container / Viewport | Sticky table headers, alphabet list dividers, sticky sidebars |

---

## 2. Inset Properties and Shorthands
Modern CSS provides the `inset` logical shorthand for `top`, `right`, `bottom`, `left`:
```css
/* Full overlay covering parent */
.overlay {
  position: absolute;
  inset: 0; /* Equivalent to: top: 0; right: 0; bottom: 0; left: 0; */
  background: rgba(0, 0, 0, 0.6);
}
```

---

## 3. Stacking Context & `z-index`
`z-index` specifies the 3D stack order of positioned elements along the Z-axis (towards the user).

### Important Rule: `z-index` only works on positioned elements (`relative`, `absolute`, `fixed`, `sticky`) or flex/grid children!

### What Creates a New Stacking Context?
1. Root element (`<html>`).
2. `position: relative | absolute` with a non-auto `z-index`.
3. `position: fixed | sticky`.
4. Flex or Grid children with a non-auto `z-index`.
5. `opacity` less than `1`.
6. `transform`, `filter`, `perspective`, `clip-path`, or `backdrop-filter` not `none`.
7. `isolation: isolate` (Explicit best-practice for isolating component z-index layers).

### Stacking Hierarchy System
```css
:root {
  --z-negative: -1;
  --z-base: 0;
  --z-elevated: 10;
  --z-sticky: 100;
  --z-dropdown: 200;
  --z-drawer: 300;
  --z-modal-backdrop: 400;
  --z-modal: 500;
  --z-toast: 600;
  --z-tooltip: 700;
}
```
