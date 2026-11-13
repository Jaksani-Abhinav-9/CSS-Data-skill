# Modern CSS Knowledge & Engineering Skill

An authoritative, framework-agnostic knowledge foundation covering modern CSS syntax, responsive mechanics, design token architecture, layout algorithms, micro-interactions, and WCAG accessibility standards.

---

## 🎯 What Is This Skill For?

This repository is designed to serve as a **deterministic, ground-truth reference** for modern web styling. It can be used as:

### 1. Context & Skill Anchor for AI Coding Agents
- Prevents AI hallucinations by anchoring models to modern W3C standards (`:has()`, container queries, subgrid, native nesting).
- Guarantees that AI-generated code is modular, semantic, accessible, and free of outdated hacks (`float`, `!important`, arbitrary `z-index`).

### 2. Design System & Token Foundation
- Serves as the single source of truth for design tokens (3-tier hierarchy: primitive $\rightarrow$ semantic $\rightarrow$ component).
- Allows engineering teams to establish fluid spacing scales, OKLCH color palettes, and dark/light mode themes before writing framework code.

### 3. Production Reference for Frontend Engineers
- A comprehensive manual for pure, vanilla CSS that eliminates unnecessary third-party CSS library dependencies.
- Contains battle-tested layout recipes, accessible form controls, and hardware-accelerated animation patterns.

---

## 📁 Knowledge Hierarchy

```text
css/
├── 01_fundamentals/
│   ├── syntax_and_selectors.md            # Modern combinators, attribute selectors, :is(), :where(), :has()
│   ├── specificity_and_cascade.md         # Specificity formula, cascade layers (@layer), inheritance
│   ├── box_model_and_sizing.md            # Content-box vs. border-box, margin collapse, intrinsic sizing
│   └── units_and_math.md                  # rem, em, ch, dvh, cqw, calc(), min(), max(), clamp()
├── 02_layout/
│   ├── flexbox_mastery.md                 # 1D flexbox axes, alignment, gap, responsive flex recipes
│   ├── grid_mastery.md                    # 2D CSS grid, fr units, minmax(), auto-fit/auto-fill, subgrid
│   └── positioning_and_stacking.md        # static, relative, absolute, fixed, sticky, stacking contexts
├── 03_responsive/
│   ├── media_queries.md                   # Mobile-first breakpoints, hover detection, color scheme queries
│   ├── container_queries.md               # @container inline-size, container query units (cqw, cqi)
│   └── fluid_responsive_design.md         # Mathematical fluid typography and spacing with clamp()
├── 04_typography/
│   ├── typography_and_web_fonts.md        # System font stacks, @font-face performance, line-height ratios
│   └── text_wrapping_and_truncation.md    # Multi-line line-clamp, overflow-wrap, optimal line lengths
├── 05_colors_and_effects/
│   ├── color_systems_and_tokens.md        # Hex, HSL, modern OKLCH color spaces, color-mix()
│   ├── custom_properties_and_themes.md    # CSS variables, data-theme dark/light mode architecture
│   └── gradients_shadows_glassmorphism.md # Gradients, text masks, multi-layered shadows, backdrop-filter
├── 06_components_and_forms/
│   ├── form_controls_styling.md           # Accessible inputs, floating labels, custom checkboxes/radios
│   ├── buttons_and_badges.md              # Button hierarchy (solid, outline, ghost), pill badges, focus rings
│   ├── cards_and_containers.md            # Responsive card layouts, elevation on hover, stat widgets
│   └── navigation_and_headers.md          # Sticky headers, breadcrumbs, responsive mobile menus
├── 07_states_and_pseudo/
│   ├── interaction_states.md              # 6-state matrix (Default, Hover, Focus-Visible, Active, Disabled, Loading)
│   └── pseudo_elements.md                 # ::before, ::after overlays, ::placeholder, ::selection
├── 08_animations_and_transitions/
│   ├── transitions_and_transforms.md      # GPU composite transforms (translate, scale), cubic-bezier easing
│   ├── keyframes_and_micro_interactions.md# Skeleton loaders, slide-up entrances, pulse indicators
│   └── reduced_motion.md                  # prefers-reduced-motion accessibility compliance
├── 09_accessibility/
│   └── accessible_styling_and_wcag.md     # WCAG 2.1 AA compliance (4.5:1 contrast), 44px touch targets, .sr-only
├── 10_architecture_and_modern/
│   ├── css_architecture_and_conventions.md# BEM methodology, modular stylesheet organisation
│   └── modern_css_features.md             # Native CSS nesting, @property animatable variables, logical properties
├── 11_ui_ux_design_systems/
│   ├── design_tokens_specification.md     # 3-tier token graph (primitive -> semantic -> component)
│   └── ui_ux_patterns_and_rules.md        # Visual hierarchy, typography scales, feedback patterns
└── 12_frameworks_and_references/
    ├── tailwind_and_shadcn_distinction.md # Mapping pure CSS concepts to utility classes and headless components
    └── upstream_resource_registry.md      # Curated reference index of modern UI libraries and specs
```

---

## ⚡ Core Engineering Principles

Every rule, pattern, and token in this repository adheres to three non-negotiable principles:

| Principle | Standard |
| :--- | :--- |
| **Framework Agnostic** | 100% pure vanilla CSS. Zero required runtime libraries, preprocessors, or frameworks. Works universally in plain HTML, React, Vue, Svelte, or Astro. |
| **Deterministic Accessibility** | Strict adherence to **WCAG 2.1 AA**: minimum 4.5:1 text contrast, custom visible focus rings (`:focus-visible`), and screen-reader utilities (`.sr-only`). |
| **Hardware-Accelerated Performance** | All animations strictly animate composite-only properties (`transform` and `opacity`) to guarantee 60fps/120fps smooth rendering without triggering browser reflows. |

---

## 📖 How to Use This Knowledge Base

### For Human Developers:
1. **Layouts:** Check `02_layout/grid_mastery.md` and `02_layout/flexbox_mastery.md` for responsive layout patterns.
2. **Tokens & Theming:** Look at `05_colors_and_effects/custom_properties_and_themes.md` to set up automated dark/light mode switching.
3. **Accessibility:** Reference `09_accessibility/` whenever styling interactive elements or forms to ensure keyboard and screen-reader accessibility.

### For AI Coding Assistants:
When prompting an AI assistant to build UI, link or feed this skill as context:
> *"Use the patterns in `02_layout/grid_mastery.md` and `05_colors_and_effects/` to construct a responsive, accessible dashboard card using pure CSS and semantic HTML."*

---

## 📄 License
MIT — Free for personal, open-source, and commercial engineering use.
