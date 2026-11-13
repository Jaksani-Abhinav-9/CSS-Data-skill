# Modal Dialogs, Popovers & Drawer Overlays
Source Attribution: shadcn/ui Dialog & Radix Dialog Primitives

## 1. What is a Modal / Dialog Component?
An interactive focused window interrupting normal page flow to display critical confirmations, detailed forms, or alerts, backed by a darkened blur backdrop.

## 2. Standard Parts & DOM Anatomy:
- `.modal-backdrop` / `.modal-overlay`: `fixed` inset 0, dark blur backdrop (`rgba(0,0,0,0.75)` + `backdrop-filter: blur(6px)`).
- `.modal-dialog` / `.modal-content`: Centered card with 16px radius, max-width 520px, deep elevation shadow.
- `.modal-header`: Title + subtitle.
- `.modal-close`: Top-right dismiss icon button.
- `.modal-body`: Main content area with 1.6 line height.
- `.modal-footer`: Right-aligned action buttons (Cancel + Confirm).

## 3. Pure CSS Implementation:
```css
.modal-overlay {
  position: fixed;
  inset: 0;
  z-index: 1000;
  background-color: rgba(0, 0, 0, 0.75);
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1.5rem;
}

.modal-dialog {
  background-color: #181b24;
  border: 1px solid #272a38;
  border-radius: 16px;
  padding: 2rem;
  max-width: 520px;
  width: 100%;
  box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.6);
  animation: modal-pop 200ms cubic-bezier(0.23, 1, 0.32, 1);
}

@keyframes modal-pop {
  from {
    opacity: 0;
    transform: scale(0.96) translateY(6px);
  }
  to {
    opacity: 1;
    transform: scale(1) translateY(0);
  }
}
```
