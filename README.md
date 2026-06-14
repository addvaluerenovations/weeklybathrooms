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
- The quiz refines each tier's "from" price into an **estimate range** from a few scoping questions (size, layout, condition, extras). The multipliers/add-ons live in the `SCOPE` array and `SPREAD` object in `quiz.html` and are **placeholders — tune them with the QS** before relying on the numbers.
- Choosing a package on the home page deep-links to `quiz.html?tier=N`, which skips the matching questions and goes straight to the scoping step for a tailored estimate.
- **The quiz gates the estimate behind a contact form**: the customer enters name/phone/email, the full quote (package, estimate range, their answers) is emailed to the team, and only then is the estimate revealed on screen.
- **Email delivery is via [Web3Forms](https://web3forms.com)** (free plan — browser submissions only). Both `quiz.html` (`LEAD.accessKey`) and `contact.html` (`WEB3FORMS_KEY`) post to `https://api.web3forms.com/submit` with the same access key; quiz leads use the subject "New Weekly Bathrooms quote enquiry", contact leads use "New Weekly Bathrooms contact enquiry". To use separate keys/inboxes, just replace the key in each file. Note: Web3Forms rejects server-side test posts on the free plan — verify by submitting the live form in a browser.
- Opening hours in `contact.html` (Mon–Fri 7am–5pm, Sat by appointment) are placeholders — confirm before going live.
- Gallery photos are labelled by suburb/type, not client name.

© Add Value Renovations Ltd · NZBN 9429041370285
