# IPO Radar — Automatic IPO Data System

This version adds an automatic SEBI filing detector. GitHub Actions checks the SEBI Public Issues page every 6 hours, adds newly detected DRHP/draft filing companies to `data/ipo-data.json`, and regenerates `auto-ipo-pipeline.html`.

## What is automatic
- New DRHP/draft public-issue filing detection from SEBI
- Deduplication by company slug
- Automatic timestamp and source URL
- Automatic pipeline page regeneration
- Git commit + Vercel/GitHub Pages deployment can publish the change

## What is intentionally NOT guessed
A SEBI filing does not necessarily mean the IPO will open soon. The bot therefore does not invent price bands, dates, lot sizes or GMP. Those fields remain TBA until verified.

## Make it live
1. Create a GitHub repository and upload this entire folder.
2. Connect that repository to Vercel (free tier is enough for the static site).
3. GitHub Actions will run automatically every 6 hours. You can also run it manually from **Actions → Automatic IPO Data Sync → Run workflow**.
4. Every successful sync commits the updated JSON/page; Vercel automatically redeploys the change.

## Important
- The workflow uses public SEBI pages and should be treated as a detector, not a licensed market-data feed.
- Respect source terms and rate limits. Do not scrape aggressively.
- For fully automatic price bands, subscription, listing dates and GMP, use a reliable/licensed market-data API or official exchange feed. Do not copy another publisher's private database.
