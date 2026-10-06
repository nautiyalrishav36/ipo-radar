# IPO Radar — Final Automatic Website

This package contains the IPO Radar site plus the automatic SEBI public-issue detection pipeline.

Open `index.html` locally to preview the website.

For public deployment:
1. Upload the extracted files to a GitHub repository.
2. Keep `.github/workflows/ipo-auto-sync.yml` in the repository.
3. Import the repository into Vercel.
4. Replace `YOUR-DOMAIN.example` in canonical/sitemap/robots files after choosing the real domain.
5. Submit `sitemap.xml` in Google Search Console.

Automatic detection is based on official SEBI public-issue filings. A filing is not necessarily an open IPO; verify final issue dates/price/lot details before treating them as final. GMP is unofficial.
