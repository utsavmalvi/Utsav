# Dr. Pooper Septic Treatments — Website

A clean, fast, mobile-friendly marketing site for the **Dr. Pooper Septic Treatments**
brand. Built as a static site (HTML + CSS + vanilla JS) with all purchase buttons
linking to the official Amazon storefront.

## Structure

```
.
├── index.html        # The full single-page site
├── css/styles.css    # All styling (design tokens, responsive layout)
├── js/main.js        # Mobile nav, footer year, scroll reveal
└── README.md
```

## Sections

- **Hero** — headline, value prop, primary "Shop on Amazon" CTA
- **Trust bar** — quick benefit highlights
- **Products** — three featured treatments, each linking to Amazon
- **How It Works** — 3-step explanation
- **Benefits** — six key reasons to buy
- **Reviews** — illustrative testimonials (point customers to verified Amazon reviews)
- **FAQ** — common questions
- **Footer** — links + legal fine print

## Run locally

It's a static site — just open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

Any static host works. Easiest options:

- **Netlify / Vercel / Cloudflare Pages** — point it at the repo, no build
  command needed, publish directory is the project root. With Netlify you can
  also just drag-and-drop the project folder at https://app.netlify.com/drop.
- **GitHub Pages** — a ready-made workflow exists at
  `.github/workflows/deploy-pages.yml`. First enable Pages
  (Settings → Pages → Source: "GitHub Actions"), then run the
  "Deploy to GitHub Pages" workflow from the Actions tab.

## Customize

- **Links:** All Amazon URLs live in `index.html`. Update the storefront URL and
  the per-product `https://www.amazon.com/dp/<ASIN>` links to match your real listings.
- **Products:** Edit the three `.product-card` blocks (names, descriptions, features).
- **Copy & reviews:** The product blurbs and testimonials are placeholders written
  to fit the brand — swap in your real copy and verified review quotes.
- **Colors/fonts:** Tweak the CSS variables at the top of `css/styles.css`.
- **Images:** The site uses emoji as lightweight placeholders. Drop real product
  photos into an `images/` folder and replace the `.product-media`/`.hero-emoji` spans.

> Note: Product descriptions and reviews are illustrative placeholders, since the
> live Amazon storefront content couldn't be scraped automatically. Replace them
> with your official product details before publishing.
