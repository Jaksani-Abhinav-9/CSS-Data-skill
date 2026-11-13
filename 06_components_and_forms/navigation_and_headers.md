# CSS Component Styling: Navigation, App Headers, and Sidebars

## 1. Sticky Top Navigation Bar

```css
.site-header {
  position: sticky;
  top: 0;
  z-index: var(--z-sticky, 100);
  width: 100%;
  background-color: rgba(9, 10, 13, 0.85);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border-color);
}

.nav-container {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 1.5rem;
  height: 64px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.brand-logo {
  font-size: 1.15rem;
  font-weight: 800;
  color: var(--text-primary);
  text-decoration: none;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.nav-menu {
  display: flex;
  align-items: center;
  gap: 1.5rem;
  list-style: none;
}

.nav-link {
  color: var(--text-secondary);
  text-decoration: none;
  font-size: 0.9rem;
  font-weight: 500;
  transition: color var(--transition-fast);
  padding: 0.5rem 0;
  position: relative;
}

.nav-link:hover, .nav-link.active {
  color: var(--text-primary);
}

.nav-link.active::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 2px;
  background-color: var(--accent-primary);
  border-radius: 2px;
}
```

---

## 2. Dashboard Sidebar Navigation
```css
.sidebar {
  width: 260px;
  height: 100vh;
  position: sticky;
  top: 0;
  background-color: var(--bg-surface);
  border-right: 1px solid var(--border-color);
  display: flex;
  flex-direction: column;
  padding: 1.5rem 1rem;
}

.sidebar-nav {
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
  margin-top: 1.5rem;
}

.sidebar-link {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 0.65rem 0.85rem;
  border-radius: var(--radius-md);
  color: var(--text-secondary);
  text-decoration: none;
  font-size: 0.9rem;
  font-weight: 500;
  transition: all var(--transition-fast);
}

.sidebar-link:hover {
  background-color: rgba(255, 255, 255, 0.05);
  color: var(--text-primary);
}

.sidebar-link.active {
  background-color: var(--accent-subtle);
  color: var(--accent-primary);
  font-weight: 600;
}
```
