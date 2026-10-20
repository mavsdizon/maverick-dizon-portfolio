# CLAUDE.md

Project context for Claude when working in this repository.

## Project

One-page portfolio website for **Maverick Dizon**, a website builder who uses AI tools to design and launch clean, simple websites for small businesses.

- Headline: "I build clean, simple websites — fast"
- Audience: small business owners looking for a quick, professional website

## Hard constraints

- **Everything lives in a single file: `index.html`.** HTML, CSS (in `<style>`) and JavaScript (in `<script>`) stay inline so the file can be uploaded directly to any host. Do not split into separate CSS/JS files or add a build step, framework, or package manager.
- No external dependencies except the Google Font (Inter).
- Must stay mobile-friendly. Breakpoints: `900px` (steps → 2 columns, contact stacks) and `680px` (single column, hamburger menu).

## Page structure (in order)

1. **Sticky nav**: logo (name), links to Work / Process / About / Contact; hamburger menu on mobile
2. **Hero**: name badge, headline, AI-tools subline, "View My Work" button → `#projects`, location
3. **Projects** (`#projects`): 4 cards in a 2-column grid (1 on mobile): image placeholder, name, one-line description, "View Site" button
4. **How I Work** (`#process`): 4 steps with inline SVG icons: Brief, Build with AI, Refine, Launch
5. **About** (`#about`): short friendly paragraphs on clean design and quick delivery
6. **Contact** (`#contact`): email, LinkedIn, Facebook links + form (name, email, message)
7. **Footer**: © year + name

## Design system

Defined as CSS variables in `:root`. Change values there rather than hardcoding colors.

| Token | Value | Use |
|---|---|---|
| `--accent` | `#1E40AF` (deep blue) | Buttons, links, highlights; the only accent color |
| `--accent-hover` | `#1E3A8A` | Button hover |
| `--accent-soft` | `#EEF2FF` | Icon backgrounds, name badge |
| `--text` | `#1F2937` | Dark gray body text |
| `--text-muted` | `#6B7280` | Secondary text |
| `--bg` / `--bg-alt` | `#FFFFFF` / `#F9FAFB` | Page / alternating sections |
| `--radius` | `14px` | Cards |

Style rules: minimal and modern, lots of white space, white background, rounded (pill) buttons, soft shadows on cards, Inter font. Keep it simple; avoid adding new colors or heavy effects.

## Behavior (JavaScript)

- Smooth scrolling via CSS `scroll-behavior` with `scroll-padding-top` for the sticky nav
- Nav gets a border/shadow after scrolling (`.scrolled`)
- Mobile menu toggle closes when a link is clicked
- `.reveal` elements fade in via IntersectionObserver (disabled under `prefers-reduced-motion`)
- Contact form validates fields, then opens a `mailto:` link to `MY_EMAIL` (constant at the top of the script). There is no backend. To switch to Formspree, follow the HTML comment above the form.

## Still to fill in

These placeholders remain in `index.html`. Replace **every** occurrence (the email also appears in the `MY_EMAIL` constant):

- `[City, Country]`
- `[your@email.com]`
- `[LinkedIn]` and `[Facebook]` (profile URLs)
- `[Year]`
- Project names: `[Café website]`, `[Salon website]`, `[Freelancer page]`, `[Event landing page]`
- Each "View Site" button's `href="#"` → live project URL
- Project image placeholders (`.card-img` divs) → real screenshots (see the CSS comment on `.card-img`)

## Deployment

Static site: no build. Host on GitHub Pages (Settings → Pages → source `main`, root) or by uploading `index.html` to any web host.

## Working conventions

- Make small, targeted edits; don't rewrite the whole file for a single change.
- After edits, check that the layout still works at mobile width.
- Commit messages: short, imperative (e.g. "Add café project link").
