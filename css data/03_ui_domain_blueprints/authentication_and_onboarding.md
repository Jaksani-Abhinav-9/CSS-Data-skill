# Authentication, Login & Signup Domain Blueprint
Source Attribution: shadcn/ui Blocks (Auth-01) & WebUI Dataset

## 1. Domain Concept: "WHAT IS AN AUTHENTICATION VIEW?"
A standalone, distraction-free screen designed to securely authenticate users (Sign In, Sign Up, Password Reset, SSO).

## 2. Standard Parts & DOM Anatomy:
1. `.auth-wrapper`: Fullscreen centered container with `min-height: 100svh` and subtle radial glow.
2. `.auth-card`: Semi-transparent card with `backdrop-filter: blur(16px)` and 16px border-radius.
3. `.auth-header`: Brand logo, `.auth-title` (24px-28px bold), and `.auth-subtitle` (muted).
4. `.auth-form`: Vertical stack containing Email `.form-group`, Password `.form-group`, and optional "Remember Me" checkbox.
5. `.btn-submit`: Full-width primary action button with hover glow and active tactile scale.
6. `.auth-footer`: Muted navigation link ("Don't have an account? Sign Up").

## 3. Scoped Pure CSS:
```css
.auth-wrapper {
  min-height: 100vh;
  min-height: 100svh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1.5rem;
  background: radial-gradient(circle at 50% 0%, rgba(255, 85, 0, 0.08) 0%, transparent 65%);
}

.auth-card {
  width: 100%;
  max-width: 440px;
  background-color: rgba(24, 27, 36, 0.85);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  border: 1px solid #272a38;
  border-radius: 16px;
  padding: 2.5rem 2rem;
  box-shadow: 0 20px 40px -15px rgba(0, 0, 0, 0.5);
}

.auth-title {
  font-size: 1.75rem;
  font-weight: 800;
  letter-spacing: -0.02em;
  color: #f8fafc;
  margin-bottom: 0.5rem;
}

.auth-form .btn-submit {
  width: 100%;
  margin-top: 0.5rem;
}
```
