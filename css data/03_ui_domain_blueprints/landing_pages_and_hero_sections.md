# Landing Pages & Hero Showcase Blueprint
Source Attribution: shadcn/ui Blocks, Vercel Landing Pages, 21st.dev

## 1. Domain Concept: "WHAT IS A HERO / LANDING VIEW?"
The primary conversion section of a website designed to captivate visitors with a value proposition, dynamic gradient headline, social proof badge, and CTA action buttons.

## 2. Standard Parts & DOM Anatomy:
1. `.hero-section`: Centered column container with 6rem top padding.
2. `.hero-badge`: Rounded pill badge (`rgba(255, 85, 0, 0.1)`) with accent border.
3. `.hero-title`: Large clamp font (`clamp(2.25rem, 5vw, 3.75rem)`), 900 weight, -0.03em tracking.
4. `.gradient-text`: Text clipped to linear gradient (`#ff5500 -> #ff8844`).
5. `.hero-subtitle`: Max-width 680px muted paragraph with 1.6 line-height.
6. `.hero-cta-group`: Horizontal row of action buttons (Primary CTA + Secondary Demo button).

## 3. Scoped Pure CSS:
```css
.hero-section {
  padding: 6rem 1.5rem 4rem 1.5rem;
  text-align: center;
  max-width: 1000px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.35rem 0.85rem;
  border-radius: 9999px;
  font-size: 0.8rem;
  font-weight: 600;
  color: #ff5500;
  background-color: rgba(255, 85, 0, 0.1);
  border: 1px solid rgba(255, 85, 0, 0.25);
  margin-bottom: 1.5rem;
}

.hero-title {
  font-size: clamp(2.25rem, 5vw, 3.75rem);
  font-weight: 900;
  line-height: 1.1;
  letter-spacing: -0.03em;
  color: #f8fafc;
  margin-bottom: 1.25rem;
}

.gradient-text {
  background: linear-gradient(135deg, #ff5500 0%, #ff8844 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero-subtitle {
  font-size: clamp(1rem, 2vw, 1.25rem);
  color: #94a3b8;
  line-height: 1.6;
  max-width: 680px;
  margin: 0 auto 2.5rem auto;
}

.hero-cta-group {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  flex-wrap: wrap;
}
```
