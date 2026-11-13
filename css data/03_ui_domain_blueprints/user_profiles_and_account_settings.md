# User Profiles & Account Settings Blueprint
Source Attribution: shadcn/ui Settings Blocks & Profile Card Standards

## 1. Domain Concept: "WHAT IS A USER PROFILE / SETTINGS VIEW?"
A dedicated view displaying user identity, bio, role, stats, social links, avatar upload controls, and account settings panels.

## 2. Standard Parts & DOM Anatomy:
1. `.profile-card`: Centered elevation card with avatar, name, role badge, bio text, and action buttons.
2. `.profile-avatar`: Circular image (`border-radius: 50%`) with 2px accent border and hover glow.
3. `.profile-name`: 1.25rem bold title.
4. `.profile-role`: 0.85rem muted text or badge.
5. `.profile-bio`: 0.9rem text with 1.6 line-height.
6. `.profile-stats`: Horizontal 3-column stats bar (Followers, Following, Projects).
7. `.btn-follow` / `.btn-edit`: Action buttons with tactile active compression.

## 3. Scoped Pure CSS:
```css
.profile-card {
  background-color: #181b24;
  border: 1px solid #272a38;
  border-radius: 16px;
  padding: 2.25rem 1.75rem;
  max-width: 360px;
  margin: 2rem auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.35);
  transition: transform 240ms cubic-bezier(0.23, 1, 0.32, 1), border-color 240ms ease;
}

.profile-card:hover {
  transform: translateY(-4px);
  border-color: #ff5500;
}

.profile-avatar {
  width: 96px;
  height: 96px;
  border-radius: 50%;
  object-fit: cover;
  border: 3px solid #ff5500;
  margin-bottom: 1.25rem;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
}

.profile-name {
  font-size: 1.35rem;
  font-weight: 700;
  color: #f8fafc;
  margin-bottom: 0.25rem;
}

.profile-role {
  font-size: 0.875rem;
  color: #ff5500;
  font-weight: 600;
  margin-bottom: 0.75rem;
}

.profile-bio {
  font-size: 0.9rem;
  color: #94a3b8;
  line-height: 1.5;
  margin-bottom: 1.5rem;
}
```
