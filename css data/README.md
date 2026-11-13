# STYLUS CSS / UI Domain Knowledge Base
Location: `skills for ai/helping agents/css data/`

This directory houses the authoritative domain knowledge corpus for the STYLUS CSS Specialist Agent and Code Generation Engine.

## Structure:
1. `01_css_fundamentals/`: Core CSS specifications (MDN aligned): Selectors, Cascade, Modern Units (100svh), Flexbox/Grid, Color systems, Easing physics.
2. `02_ui_component_knowledge/`: Anatomy, parts, and scoped CSS patterns for all standard UI components (Buttons, Forms, Cards, Modals, Tables, Alerts, Tabs, Skeletons).
3. `03_ui_domain_blueprints/`: Full-page domain compositions (Auth, Landing pages, Dashboards, Pricing tables, E-Commerce, User Profiles, Chatbots).
4. `04_shadcn_and_design_system_registry/`: shadcn/ui component matrix, design tokens, and tactile interaction guidelines.

## Utilization:
- **Retrieval & Context Injection**: Integrated directly into `models/css/generator.py` and `CSSDOMInspector` for instant deterministic synthesis and zero-leakage selector scoping.
