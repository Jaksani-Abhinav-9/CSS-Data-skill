# shadcn/ui Component Anatomy & CSS Pattern Matrix
Source Attribution: shadcn/ui Registry & Radix UI Primitives

| Component Name | UX Purpose / What Is It? | Standard Anatomy Sub-Elements | Key CSS Patterns Applied |
|---|---|---|---|
| **Accordion** | Vertically stacked expandable disclosure panels | `.accordion`, `.accordion-item`, `.accordion-header`, `.accordion-trigger`, `.accordion-content` | `grid-template-rows: 0fr -> 1fr` height transition, chevron rotate `180deg` |
| **Alert / Toast** | Status messages attracting user attention | `.alert`, `.alert-title`, `.alert-description`, `.alert-icon` | Border-left 4px accent, `rgba` tinted background, flex start icon alignment |
| **Avatar** | Visual representation of user/entity | `.avatar`, `.avatar-image`, `.avatar-fallback` | `border-radius: 50%`, `object-fit: cover`, centered initials fallback |
| **Badge** | Small status or category label indicator | `.badge`, `.badge-default`, `.badge-secondary`, `.badge-outline` | `border-radius: 9999px`, compact padding `0.25rem 0.65rem`, uppercase font |
| **Button** | Clickable action trigger with tactile feedback | `.btn`, `.btn-primary`, `.btn-secondary`, `.btn-destructive`, `.btn-outline`, `.btn-ghost` | `scale(0.97)` on active, `translateY(-1px)` on hover, `cubic-bezier(0.23, 1, 0.32, 1)` |
| **Card** | Surface container grouping related information | `.card`, `.card-header`, `.card-title`, `.card-description`, `.card-content`, `.card-footer` | Surface `#181b24`, 1px border `#272a38`, 12px-16px radius, subtle box-shadow |
| **Dialog / Modal** | Window overlaid on page requiring interaction | `.dialog-overlay`, `.dialog-content`, `.dialog-header`, `.dialog-footer`, `.dialog-close` | `position: fixed; inset: 0`, backdrop blur, center flexbox, pop-in animation |
| **Dropdown Menu** | Contextual action list revealed by button | `.dropdown-menu`, `.dropdown-trigger`, `.dropdown-content`, `.dropdown-item` | `position: absolute`, z-index 50, hover item highlight background |
| **Input / Form** | Data capture fields with focus outlines | `.form-group`, `.form-label`, `.form-control`, `.form-error` | `#12141a` input surface, 3px focus ring, `:user-invalid` error outline |
| **Navigation Bar** | Persistent top-level site orientation bar | `.navbar`, `.nav-container`, `.nav-brand`, `.nav-menu`, `.nav-link` | `position: sticky; top: 0`, backdrop blur, space-between flexbox |
| **Progress Bar** | Visual indicator of operation completion | `.progress`, `.progress-bar`, `.progress-indicator` | Track background `#272a38`, accent indicator fill, `overflow: hidden` |
| **Skeleton** | Animated placeholder shimmer during loading | `.skeleton`, `.skeleton-card`, `.skeleton-text`, `.skeleton-avatar` | Linear gradient animation shimmer `@keyframes shimmer` |
| **Tabs** | Segmented view switcher within same container | `.tabs`, `.tab-list`, `.tab-trigger`, `.tab-content` | Border-bottom active indicator, relative positioning |
| **Tooltip** | Informational popup on hover/focus | `.tooltip`, `.tooltip-trigger`, `.tooltip-content` | Floating dark pill, font-size 0.75rem, z-index 1000 |
