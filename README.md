# IPO Radar India — Google-ready static website

This package is designed to be deployable on a static host such as Vercel or GitHub Pages.

## Included
- Search-engine-readable HTML pages (not only client-side JavaScript)
- Home page
- 26 upcoming IPO detail pages
- Current open IPO list + detail pages
- GMP explainer/tracker
- IPO calendar
- Subscription explainer
- Investment calculator
- About, Disclaimer, Privacy and Contact pages
- `robots.txt`
- `sitemap.xml`
- Canonical tags
- Open Graph metadata
- Favicon
- Mobile responsive design

## Important
This package cannot guarantee Google ranking or indexing. Google says a sitemap helps discovery but does not guarantee crawling/indexing, and rankings are not guaranteed. After deployment, verify the domain in Google Search Console, submit the sitemap, and use URL Inspection for important pages.

## Data
The 4 open IPO records and 26 upcoming names were populated from publicly visible market information checked on 6 Oct 2026. Upcoming dates/price bands are deliberately marked TBA unless available. Before public launch, verify every number against current official offer documents/exchange disclosures.

Primary verification sources:
- SEBI public issues: https://www.sebi.gov.in/filings/public-issues.html
- NSE public offer documents: https://www.nseindia.com/static/products-services/public-offer-documents

## Publishing
1. Upload the complete folder to a GitHub repository.
2. Import the repository into Vercel or use GitHub Pages.
3. Replace `YOUR-DOMAIN.example` in `canonical`, `robots.txt`, and `sitemap.xml` with your actual domain.
4. Deploy.
5. Add the site to Google Search Console and submit `/sitemap.xml`.
6. Replace the placeholder email on `contact.html`.
7. Add a real database/admin backend before promising live updates.

## Live data architecture for production
For automatic updates, connect:
Frontend -> API/backend -> database -> verified/licensed data source.
Do not scrape or republish another site's database without permission. Prefer official exchange/regulatory data or a licensed provider.

## Legal/financial
The site is informational, not investment advice. GMP is unofficial. Keep disclaimers visible and current.
