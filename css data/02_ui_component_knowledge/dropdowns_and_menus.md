# Dropdown Menus & Action Lists
Source Attribution: Radix Dropdown Menu, shadcn/ui Dropdown Menu

## 1. What is a Dropdown Component?
A floating contextual list of actions displayed upon clicking or activating a trigger button.

## 2. Standard Parts & DOM Anatomy:
- `.dropdown`: Relative container wrapper.
- `.dropdown-trigger`: Action button.
- `.dropdown-menu`: Floating panel with 10px radius, dark surface, elevation shadow.
- `.dropdown-item`: Menu item link/button with hover highlight (`rgba(255, 85, 0, 0.1)`).

## 3. Scoped Pure CSS:
```css
.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-menu {
  position: absolute;
  top: calc(100% + 6px);
  left: 0;
  min-width: 180px;
  background-color: #181b24;
  border: 1px solid #272a38;
  border-radius: 10px;
  padding: 0.35rem;
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.5);
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
  z-index: 50;
}

.dropdown-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.5rem 0.75rem;
  color: #cbd5e1;
  text-decoration: none;
  font-size: 0.875rem;
  border-radius: 6px;
  transition: background-color 120ms ease, color 120ms ease;
}

.dropdown-item:hover {
  background-color: rgba(255, 85, 0, 0.1);
  color: #ff5500;
}
```
