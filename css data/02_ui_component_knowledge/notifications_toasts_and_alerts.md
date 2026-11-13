# Notifications, Toast Alerts & Status Badges
Source Attribution: shadcn/ui Toast, Radix Toast & Sonner primitives

## 1. What is a Notification / Toast Component?
A floating or inline feedback container designed to unobtrusively inform users of system events (success, error, warning, info), with auto-dismiss timers and optional action triggers.

## 2. Standard Parts & DOM Anatomy:
- `.notification-card` / `.toast`: Flex row container with 10px radius, deep elevation shadow, and a 4px accent border-left.
- `.notification-icon`: Left-aligned visual indicator (check, alert circle, info).
- `.notification-content`: Flex-1 column holding the title and description.
- `.notification-title`: 700 weight, 0.95rem font size, #f8fafc.
- `.notification-message` / `.toast-description`: 0.875rem muted text (#94a3b8).
- `.badge`: Small pill label (9999px radius, uppercase font).
  - `.badge-success`: Tinted green background (`rgba(34, 197, 94, 0.15)`) + green border.
  - `.badge-warning`: Tinted amber background (`rgba(245, 158, 11, 0.15)`) + amber border.
  - `.badge-error`: Tinted red background (`rgba(239, 68, 68, 0.15)`) + red border.
- `.toast-close`: Micro dismiss button.

## 3. Scoped Pure CSS:
```css
.notification-card, .toast {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  padding: 1.25rem;
  background-color: #181b24;
  border: 1px solid #272a38;
  border-left: 4px solid #ff5500;
  border-radius: 10px;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.4);
  max-width: 440px;
  margin: 1rem auto;
  transition: transform 200ms cubic-bezier(0.23, 1, 0.32, 1);
}

.notification-title {
  font-size: 0.95rem;
  font-weight: 700;
  color: #f8fafc;
  margin-bottom: 0.25rem;
}

.notification-message {
  font-size: 0.875rem;
  color: #94a3b8;
  line-height: 1.5;
}

.badge {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  padding: 0.25rem 0.65rem;
  font-size: 0.75rem;
  font-weight: 700;
  border-radius: 9999px;
  text-transform: uppercase;
}

.badge-success {
  background-color: rgba(34, 197, 94, 0.15);
  color: #22c55e;
  border: 1px solid rgba(34, 197, 94, 0.3);
}
```
