# Tecera Website

Static multi-page site for [tecerabiz.com](https://tecerabiz.com), hosted on Vercel.

## Structure

```
tecera-site/
├── index.html              Home                     -> https://tecerabiz.com/
├── life-sciences.html      Life Sciences            -> /life-sciences
├── about.html              Who We Are               -> /about
├── resources.html          Resources                -> /resources
├── privacy-policy.html     Privacy Policy           -> /privacy-policy
├── sitemap.xml             All pages with last-modified dates
├── robots.txt              Allows search engines and AI crawlers
├── llms.txt                Short summary of Tecera for AI assistants
├── llms-full.txt           Full plain-text content of every page
├── vercel.json             Clean URLs (no .html), headers, caching
└── assets/images/          Images (WebP for photos, PNG for logo/icons)
    ├── logo.png, icon-dsg.png, favicon.ico.png
    ├── hero-home.webp, stack-home.webp, hero-lifesciences.webp, fdc-image.webp
    └── og-image.png        1200x630 social share image
```

Each page is a full HTML file with its own title, description, canonical URL,
Open Graph tags and structured data (JSON-LD). Navigation uses real links, so
search engines and AI crawlers can discover every page without running JavaScript.
`vercel.json` sets `cleanUrls`, so `/about` serves `about.html`.

## Editing content

Shared parts (navigation, footer, contact modal, styles) appear in every page file.
If you change them, change all five files. Page-specific content lives inside the
`<div class="page active" id="page-...">` block of each file.

After any content change:
1. Update `<lastmod>` for that page in `sitemap.xml`.
2. Update `llms.txt` / `llms-full.txt` if the change affects what Tecera does or offers.
3. If the FAQ on the Life Sciences page changes, update the FAQ entries in that page's JSON-LD so they match the visible text.

## Deployment

Connected to `tecerabiz.com` via GoDaddy DNS. Auto-deploys on every push to `main`.

```
git add .
git commit -m "your message"
git push origin main
```

## External dependencies

| Asset | Purpose |
|-------|---------|
| Google Fonts (Poppins, Inter) | Typography |
| HubSpot embed (Portal: 247270811) | Contact form, captures to CRM |

## Key contacts
- Enquiries: info@tecerabiz.com
- HubSpot: [View submissions](https://app.hubspot.com/forms/247270811)
