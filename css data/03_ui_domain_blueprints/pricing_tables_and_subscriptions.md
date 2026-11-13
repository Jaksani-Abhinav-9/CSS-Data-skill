# Pricing Tables & Subscription Tiers Domain Blueprint
Source Attribution: shadcn/ui Blocks & Modern SaaS UI Ecosystems

## 1. Domain Concept: "WHAT IS A PRICING SECTION?"
A comparison grid displaying subscription tiers (e.g. Starter, Pro, Enterprise) highlighting value propositions, price amounts, billing frequencies, feature checklists, and primary CTA buttons.

## 2. Standard Parts & DOM Anatomy:
1. `.pricing-section`: Centered section with header (Title + Subtitle + optional monthly/annual billing switch).
2. `.pricing-grid`: Responsive 3-column auto-wrapping grid (`repeat(auto-fit, minmax(280px, 1fr))`).
3. `.pricing-card`: Surface card with 14px radius, padding, price value, feature list, and CTA button.
4. `.pricing-card.popular`: Featured center tier with flame border (`#ff5500`), subtle elevation transform, and `.popular-badge` ribbon.
5. `.price-amount`: Large bold numeral (e.g. `$29`) with `/month` frequency label.
6. `.features-list`: Unordered list with checkmark icons.

## 3. Scoped Pure CSS:
```css
.pricing-section {
  max-width: 1200px;
  margin: 0 auto;
  padding: 4rem 1.5rem;
  text-align: center;
}

.pricing-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  align-items: stretch;
}

.pricing-card {
  background-color: #181b24;
  border: 1px solid #272a38;
  border-radius: 16px;
  padding: 2.5rem 2rem;
  display: flex;
  flex-direction: column;
  text-align: left;
  transition: transform 240ms cubic-bezier(0.23, 1, 0.32, 1), border-color 240ms ease;
}

.pricing-card.popular {
  border-color: #ff5500;
  box-shadow: 0 16px 32px -8px rgba(255, 85, 0, 0.2);
  transform: scale(1.03);
}

.pricing-card .btn-plan {
  margin-top: auto;
  width: 100%;
}
```
