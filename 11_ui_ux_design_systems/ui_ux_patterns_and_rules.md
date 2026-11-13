# UI/UX Patterns: Consolidated Interface Engineering Rules

*Synthesized from UI/UX Mastery Skill, UI/UX Pro Max, Vercel Web Interface Guidelines, and Emil Kowalski Interaction Rules.*

---

## 1. Visual Hierarchy & Scannability Rules
1. **Never use pure `#000000` or `#ffffff` for text/background**: Use rich darks (`#090a0d`, `#0f172a`) and soft whites (`#f8fafc`).
2. **One Primary Action per View**: Avoid competing solid accent buttons on the same screen. Pair 1 Primary with Secondary/Ghost buttons.
3. **Z-Pattern and F-Pattern Scanning**: Align primary headings and brand logos top-left; align primary calls-to-action (CTAs) top-right and bottom-right.

---

## 2. Forms and Validation UX
1. **Never hide form labels**: Place labels top-aligned above inputs for fastest cognitive comprehension.
2. **Explicit error states**: Red border alone fails colorblind accessibility. Always pair visual border with a clear text error message.
3. **Always preserve user input**: Form validation errors must never wipe out already-typed values.
4. **Appropriate input types**: Use `type="email"`, `type="password"`, `type="tel"`, `autocomplete="..."` to trigger proper mobile keyboards.

---

## 3. Micro-Interaction & Animation Rules
1. **Duration Budget**: Micro-interactions should take **150ms to 300ms**. Anything over 400ms feels sluggish.
2. **Spatial Consistency**: If an element opens by sliding downwards, closing it must reverse the motion by sliding upwards.
3. **Hover + Active Feedback**: Every interactive card, button, and navigation item must provide immediate visual feedback on hover and mouse down.
