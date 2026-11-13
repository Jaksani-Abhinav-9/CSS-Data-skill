# Accordions, Tabs & Segmented Controls Anatomy
Source Attribution: shadcn/ui Accordion, Tabs & Radix Primitives

## 1. What is an Accordion / Tab Component?
An interactive disclosure system allowing users to toggle the visibility of content sections in limited vertical screen real estate (e.g. FAQ accordions, settings tab bars).

## 2. Standard Parts & DOM Anatomy:
- `.accordion`: Vertical flex stack with 0.75rem gap.
- `.accordion-item`: Surface card with 10px radius, border, and active state highlight.
- `.accordion-header` / `.accordion-trigger`: Full-width button with space-between flex layout and rotating chevron icon.
- `.accordion-body` / `.accordion-content`: Expandable body with 1.6 line-height.
- `.tabs-container`: Outer wrapper holding tab list and tab panels.
- `.tab-list`: Horizontal flex row with border-bottom indicator track.
- `.tab-trigger`: Clean text button with relative positioning and active accent underline (`::after`).

## 3. Scoped Pure CSS:
```css
.accordion-item {
  background-color: #181b24;
  border: 1px solid #272a38;
  border-radius: 10px;
  overflow: hidden;
  transition: border-color 150ms ease;
}

.accordion-item:hover, .accordion-item.active {
  border-color: #ff5500;
}

.accordion-header {
  width: 100%;
  padding: 1.25rem 1.5rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: none;
  border: none;
  color: #f8fafc;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  text-align: left;
}

.accordion-body {
  padding: 0 1.5rem 1.25rem 1.5rem;
  color: #94a3b8;
  font-size: 0.95rem;
  line-height: 1.6;
}

.tab-trigger.active {
  color: #ff5500;
}

.tab-trigger.active::after {
  content: '';
  position: absolute;
  bottom: -1px;
  left: 0;
  right: 0;
  height: 2px;
  background-color: #ff5500;
}
```
