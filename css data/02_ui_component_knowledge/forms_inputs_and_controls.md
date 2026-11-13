# Form Controls, Input States & Validation Anatomy
Source Attribution: shadcn/ui Form primitives & MDN Form Guidelines

## 1. What is a Form Control Component?
A complete data input module containing: label, input/textarea/select field, placeholder, focus ring, helper text, and validation error messages.

## 2. Standard Parts & DOM Anatomy:
- `.form-group`: Vertical container with `0.5rem` gap.
- `.form-label`: 600 weight, 0.875rem font size.
- `.form-control`: Dark background (`#12141a`), 1px border (`#272a38`), 8px radius.
- `.form-control:focus`: Accent border (`#ff5500`) + glowing outer ring (`box-shadow: 0 0 0 3px rgba(...)`).
- `.form-control:user-invalid`: Red border (`#ef4444`) + error ring.
- `.form-error` / `.error-msg`: 0.8rem red descriptive label.

## 3. Scoped Pure CSS Implementation:
```css
.form-group {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  text-align: left;
}

.form-label {
  font-size: 0.875rem;
  font-weight: 600;
  color: #f8fafc;
}

.form-control {
  width: 100%;
  padding: 0.75rem 1rem;
  font-family: inherit;
  font-size: 0.95rem;
  color: #f8fafc;
  background-color: #12141a;
  border: 1px solid #272a38;
  border-radius: 8px;
  outline: none;
  transition: border-color 0.15s cubic-bezier(0.4, 0, 0.2, 1),
              box-shadow 0.15s cubic-bezier(0.4, 0, 0.2, 1);
}

.form-control:focus {
  border-color: #ff5500;
  box-shadow: 0 0 0 3px rgba(255, 85, 0, 0.12);
}

.form-control:user-invalid {
  border-color: #ef4444;
  box-shadow: 0 0 0 3px rgba(239, 68, 68, 0.15);
}
```
