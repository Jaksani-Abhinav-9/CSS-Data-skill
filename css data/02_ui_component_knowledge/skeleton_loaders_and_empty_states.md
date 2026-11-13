# Skeleton Loaders & Empty States Anatomy
Source Attribution: shadcn/ui Skeleton, Vercel Loading Guidelines

## 1. What are Skeleton Loaders and Empty States?
- **Skeleton Loader**: A low-fidelity wireframe placeholder showing animated gradient shimmer while asynchronous data loads, reducing perceived latency.
- **Empty State**: A friendly contextual container displayed when a list/table has zero items, prompting action with an icon, title, description, and primary CTA.

## 2. Standard Parts & DOM Anatomy:
- `.skeleton`: Rounded gray placeholder with continuous horizontal shimmer keyframe.
- `.skeleton-avatar`: 50% radius circular wireframe.
- `.skeleton-title` / `.skeleton-text`: Pill lines with variable widths (e.g. 60%, 80%).
- `.empty-state`: Centered container with 3rem padding, empty state illustration/icon, `.empty-title`, and `.empty-action`.

## 3. Scoped Pure CSS:
```css
.skeleton {
  background: linear-gradient(90deg, #181b24 25%, #272a38 50%, #181b24 75%);
  background-size: 200% 100%;
  animation: skeleton-shimmer 1.5s infinite linear;
  border-radius: 6px;
}

@keyframes skeleton-shimmer {
  0% { background-position: 200% 0; }
  100% { background-position: -200% 0; }
}

.empty-state {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 4rem 2rem;
  text-align: center;
  background-color: #181b24;
  border: 1px dashed #272a38;
  border-radius: 16px;
}

.empty-title {
  font-size: 1.25rem;
  font-weight: 700;
  color: #f8fafc;
  margin: 1rem 0 0.5rem 0;
}

.empty-desc {
  font-size: 0.9rem;
  color: #94a3b8;
  max-width: 420px;
  margin-bottom: 1.5rem;
}
```
