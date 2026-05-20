# Serverless Capital — Website

Official website for **Serverless Capital**, a venture capital firm backing early-stage founders building serverless infrastructure, developer tools, and API-first products.

**Live site:** [serverlesscapital.com](https://serverlesscapital.com)

---

## Overview

This is a static single-page website built with pure HTML, CSS, and vanilla JavaScript. No build tools, no frameworks, no dependencies — just fast, portable HTML that deploys anywhere.

---

## Features

- **Responsive design** — Mobile-first, tested at 320px to 1440px+
- **Serene pastel design system** — Lavender, sage, and peach accent palette on a warm white base
- **Scroll reveal animations** — Intersection Observer-powered, respects `prefers-reduced-motion`
- **Accessible** — ARIA labels, keyboard navigation, focus styles, semantic HTML
- **SEO optimized** — Full meta tags, Open Graph, Twitter Card, canonical URL
- **AEO optimized** — FAQ section with `FAQPage` schema.org structured data
- **GEO optimized** — `llms.txt`, `Organization` schema, clear factual content structure for AI indexing
- **Performance** — Zero JS dependencies, CSS custom properties, Google Fonts preconnect
- **Google Analytics** — GA4 tag `G-PKEZQENKZH` integrated in `<head>`
- **Book a Call** — Integrated Google Calendar scheduling link throughout

---

## File Structure

```
serverlesscapital-website/
├── index.html        # Main website (single-page, includes GA4 tag)
├── robots.txt        # Search engine crawl rules (allows all bots incl. AI crawlers)
├── llms.txt          # GEO: Structured data for LLMs and AI search engines
└── README.md         # This file
```

### Recommended additions

```
├── sitemap.xml       # XML sitemap (reference in robots.txt)
├── og-image.png      # Open Graph image (1200×630px)
└── favicon.ico       # Favicon (currently using inline SVG data URI)
```

---

## Design System

### Color Palette

| Token | Value | Usage |
|---|---|---|
| `--bg` | `#FAFAF8` | Page background |
| `--bg-card` | `#F5F1FA` | Card backgrounds |
| `--bg-accent` | `#EDE8F5` | Purple tint areas |
| `--bg-sage` | `#EBF4F1` | Sage/green tint areas |
| `--bg-peach` | `#FDF0EA` | Peach tint areas |
| `--primary` | `#8E7DC0` | Primary brand (muted lavender) |
| `--sage` | `#7BA99E` | Secondary accent (sage) |
| `--peach` | `#E09070` | Tertiary accent (peach) |
| `--text` | `#252533` | Primary text |
| `--text-muted` | `#7A7A90` | Secondary text |

### Typography

- **Headings:** Playfair Display (serif) — Google Fonts
- **Body / UI:** Inter (sans-serif) — Google Fonts

---

## Sections

| Section | ID | Purpose |
|---|---|---|
| Navigation | `#nav` | Sticky top nav with Book a Call CTA |
| Hero | — | Main headline, subtext, dual CTA |
| Stats Bar | `#stats` | 4 key investment metrics |
| About | `#about` | Philosophy, values, visual cards |
| Thesis | `#thesis` | 3 investment categories |
| Investment Info | — | Check size, stage, geography details |
| Portfolio | `#portfolio` | Portfolio company cards |
| Process | `#process` | 4-step investment process |
| FAQ | `#faq` | Accordion FAQ (schema.org FAQPage) |
| CTA | — | Book a Call + email contact |
| Footer | — | Links, offices, legal |

---

## SEO / AEO / GEO Strategy

### SEO (Search Engine Optimization)
- Semantic HTML5 elements (`main`, `nav`, `section`, `article`, `footer`)
- Full `<meta>` tag coverage including description, keywords, author
- Open Graph and Twitter Card meta tags
- Canonical URL
- `robots.txt` with sitemap reference
- Google Analytics 4 (`G-PKEZQENKZH`) for traffic and conversion tracking

### AEO (Answer Engine Optimization)
- `FAQPage` schema.org JSON-LD with 5 common investor questions
- `Organization` schema.org JSON-LD
- `WebSite` schema.org JSON-LD
- Clear, structured, factual content written for featured snippet capture
- Heading hierarchy (`h1` → `h2` → `h3`) follows a logical answer structure

### GEO (Generative Engine Optimization)
- `llms.txt` at site root with comprehensive structured firm data
- Explicit, factual statements about check size, stage, geography, and team
- `ClaudeBot`, `GPTBot`, `PerplexityBot`, and other AI crawlers explicitly allowed in `robots.txt`
- Content structured for easy extraction by LLMs answering "What is Serverless Capital?"

---

## Deployment

This site is a static HTML file with no build step.

### Deploy to any static host

**Netlify (drag-and-drop)**
1. Go to [netlify.com](https://netlify.com)
2. Drag the `serverlesscapital-website/` folder to the deploy area

**Vercel**
```bash
npx vercel --prod
```

**GitHub Pages**
```bash
git init
git add .
git commit -m "Initial website"
git branch -M main
git remote add origin https://github.com/mohinishbasha/serverlesscapital-website.git
git push -u origin main
# Then enable GitHub Pages in repo Settings → Pages → Deploy from main branch
```

**Any web server / CDN**
```bash
# Just serve the directory
python3 -m http.server 3000
# or
npx serve .
```

---

## Local Development

No build step needed. Open `index.html` directly in a browser, or serve locally:

```bash
# Python
python3 -m http.server 3000

# Node.js
npx serve .

# VS Code
# Install "Live Server" extension → right-click index.html → Open with Live Server
```

---

## Contact

- **Book a Call:** [calendar.app.google/srj97v25ygCC6jtAA](https://calendar.app.google/srj97v25ygCC6jtAA)
- **Email:** hello@serverlesscapital.com
- **Offices:** Austin, TX · San Jose, CA · India

---

*Built for Serverless Capital · 2026*
