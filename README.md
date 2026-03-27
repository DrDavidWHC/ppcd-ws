# ppcd-astro

PPC Dentist website — Astro 4.x + Tailwind CSS, deployed to Cloudflare Pages.

## Setup

```bash
npm install
npm run dev
```

## Deploy to Cloudflare Pages

1. Push to GitHub
2. Connect repo in Cloudflare Pages dashboard
3. Build command: `npm run build`
4. Build output directory: `dist`

## Adding GHL Form Integration (Future)

When ready to wire forms to GoHighLevel:

1. `npx astro add cloudflare` — adds the CF Pages adapter
2. Create `src/pages/api/contact.ts` as a Cloudflare Pages Function
3. POST form data to GHL webhook URL (store in CF environment variables)
4. Update form `action` attributes to point to `/api/contact`

## Project Structure

```
src/
  layouts/
    Layout.astro          # Shared nav + footer
  pages/
    index.astro           # Home
    about.astro           # About Dr. Wank
    hipaa-compliant-call-tracking.astro
    hipaa-compliant-website-forms.astro
    practice-health-guides.astro
    practice-health-guides-tos.astro
    contact.astro
    privacy.astro
    tos.astro
    accessibility.astro
    404.astro
public/
  logo-dark.png           # Dark bg logo (footer)
  logo-light.png          # Light bg logo (nav)
  _redirects              # Cloudflare redirects
  _headers                # Security headers
  robots.txt
  sitemap.xml
```

## Brand Colors

| Name  | Hex       | Usage                    |
|-------|-----------|--------------------------|
| Slate | `#4a5f7a` | Primary / nav / footer   |
| Red   | `#e8294a` | CTA buttons / accents    |
| Teal  | `#2ab8b8` | Secondary accent         |
| Lime  | `#8dc63f` | Tertiary accent          |
| Dark  | `#111111` | Footer background        |

## Fonts

- **Syne** (display/headings) — via Google Fonts
- **DM Sans** (body) — via Google Fonts
