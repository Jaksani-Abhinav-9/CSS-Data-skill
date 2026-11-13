# CSS Component Styling: Form Controls, Inputs, and Checkboxes

## 1. Text Inputs and Textareas

```css
.form-group {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  margin-bottom: 1.25rem;
}

.form-label {
  font-size: 0.875rem;
  font-weight: 600;
  color: var(--text-primary);
  display: flex;
  justify-content: space-between;
}

.form-control {
  width: 100%;
  padding: 0.75rem 1rem;
  font-family: inherit;
  font-size: 0.95rem;
  line-height: 1.5;
  color: var(--text-primary);
  background-color: var(--bg-surface);
  border: 1px solid var(--border-color);
  border-radius: var(--radius-md);
  outline: none;
  transition: border-color var(--transition-fast), box-shadow var(--transition-fast);
}

.form-control::placeholder {
  color: var(--text-muted);
}

/* Focus State with Ring */
.form-control:focus {
  border-color: var(--accent-primary);
  box-shadow: 0 0 0 3px var(--accent-subtle);
}

/* Error / Invalid State */
.form-control.is-invalid,
.form-control:user-invalid {
  border-color: var(--status-error);
  box-shadow: 0 0 0 3px rgba(239, 68, 68, 0.15);
}

.form-error-msg {
  font-size: 0.8rem;
  color: var(--status-error);
  margin-top: 0.25rem;
}
```

---

## 2. Accessible Custom Checkbox

```css
.checkbox-label {
  display: inline-flex;
  align-items: center;
  gap: 0.65rem;
  cursor: pointer;
  user-select: none;
  font-size: 0.9rem;
  color: var(--text-primary);
}

.custom-checkbox {
  appearance: none;
  width: 18px;
  height: 18px;
  border: 1.5px solid var(--border-color);
  border-radius: var(--radius-sm);
  background-color: var(--bg-surface);
  cursor: pointer;
  display: grid;
  place-content: center;
  transition: all var(--transition-fast);
}

.custom-checkbox::before {
  content: "";
  width: 10px;
  height: 6px;
  border-left: 2px solid #ffffff;
  border-bottom: 2px solid #ffffff;
  transform: rotate(-45deg) scale(0);
  transition: transform var(--transition-fast);
  margin-top: -2px;
}

.custom-checkbox:checked {
  background-color: var(--accent-primary);
  border-color: var(--accent-primary);
}

.custom-checkbox:checked::before {
  transform: rotate(-45deg) scale(1);
}

.custom-checkbox:focus-visible {
  outline: 2px solid var(--accent-primary);
  outline-offset: 2px;
}
```
