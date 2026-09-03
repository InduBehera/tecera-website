# Tecera Website

Single-file SPA for [tecerabiz.com](https://tecerabiz.com)

## Structure

```
tecera-site/
├── index.html          ← Main website (self-contained SPA)
├── assets/
│   └── images/         ← Source images (embedded as base64 in index.html)
│       ├── logo.png              (10 KB)  Nav logo
│       ├── hero-home.png         (203 KB) Home page hero
│       ├── stack-home.jpg        (94 KB)  Built on Your Stack section
│       ├── icon-dsg.png          (1 KB)   Data Security icon
│       ├── hero-lifesciences.png (223 KB) Life Sciences hero
│       └── fdc-image.png         (1 MB)   Forward-Deployed Consultants
└── README.md
```

## Pages
- **Home** — Hero, What We Do, Built on Your Stack, Data Security, Track Record, CTA
- **Life Sciences** — Services, Market Research, How We Work, FAQ
- **About** — Beliefs, Team, Careers, Work With Us
- **Privacy Policy** — GDPR-compliant, Last Modified Sept 04 2026

## External Dependencies
| Asset | Purpose |
|-------|---------|
| Google Fonts (Poppins, Inter) | Typography |
| HubSpot embed (Portal: 247270811) | Contact form — captures to CRM |

## Deployment
Hosted on Vercel. Connected to `tecerabiz.com` via GoDaddy DNS.
Auto-deploys on every push to `main`.

## To update the site
1. Edit `index.html`
2. `git add . && git commit -m "your message"`
3. `git push origin main`
Vercel deploys automatically within ~30 seconds.

## Key contacts
- Enquiries: info@tecerabiz.com
- HubSpot: [View submissions](https://app.hubspot.com/forms/247270811)
