# File Upload & Dropzone Component
Source Attribution: Modern SaaS Asset Uploaders

## 1. Standard Parts:
- `.dropzone-box`: Dashed border container with hover pulse, center aligned.
- `.dropzone-title`: 1.1rem title.

## 2. Scoped Pure CSS:
```css
.dropzone-box {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 3.5rem 2rem;
  border: 2px dashed #272a38;
  border-radius: 14px;
  background-color: #181b24;
  text-align: center;
  max-width: 540px;
  margin: 2rem auto;
  transition: border-color 200ms ease, background-color 200ms ease;
}

.dropzone-box:hover {
  border-color: #ff5500;
  background-color: rgba(255, 85, 0, 0.02);
}

.dropzone-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: #f8fafc;
  margin-bottom: 1rem;
}
```
