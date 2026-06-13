# Weekly Bathrooms

Marketing site for **Weekly Bathrooms** — Auckland's fast, fixed-price, productised bathroom renovation brand. *Bathrooms in weeks, not months.*

Backed by Add Value Renovations Ltd (Registered Master Builder, LBP).

## Pages

| File | Page |
|------|------|
| `index.html` | Home — positioning, the 4 week-tiers, how it works, FAQ |
| `quiz.html` | "Which week is your bathroom?" — 30-second quiz with instant indicative pricing → book a site check |
| `gallery.html` | Our bathrooms — filterable photo gallery with lightbox |
| `contact.html` | Contact — call/email/visit details, enquiry form, opening hours, and map |
| `wb-gallery-photos/` | Optimised gallery images (real Add Value Renovations projects) |

Static site — plain HTML/CSS/JS, no build step. Fonts load from Google Fonts; everything else is self-contained.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Deploy

Any static host works (GitHub Pages, Netlify, Cloudflare Pages). For GitHub Pages: Settings → Pages → deploy from `main` / root.

## Notes / TODO

- Tier prices in `quiz.html` (the `TIERS` object) and `index.html` are **indicative placeholders** pending QS sign-off.
- The lead forms in `quiz.html` and `contact.html` currently log the lead to the console and show a confirmation — wire both to a backend / Make.com webhook to capture live leads.
- Opening hours in `contact.html` (Mon–Fri 7am–5pm, Sat by appointment) are placeholders — confirm before going live.
- Gallery photos are labelled by suburb/type, not client name.

© Add Value Renovations Ltd · NZBN 9429041370285
