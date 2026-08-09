# Car Fund Tracker

A standalone, single-page PWA for tracking a 21-week car-savings plan: one week to
pay off a debt, then 20 weekly $250 deposits toward a $5,000 car fund.

Live at: https://quavv-pixel.github.io/car-fund-tracker-/ (once GitHub Pages is
turned on for this repo — see below).

## What's here

- `index.html` — the entire app. No build step, no dependencies, no framework —
  plain HTML/CSS/JS. Progress (checked weeks) is saved to `localStorage` on the
  device.
- `manifest.json` + `icons/` — makes it installable to a phone home screen as
  its own app.
- `.github/workflows/deploy-pages.yml` — deploys this repo straight to GitHub
  Pages on every push to `main`. No build step, so it just publishes the repo
  as-is.

## One-time setup to go live

This repo's files and workflow are ready, but GitHub requires a repo owner
(not a bot token) to flip one setting the first time a repo's Pages site is
turned on:

1. Go to **Settings → Pages** on this repo
2. Under **Build and deployment → Source**, choose **GitHub Actions**

After that, every push to `main` deploys automatically.

## Running it locally

Open `index.html` directly in a browser, or serve the folder with any static
file server, e.g. `npx serve .`

## Editing the plan

All the numbers that drive the tracker (gross pay, tax rate, weekly savings
amount, bills/rides/food budget, the $5,000 goal, the debt amount, and the
Jun 17 2026 start date) live at the top of the `<script>` block in
`index.html` as named constants. Milestone dates and the footer date range
are computed from those constants — change a number once and every
date/label on the page follows.
