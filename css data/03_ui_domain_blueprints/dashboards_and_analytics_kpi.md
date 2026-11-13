# Dashboards, SaaS Admin & Analytics KPI Blueprint
Source Attribution: shadcn/ui Dashboard Blocks & Tremor UI

## 1. Domain Concept: "WHAT IS A DASHBOARD VIEW?"
An administrative portal presenting telemetry, KPI statistics, charts, activity logs, and system controls.

## 2. Standard Parts & DOM Anatomy:
1. `.dashboard-layout`: Two-column grid (260px fixed `.sidebar` + fluid `.main-content`).
2. `.stats-grid`: Multi-card grid showing 3-4 top KPI metrics (e.g. Revenue, Active Users, Conversion Rate).
3. `.stat-card`: Compact metric tile with title, large stat value, and positive/negative trend badge.
4. `.chart-container`: Elevation card holding data visualizations.
5. `.data-table`: Striped/hoverable tabular data view with status pills.

## 3. Scoped Pure CSS:
```css
.dashboard-layout {
  display: grid;
  grid-template-columns: 260px 1fr;
  min-height: 100svh;
}

.sidebar {
  background-color: #12141a;
  border-right: 1px solid #272a38;
  padding: 1.5rem;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1.25rem;
  margin-bottom: 2rem;
}

.stat-card {
  background-color: #181b24;
  border: 1px solid #272a38;
  border-radius: 12px;
  padding: 1.25rem;
}

.stat-value {
  font-size: 1.85rem;
  font-weight: 800;
  color: #f8fafc;
  margin: 0.35rem 0;
}

@media (max-width: 768px) {
  .dashboard-layout {
    grid-template-columns: 1fr;
  }
  .sidebar {
    display: none;
  }
}
```
