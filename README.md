# Roohiluna — Handcrafted Cotton-Yarn Lampshades

> Sculptural Light. Handwoven Soul.

A fully self-contained wholesale website for **Roohiluna Handicrafts**, an artisan lampshade brand handcrafted in India.

## Live Site

Hosted via GitHub Pages: [https://raihana1mran.github.io/Roohiluna](https://raihana1mran.github.io/Roohiluna)

## Features

- **10 lampshade designs** with wholesale pricing in KWD
- **Multi-currency estimator** — live exchange rates via ExchangeRate-API (15 currencies)
- **Custom colour palette builder** — 2, 4 or 6 colours per shade with hex code input
- **Wholesale estimation form** — generates a quotation emailed to sales@roohiluna.com
- **Sample cart** — 280 KWD per sample with free shipping, Stripe checkout
- **AI sales chatbot** powered by Claude
- **PDF wholesale catalogue** — downloadable 7-page catalogue
- **7 policy pages** — company profile, wholesale/MOQ, T&Cs, shipping, returns, privacy, contact
- **Founders section** with portraits
- **Scroll animations**, infinite marquee, hero lamp light animation
- Fully responsive on mobile, tablet and desktop

## Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | Tailwind CSS (CDN) |
| Fonts | Syne + Plus Jakarta Sans (Google Fonts) |
| JavaScript | Vanilla JS (no framework) |
| Exchange rates | ExchangeRate-API (free tier) |
| Chatbot | Anthropic Claude API |
| Checkout | Stripe Payment Link |
| PDF | Embedded base64 (ReportLab) |
| Hosting | GitHub Pages |

## Project Structure

```
/
├── index.html        # Complete self-contained site (images embedded as base64)
└── README.md
```

All images, fonts fallbacks, product drawings and the PDF catalogue are embedded directly inside `index.html` so no additional assets or build step are required.

## Configuration

Before going live, open `index.html` and update these values inside the main `<script>` block:

```js
var CFG = {
  STRIPE_LINK: "",          // ← Your Stripe Payment Link URL
  EMAIL: "sales@roohiluna.com"
};
var RATES_KEY = "77f5d16bc2a40e991a06f7b4"; // ← Your ExchangeRate-API key
```

And inside the Claude chatbot `<script>` block, the API call goes directly to Anthropic. For production, route it through a server-side function to keep your API key private.

## Deployment (GitHub Pages)

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set Source to **Deploy from branch → main → / (root)**
4. Save — the site goes live at `https://raihana1mran.github.io/Roohiluna`

## Contact

**sales@roohiluna.com**

---

*Handcrafted in India · Made for the world*
