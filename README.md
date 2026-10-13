# Moving Cost Calculator

A single-page calculator for estimating the full cost of buying a home in **England / Northern Ireland**, including SDLT (from April 2025), mortgage repayments, and monthly affordability.

## Features

- **SDLT calculation** — April 2025 bands for main residence (non-first-time buyer)
- **Capital breakdown** — cash savings + house sale proceeds (net of outstanding mortgage and 1% estate agent fee)
- **Mortgage repayment** — standard repayment formula over a configurable term (5–40 years)
- **LTV badge** — colour-coded good / ok / high indicator
- **Monthly affordability** — income vs. mortgage vs. custom expenses, with surplus/deficit
- **Custom expenses** — add/remove named monthly expenses that feed into affordability
- **Warnings** — flags deposit below 5%, insufficient capital, and unaffordable scenarios
- **Persistence** — all inputs and expenses saved to `localStorage` between sessions

## SDLT Bands (April 2025, main residence)

| Band | Rate |
|------|------|
| Up to £125,000 | 0% |
| £125,001 – £250,000 | 2% |
| £250,001 – £925,000 | 5% |
| £925,001 – £1,500,000 | 10% |
| Above £1,500,000 | 12% |

## Deployment

The app is a static `index.html` deployed to **Cloudflare Workers** using the Assets feature.

```bash
# Install Wrangler (if not already)
npm install -g wrangler

# Deploy
wrangler deploy
```

The `wrangler.jsonc` is already configured — no build step required.

## Local development

Open `index.html` directly in a browser, or serve it locally:

```bash
wrangler dev
# or
npx serve .
```

## Disclaimers

- Legal cost estimate is a rough approximation (conveyancer, searches, land registry, misc). Actual costs vary.
- Not financial advice.
