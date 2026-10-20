# Maverick Dizon — Portfolio

A clean, simple, mobile-friendly one-page portfolio for **Maverick Dizon**, a website builder who uses AI tools to design and launch websites for small businesses.

> I build clean, simple websites — fast.

## Features

- Single self-contained `index.html` (HTML, CSS and JavaScript inline): no build step, upload and go
- Sections: Hero, Projects, How I Work, About, Contact, Footer
- Sticky top menu with a mobile hamburger menu
- Smooth scrolling and subtle fade-in animations (respects reduced-motion settings)
- Responsive layout: project grid becomes one column on mobile
- Contact form with validation that opens the visitor's email app
- Minimal design: white background, dark gray text, deep blue accent (`#1E40AF`), rounded buttons, soft card shadows, [Inter](https://fonts.google.com/specimen/Inter) font

## Getting started

Open `index.html` in any browser. That's it.

## Customizing

Before publishing, replace the remaining placeholders in `index.html`:

| Placeholder | Replace with |
|---|---|
| `[City, Country]` | Your location |
| `[your@email.com]` | Your email (appears in the contact section **and** the `MY_EMAIL` constant in the script) |
| `[LinkedIn]`, `[Facebook]` | Your profile URLs |
| `[Year]` | Current year |
| `[Café website]` etc. | Real project names |
| `href="#"` on "View Site" buttons | Live project URLs |

**Accent color:** change `--accent` (and `--accent-hover`) in the `:root` block at the top of the stylesheet.

**Project images:** replace each `.card-img` placeholder `<div>` with an `<img>`. A comment in the CSS shows the exact markup.

**Contact form:** by default the form opens the visitor's email app. To receive submissions directly, create a free [Formspree](https://formspree.io) form and follow the comment above the `<form>` tag.

## Deployment

### GitHub Pages
1. Push this repository to GitHub (the repo must be public on a free account).
2. Go to **Settings → Pages**.
3. Set the source to the `main` branch, `/ (root)` folder, and save.
4. Your site will be live at `https://YOUR-USERNAME.github.io/maverick-dizon-portfolio/`.

### Any other host
Upload `index.html` to Netlify, Vercel, Hostinger, cPanel or any static host.

## Project structure

```
.
├── index.html   # The entire website
├── CLAUDE.md    # Project context for Claude / Claude Code
└── README.md    # This file
```

## Contact

Maverick Dizon · [your@email.com] · [LinkedIn] · [Facebook]
