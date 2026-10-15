# Student Study Planner

A modern, responsive web application designed to help students organize their academic life — tasks, subjects, calendar, and progress tracking — all in one clean workspace.

---

## Features

### ✅ Implemented

**Authentication**
- Simple name-based login with real-time validation (min 2 chars, max 50)
- Session persistence via LocalStorage (`isLoggedIn`, `userName`)
- Secure logout with dropdown menu

**Dashboard & Navigation**
- Fixed left sidebar (280px) with 6 sections: Dashboard, Tasks, Subjects, Calendar, Progress & Analytics, Settings
- Active state indication
- Mobile-first responsive: collapses to off-canvas drawer (<1024px) with hamburger FAB
- Top bar: global search (Esc to clear), calendar button, add task button, user profile dropdown
- Fully responsive top bar: stacked on mobile, horizontal on desktop (≥768px)

**UI Components (Ready for Logic)**
- Search input with icon, focus states, keyboard accessible
- Primary buttons with loading states
- Form inputs with validation styling (error/success)
- Avatar component (initials fallback)
- Status badges (ready/warning/danger)
- Cards, modals, dropdowns with outside-click/Escape dismiss
- Custom scrollbars

**Data & Storage**
- Full LocalStorage persistence (offline-first)
- No backend required — runs entirely in the browser
- Data survives browser restarts

---

### 🚧 Planned / In Progress

**Task Management**
- Add, complete, organize tasks by subject
- Priority levels and due dates
- Filter, sort, drag-and-drop reordering

**Subjects & Calendar**
- Subject-wise organization with color coding
- Calendar view (month/week/day) for scheduling
- Today/Upcoming/Overdue indicators

**Progress & Analytics**
- Study streak tracking
- Completion rate visualization
- Subject-wise breakdown charts

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| **Markup** | Semantic HTML5 |
| **Styling** | Tailwind CSS v4 (via CDN) + Custom CSS Variables |
| **Icons** | Ionicons 8 |
| **Typography** | Inter (Google Fonts) |
| **Logic** | Vanilla ES6+ JavaScript (modules, async/await) |
| **Storage** | LocalStorage API |
| **Architecture** | Single-page application (SPA) pattern |

---

## Project Structure

```
student-study-planner/
├── src/
│   ├── pages/
│   │   ├── index.html      # Main dashboard (authenticated)
│   │   └── login.html      # Login screen
│   ├── styles/
│   │   └── main.css        # Design tokens, components, responsive rules
│   └── assets/
│       └── images/         # Screenshots & illustrations
└── README.md
```

---

## Getting Started

### Prerequisites
- Any modern browser (Chrome, Firefox, Safari, Edge)
- No build tools, Node.js, or server required

### Run Locally
```bash
# Option 1: Open directly
open src/pages/login.html

# Option 2: Serve with a static server (recommended for SPA routing)
npx serve src/pages
# or
python -m http.server 8000 -d src/pages
```

Then navigate to `http://localhost:8000` (or the served URL).

---

## Design System

**Color Palette** (CSS Variables in `:root`)
```css
--color-primary: #2563EB;       /* Blue 600 */
--color-primary-hover: #1D4ED8; /* Blue 700 */
--color-primary-light: #DBEAFE; /* Blue 100 */
--color-bg: #FAF8FF;            /* Near-white with hint of purple */
--color-surface: #FFFFFF;       /* Pure white */
--color-border: #E5E7EB;        /* Gray 200 */
--color-text: #111827;          /* Gray 900 */
--color-text-muted: #6B7280;    /* Gray 500 */
--color-success: #059669;       /* Emerald 600 */
--color-warning: #D97706;       /* Amber 600 */
--color-danger: #DC2626;        /* Red 600 */
--color-error: #DC2626;
--color-error-bg: #FEF2F2;
```

**Spacing & Radius**
- Base unit: 4px (Tailwind scale)
- Border radius: 10px (buttons/inputs), 12px (cards), 16px (modals)

**Shadows**
- Subtle elevation: `0 1px 3px rgba(0,0,0,0.05), 0 4px 12px rgba(0,0,0,0.03)`

**Breakpoints** (Tailwind v4 defaults)
- `sm`: 640px
- `md`: 768px
- `lg`: 1024px
- `xl`: 1280px

---

## Responsive Behavior

| Component | <640px | 640–767px | 768–1023px | ≥1024px |
|-----------|--------|-----------|------------|---------|
| Sidebar | Off-canvas drawer + FAB | Off-canvas drawer + FAB | Off-canvas drawer + FAB | Fixed 280px |
| Top bar | Stacked: search → 3 icon buttons | Stacked: search → 3 icon buttons | Horizontal: search left, actions right | Horizontal: search left, actions right |
| Calendar btn | Icon only | Icon only | Icon + "Today, Oct 24" | Icon + "Today, Oct 24" |
| Add Task btn | Icon only | Icon only | "Add Task" + icon | "Add Task" + icon |
| Profile | Avatar only (44px) | Avatar only (44px) | Avatar + name + grade | Avatar + name + grade |

---

## Accessibility

- Semantic HTML landmarks (`<main>`, `<nav>`, `<aside>`, `<header>`)
- ARIA labels, roles, and live regions on all interactive elements
- Full keyboard navigation (Tab, Enter, Escape, Arrow keys)
- Focus-visible outlines with custom primary color
- Sufficient color contrast (WCAG AA)
- Screen-reader friendly form validation
- `novalidate` + custom validation with `aria-describedby` + `aria-live`

---

## Browser Support

| Browser | Version |
|---------|---------|
| Chrome  | 90+     |
| Firefox | 88+     |
| Safari  | 14+     |
| Edge    | 90+     |

Requires: ES6 Modules, CSS Custom Properties, LocalStorage, `focus-visible`

---

## Roadmap

- [ ] Task CRUD with drag-and-drop reordering
- [ ] Subject management (create, edit, delete, color picker)
- [ ] Calendar integration (month/week/day views, event creation)
- [ ] Progress charts (Chart.js or Canvas API)
- [ ] Pomodoro timer with session logging
- [ ] Data export/import (JSON, CSV)
- [ ] Dark mode toggle
- [ ] PWA manifest + service worker for offline installability

---

## Learning Outcomes

This project demonstrates:
- Modern CSS architecture with design tokens and utility-first framework integration
- Vanilla JavaScript SPA patterns (routing, state, DOM management)
- Accessibility-first development
- Responsive layout techniques (Flexbox, Grid, media queries)
- LocalStorage as a client-side database
- Clean component organization without a framework

---

## License

MIT — free to use, modify, and distribute.

---

## Author

**Aman Bhagat**  
Grade 12 Student • Aspiring Full-Stack Developer  
[GitHub](https://github.com/amanxploit) • [LinkedIn](https://www.linkedin.com/in/aman-bhagat-10641422a/)