# STYLUS CSS Knowledge Foundation

Welcome to the **STYLUS CSS Knowledge Foundation**. This directory serves as the authoritative, ground-truth knowledge repository for CSS syntax, fundamentals, layout algorithms, responsive mechanics, visual design tokens, component styling, and UI/UX engineering principles.

---

## Knowledge Hierarchy

```
css/
├── 01_fundamentals/
│   ├── syntax_and_selectors.md            # Syntax, combinators, attribute selectors, :is, :where, :has
│   ├── specificity_and_cascade.md         # Specificity calculation, 6-step cascade, @layer, inheritance
│   ├── box_model_and_sizing.md            # Box model, border-box, margin collapse, sizing constraints
│   └── units_and_math.md                  # px, rem, em, %, vh, dvh, cqw, calc, min, max, clamp
├── 02_layout/
│   ├── flexbox_mastery.md                 # 1D flexbox container/item axes, alignment, gap, recipes
│   ├── grid_mastery.md                    # 2D CSS grid, fr units, minmax, auto-fit, areas, subgrid
│   └── positioning_and_stacking.md        # static, relative, absolute, fixed, sticky, z-index, contexts
├── 03_responsive/
│   ├── media_queries.md                   # Mobile-first breakpoints, hover detection, color schemes
│   ├── container_queries.md               # @container inline-size, container units (cqw, cqi)
│   └── fluid_responsive_design.md         # Fluid clamp typography & spacing scales, intrinsic design
├── 04_typography/
│   ├── typography_and_web_fonts.md        # System font stacks, @font-face, line-height, tracking
│   └── text_wrapping_and_truncation.md    # Single/multi-line clamp, overflow-wrap, line measures
├── 05_colors_and_effects/
│   ├── color_systems_and_tokens.md        # Hex, RGB, HSL, OKLCH, color-mix, semantic color scales
│   ├── custom_properties_and_themes.md    # CSS variables, data-theme dark/light mode architecture
│   └── gradients_shadows_glassmorphism.md # Gradients, text clipping, multi-layered shadows, glass panels
├── 06_components_and_forms/
│   ├── form_controls_styling.md           # Text inputs, textareas, custom accessible checkboxes
│   ├── buttons_and_badges.md              # Primary/secondary/ghost hierarchy, pill badges, focus rings
│   ├── cards_and_containers.md            # Card layout, hover elevation, metric stat tiles
│   └── navigation_and_headers.md          # Sticky navbar, active indicators, dashboard sidebars
├── 07_states_and_pseudo/
│   ├── interaction_states.md              # 6-state matrix (Default, Hover, Focus, Active, Disabled, Loading)
│   └── pseudo_elements.md                 # ::before, ::after, ::placeholder, ::selection, glow overlays
├── 08_animations_and_transitions/
│   ├── transitions_and_transforms.md      # GPU composite transforms, cubic-bezier easing curves
│   ├── keyframes_and_micro_interactions.md# Spinners, skeleton shimmer, slide-up entrances, pulse glows
│   └── reduced_motion.md                  # prefers-reduced-motion accessibility compliance
├── 09_accessibility/
│   └── accessible_styling_and_wcag.md     # WCAG 2.1 AA contrast (4.5:1), 44px touch targets, .sr-only, skip-link
├── 10_architecture_and_modern/
│   ├── css_architecture_and_conventions.md# BEM methodology, utility patterns, production stylesheet structure
│   └── modern_css_features.md             # Native CSS nesting, @property animatable variables, logical properties
├── 11_ui_ux_design_systems/
│   ├── design_tokens_specification.md     # 3-tier token graph (primitive -> semantic -> component)
│   └── ui_ux_patterns_and_rules.md        # Consolidated visual hierarchy, forms UX, micro-interaction rules
└── 12_frameworks_and_references/
    ├── tailwind_and_shadcn_distinction.md # Separation of pure CSS from Tailwind and shadcn
    └── upstream_resource_registry.md      # Complete inventory and classification of 26 upstream repos
```

---

## Architectural Rules
1. **Purity First**: Foundational CSS stands completely independent of JavaScript frameworks, Tailwind, or component libraries.
2. **Deterministic Grounding**: Every rule and token follows modern W3C standards and WCAG 2.1 AA accessibility guidelines.
3. **No Premature Model Training**: This directory represents the knowledge base to prepare for future CSS specialist training.
