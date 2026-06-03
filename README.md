# HR Junkie Landing Page

A lightweight, SEO-friendly marketing site for **HR Junkie**, converted from the Figma design (`HR_Junkie.fig`).

**Live demo:** [https://hr-junk.netlify.app](https://hr-junk.netlify.app)

## Stack

- **[Astro](https://astro.build)** — ships zero JavaScript by default; static HTML for excellent SEO and performance
- **Tailwind CSS v4** — utility styling aligned with the Figma navy/blue palette
- **Plus Jakarta Sans** — modern sans-serif typography

## Getting started

```bash
cd hr-junkie
npm install
npm run dev
```

Open [http://localhost:4321](http://localhost:4321).

## Build for production

```bash
npm run build
npm run preview
```

Output is in `dist/` — deploy to any static host (Vercel, Netlify, Cloudflare Pages, etc.). This site is deployed on **Netlify** at [hr-junk.netlify.app](https://hr-junk.netlify.app).

## Performance

- **Optimized imagery** — all photos/illustrations are served as resized **WebP** (originals were oversized PNG/JPEG and base64-in-SVG assets). This cut the image payload from **~13 MB to ~600 KB (~95% smaller)**.
- **Fast LCP** — the above-the-fold hero image loads eagerly with `fetchpriority="high"`; all other images are `loading="lazy"` + `decoding="async"`.
- **No layout shift** — images carry explicit `width`/`height` (or fixed aspect boxes) to reserve space and avoid CLS.
- **Zero client JS by default** — Astro renders static HTML, so pages are interactive immediately.

## Project structure

```
src/
  components/   # Header, Hero, feature sections, footer
  layouts/    # BaseLayout with SEO meta tags
  pages/      # index.astro (landing page)
public/
  images/     # Assets exported from Figma
```

## Design sections (aligned with Figma / Body.png)

1. Navigation — Platform, Solutions, Resources, Pricing
2. Hero — “We make HR & Payroll work across borders” + Cross Border video
3. Feature grid — light-blue bordered 2×2 cards
4. Alternating features — Payroll, Compliance, Workflows (6 icons), Employee
5. Navy promo banners — yellow “Get Started” CTAs
6. Mobile app — store badges + 3 phone mockups
7. Resources — 3 blog cards
8. Pre-footer — newsletter + “Work Made Simple, Lives Made Better.”
9. Footer — logo, social, link columns, compliance badges
