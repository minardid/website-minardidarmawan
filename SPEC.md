# SPEC.md — Minardi Darmawan Personal Branding Site

## 1. Concept & Vision

A dark, precision-engineered personal portfolio that channels Linear's signature aesthetic — near-black surfaces, semi-transparent white borders, and a single indigo-violet accent. The site positions Minardi as a credible, no-nonsense product professional who ships. It doesn't try to impress with flashiness; it impresses with restraint, clarity, and craft. Think: a PM who writes clean PRDs and ships products that matter.

---

## 2. Design Language

### Aesthetic Direction
**Linear Dark** — ultra-minimal dark mode, near-black canvas (#08090a), white-on-dark typography hierarchy, single indigo-violet accent (#7170ff). Not a dark theme slapped onto a light design — darkness is the native medium.

### Color Palette
| Role | Hex | Usage |
|------|-----|-------|
| Background | `#08090a` | Page canvas |
| Panel | `#0f1011` | Header, sidebar |
| Surface | `#191a1b` | Cards, elevated elements |
| Surface Hover | `#28282c` | Interactive hover states |
| Border Subtle | `rgba(255,255,255,0.05)` | Default borders |
| Border Standard | `rgba(255,255,255,0.08)` | Card borders, inputs |
| Text Primary | `#f7f8f8` | Headlines, key text |
| Text Secondary | `#d0d6e0` | Body text |
| Text Tertiary | `#8a8f98` | Muted text, descriptions |
| Text Quaternary | `#62666d` | Timestamps, metadata |
| Brand Indigo | `#5e6ad2` | CTA backgrounds |
| Accent Violet | `#7170ff` | Links, interactive accents |
| Accent Hover | `#828fff` | Hover state for accent |
| Success Green | `#10b981` | Status indicators |

### Typography
- **Primary**: Inter Variable (Google Fonts CDN substitute)
- **Mono**: JetBrains Mono
- **Font features**: `"cv01", "ss03"` — geometric alternates for cleaner aesthetic
- **Weights**: 300 (light body), 400 (reading), 510 (signature emphasis), 590 (strong)
- **Display sizes**: aggressive negative letter-spacing (-1.584px at 72px down to -0.288px at 24px)

### Spatial System
- Base unit: 8px
- Section padding: 80px vertical (desktop), 48px (mobile)
- Container max-width: 1200px
- Card padding: 24px
- Border radius: 6px (buttons), 8px (cards), 12px (panels)

### Motion Philosophy
- Entrance: fade-up on scroll, 400ms ease-out, 50ms stagger between items
- Hover: 150ms color/border transitions — snappy, not floaty
- No decorative animations — every motion serves navigation or feedback
- Page transitions: simple opacity fade

### Visual Assets
- Icons: Lucide icons (line style, consistent 1.5px stroke)
- No decorative background images — dark canvas IS the decoration
- Subtle gradient overlays on hero section (indigo glow, very faint)
- Portfolio: screenshot-style cards with subtle border

---

## 3. Layout & Structure

### Single Page Architecture (Anchor Navigation)
```
[Header - Sticky, minimal]
  Logo/Name (left) | Nav links (center) | CTA button (right)

[Hero Section - Full viewport height]
  Large display headline
  Subtitle (1-2 lines about positioning)
  Two CTAs: "View Work" + "Download CV"
  Subtle animated gradient glow behind headline

[About Section]
  Two-column: Text left, key facts right
  Headline + 2-3 paragraph bio
  Stats grid: Years experience, Products shipped, Industries

[Experience Section]
  Vertical timeline layout
  Each entry: Company, Role, Duration, Key achievements (bullet points)
  Subtle left-border accent line

[Portfolio Section]
  2-column grid of project cards
  Each card: Project name, category tag, brief description, key impact metric
  Hover: subtle border brightening + slight lift

[Skills/Toolkit Section]
  Horizontal pill/tag layout grouped by category
  Categories: Product, Design, Engineering, Data

[Contact Section]
  Centered, minimal
  Headline + brief call to action
  Social links: LinkedIn, Credly, Email
  Contact form (name, email, message)

[Footer - Minimal]
  Copyright, subtle top border
```

### Responsive Strategy
- Desktop (>1024px): Full layout, 2-column grids
- Tablet (768-1024px): Single column sections, reduced padding
- Mobile (<768px): Stacked layout, hamburger nav, full-width cards
- Breakpoints: 640px, 768px, 1024px, 1280px

---

## 4. Features & Interactions

### Navigation
- Sticky header on scroll (adds subtle border-bottom when scrolled)
- Smooth scroll to sections on nav click
- Active section highlighted in nav
- Mobile: hamburger menu → full-screen overlay nav

### Hero Section
- Display headline with negative letter-spacing
- Rotating/typing subtitle effect OR static powerful statement
- CTA buttons: primary (brand indigo) + ghost (transparent with border)
- Very subtle radial gradient glow behind text (indigo, 5-10% opacity)

### Portfolio Cards
- Hover: border transitions from `rgba(255,255,255,0.05)` to `rgba(255,255,255,0.12)`, subtle translateY(-2px)
- Click: expands to modal OR scrolls to detail section
- Category pills on each card

### Contact Form
- Fields: Name, Email, Message
- Validation: required fields, email format
- Submit: shows loading state → success message
- Error handling: inline field errors

### Scroll Animations
- Sections fade-in + translateY(20px → 0) on scroll into view
- Intersection Observer, 0.1 threshold

---

## 5. Component Inventory

### Header
- States: default (transparent bg), scrolled (panel bg + border)
- Logo: text mark "MD" or "Minardi" in Inter 510
- Nav links: Inter 13px 510, secondary text, hover → primary text
- CTA: ghost button style

### Hero Section
- Display headline: Inter 510, 72px (desktop), negative tracking
- Subtitle: Inter 400, 18px, secondary text color
- Primary CTA: brand indigo bg, white text, 6px radius
- Ghost CTA: transparent bg, white border, white text

### Section Header
- Overline label: Inter 12px 510, uppercase, tertiary text, tracking wide
- Section title: Inter 400, 32-48px, primary text, negative tracking
- Optional subtitle: Inter 400, 16px, secondary text

### Experience Card
- Left accent bar (2px, brand indigo)
- Company name: Inter 590, 17px
- Role + duration: Inter 400, 14px, tertiary text
- Achievements: bullet list, Inter 400, 15px, secondary text
- Border-left: subtle → visible on hover

### Portfolio Card
- Surface background with standard border
- Category pill (top-left)
- Project name: Inter 590, 18px
- Description: Inter 400, 14px, tertiary text
- Impact metric (optional): Inter 510, 13px, accent color
- Hover: border brightens, slight elevation

### Pill/Tag
- Background: transparent or rgba(255,255,255,0.05)
- Border: rgba(255,255,255,0.08)
- Text: Inter 510, 12px
- Border-radius: 9999px (pill)
- Categories get different subtle accent tints

### Contact Form Input
- Background: rgba(255,255,255,0.02)
- Border: rgba(255,255,255,0.08)
- Focus: border → accent violet
- Placeholder: quaternary text
- Error: red border + error message below

### Button
- Primary: bg brand indigo, text white, hover → accent hover
- Ghost: bg transparent, border rgba(255,255,255,0.08), text secondary
- Icon button: circle, 40px, ghost style

### Footer
- Top border: subtle
- Copyright: Inter 13px, quaternary text
- Social links: icon buttons, ghost style

---

## 6. Technical Approach

### Framework: Astro
- Static site generator, minimal JS by default
- Component-based architecture
- Output: pure HTML/CSS/JS for Firebase Hosting

### Deployment: Firebase Hosting
- Build command: `npm run build`
- Output directory: `dist`
- Deploy via Firebase CLI
- Free tier: 10GB storage, 360MB/day transfer

### Project Structure
```
/
├── public/
│   ├── favicon.svg
│   └── img/ (any static images)
├── src/
│   ├── components/
│   │   ├── Header.astro
│   │   ├── Hero.astro
│   │   ├── About.astro
│   │   ├── Experience.astro
│   │   ├── Portfolio.astro
│   │   ├── Skills.astro
│   │   ├── Contact.astro
│   │   ├── Footer.astro
│   │   └── ui/ (Button, Card, Pill, etc.)
│   ├── layouts/
│   │   └── Base.astro
│   ├── pages/
│   │   └── index.astro
│   └── styles/
│       └── global.css
├── firebase.json
├── astro.config.mjs
└── package.json
```

### Key Implementation Notes
- Use Astro's scoped CSS or CSS modules for component styles
- Global CSS for design tokens (CSS custom properties)
- Intersection Observer for scroll animations (vanilla JS)
- FormSubmit.co or similar for form handling (no backend needed)
- Lucide icons via CDN or inline SVG
- Google Fonts: Inter + JetBrains Mono via `<link>` preconnect

---

## Content Summary (from existing site)

### About
- Former Software Engineer → Product Manager
- 7+ years across Healthcare, HR, and Tech Solutions
- Key products: digital health solutions, mobile attendance, payroll management, workflow automation

### Experience (to be expanded)
- Healthcare: digital health, member advocacy, employee benefits
- HR: mobile attendance, payroll management
- Tech: business automation, workflow optimization

### Skills
- Product: Product strategy, Agile, User research, Data-driven decision making
- Engineering background (former SWE)
- Tools: (to be added based on actual stack)

### Contact
- LinkedIn: https://www.linkedin.com/in/minardidarmawan/
- Credly badges
- Email: (to confirm)
