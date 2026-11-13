# CSS Component Styling: Cards, Containers, and Data Tiles

## 1. Card Container Architecture

```css
.card {
  display: flex;
  flex-direction: column;
  background-color: var(--bg-card);
  border: 1px solid var(--border-color);
  border-radius: var(--radius-lg);
  padding: 1.5rem;
  box-shadow: var(--shadow-sm);
  transition: transform var(--transition-base), box-shadow var(--transition-base), border-color var(--transition-base);
  overflow: hidden;
  position: relative;
}

.card:hover {
  transform: translateY(-2px);
  border-color: rgba(255, 85, 0, 0.4);
  box-shadow: var(--shadow-md);
}

.card-header {
  margin-bottom: 1rem;
}

.card-title {
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--text-primary);
}

.card-description {
  font-size: 0.9rem;
  color: var(--text-secondary);
  margin-top: 0.25rem;
}

.card-body {
  flex: 1;
}

.card-footer {
  margin-top: 1.25rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
```

---

## 2. KPI / Metric Stat Tile

```css
.stat-card {
  background: var(--bg-card);
  border: 1px solid var(--border-color);
  border-radius: var(--radius-md);
  padding: 1.25rem;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.stat-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.stat-label {
  font-size: 0.85rem;
  font-weight: 600;
  color: var(--text-secondary);
}

.stat-value {
  font-size: 1.75rem;
  font-weight: 800;
  color: var(--text-primary);
  letter-spacing: -0.02em;
}

.stat-trend {
  font-size: 0.8rem;
  font-weight: 700;
}

.trend-up {
  color: var(--status-success);
}

.trend-down {
  color: var(--status-error);
}
```
