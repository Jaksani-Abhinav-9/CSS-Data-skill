# Data Tables, Lists & Tabular Grid Anatomy
Source Attribution: shadcn/ui Table & TanStack Table CSS Patterns

## 1. What is a Data Table Component?
A structured grid displaying multi-column tabular datasets with sortable sticky headers, interactive hover rows, alternating zebra stripes, and embedded status badges.

## 2. Standard Parts & DOM Anatomy:
- `.table-container` / `.data-table-wrapper`: `overflow-x: auto;` responsive scroll wrapper with rounded border.
- `.data-table` / `table`: `width: 100%; border-collapse: collapse;`.
- `.table-header` / `thead`: Sticky top background (`#12141a`), 0.75rem uppercase headers (#94a3b8), 1px bottom border.
- `.table-row` / `tr`: Row with bottom border (`#272a38`) and smooth hover transition (`background-color: rgba(255, 85, 0, 0.04)`).
- `.table-cell` / `td`: Standard padding (`1rem 1.25rem`), vertical align middle.
- `.table-pagination`: Footer toolbar with page controls and row counts.

## 3. Scoped Pure CSS:
```css
.table-container {
  width: 100%;
  overflow-x: auto;
  background-color: #181b24;
  border: 1px solid #272a38;
  border-radius: 12px;
}

.data-table {
  width: 100%;
  border-collapse: collapse;
  text-align: left;
  font-size: 0.9rem;
}

.data-table th {
  background-color: #12141a;
  color: #94a3b8;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  font-size: 0.75rem;
  padding: 1rem 1.25rem;
  border-bottom: 1px solid #272a38;
}

.data-table td {
  padding: 1rem 1.25rem;
  border-bottom: 1px solid #272a38;
  color: #f8fafc;
}

.data-table tr:hover {
  background-color: rgba(255, 85, 0, 0.04);
}
```
