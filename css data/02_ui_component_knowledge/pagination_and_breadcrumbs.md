# Pagination & Breadcrumbs Navigation
Source Attribution: shadcn/ui Pagination & Breadcrumb

## 1. Standard Parts:
- `.pagination`: Flex row of page buttons with active indicator.
- `.breadcrumb-trail`: Hierarchical horizontal links separated by slashes.

## 2. Scoped Pure CSS:
```css
.pagination {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  margin: 2rem auto;
}

.page-btn {
  padding: 0.5rem 0.85rem;
  background-color: #181b24;
  border: 1px solid #272a38;
  border-radius: 8px;
  color: #94a3b8;
  font-size: 0.875rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 150ms ease;
}

.page-btn:hover, .page-btn.active {
  background-color: #ff5500;
  color: #ffffff;
  border-color: #ff5500;
}

.breadcrumb-trail {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 0.875rem;
  color: #64748b;
  margin: 1rem 0;
}

.crumb-link {
  color: #94a3b8;
  text-decoration: none;
  transition: color 150ms ease;
}

.crumb-link:hover {
  color: #ff5500;
}

.crumb-active {
  color: #f8fafc;
  font-weight: 600;
}
```
