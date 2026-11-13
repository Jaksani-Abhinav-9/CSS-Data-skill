# CSS Interaction States: The Complete 6-State Matrix

## 1. The 6 Mandatory UI Component States
Every interactive element (buttons, links, inputs, cards) must define explicit visual treatments for the 6 interactive states:

```
[1. Default / Idle]   ---> Normal state at rest
[2. Hover]            ---> Mouse cursor hovers over element
[3. Focus / Visible]  ---> Keyboard tab navigation reaches element
[4. Active / Pressed] ---> Mouse down / tap moment of interaction
[5. Disabled]         ---> Element unavailable (`disabled`, `aria-disabled="true"`)
[6. Loading]          ---> Background operation in progress (`aria-busy="true"`)
```

---

## 2. LVHA Pseudo-Class Order for Links
To avoid cascade conflicts, link pseudo-classes must be declared in this strict order:
1. `:link`
2. `:visited`
3. `:hover`
4. `:active`

---

## 3. Focus-Visible (Keyboard Accessibility Best Practice)
Never use `outline: none` without providing an accessible alternative! Use `:focus-visible` so mouse clicks don't show intrusive rings, while keyboard users receive high-visibility focus indicators:

```css
/* Remove default outline only when focus-visible will handle it */
:focus:not(:focus-visible) {
  outline: none;
}

/* Clear, distinct focus ring for keyboard navigation */
:focus-visible {
  outline: 2px solid var(--accent-primary);
  outline-offset: 2px;
}
```

---

## 4. Form Validation States
- `:valid` & `:invalid`: Evaluates native HTML5 validation constraints.
- `:user-invalid`: Evaluates validity only **after the user has interacted with the field** (prevents intimidating red errors on fresh unsubmitted forms).
- `:placeholder-shown`: True when input field is empty.
- `:disabled` & `:read-only`: Disables interaction while maintaining readability.
