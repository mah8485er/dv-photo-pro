[README-DV-Photo-Pro.txt](https://github.com/user-attachments/files/34937031/README-DV-Photo-Pro.txt)
DV-Photo-Pro — Phase 1 update
================================

This package contains the updated static website files for deployment on Vercel.

What changed
------------
1. Added a bilingual About Us page using the existing virtual-page/hash navigation.
2. Added a visible disclosure beside the Iraqi district/area field explaining that Google Translate receives the Arabic text entered for translation.
3. Updated the Arabic and English Privacy Policy to distinguish local photo processing from third-party address translation.
4. Corrected privacy statements in the footer, FAQ, metadata, and structured data so they do not claim that every feature is fully local.
5. Clarified that the photo tool uses user-positioned guide lines and does not automatically detect facial landmarks.
6. Softened unsupported guarantees/statistics in the bilingual articles.
7. Standardized canonical, Open Graph, structured-data, and share URLs on https://www.dv-photo-pro.com/.
8. Changed the Open Graph image reference to favicon.png, which is included in this package.
9. Removed fragment-only entries from sitemap.xml; only the canonical homepage is listed because the app currently uses hash-based virtual pages rather than separate crawlable HTML pages.
10. Added Referrer-Policy and Permissions-Policy headers in vercel.json. No restrictive Content-Security-Policy was added, to avoid breaking current third-party scripts and embeds.

Files changed
-------------
- index.html
- articles.js
- sitemap.xml
- vercel.json

Files retained
--------------
- favicon.png
- robots.txt

Validation performed
--------------------
- Node.js syntax check passed for the inline application JavaScript.
- Node.js syntax check passed for articles.js.
- HTML parsed successfully for structural inspection.
- No duplicate HTML id attributes were found.
- sitemap.xml parsed successfully.
- vercel.json parsed successfully.
- Confirmed About Us page, footer button, hash route, and address-translation disclosure are present.

Important limitation
--------------------
These checks are static/code checks. A full browser test of every interactive feature and a live Vercel deployment test have NOT been performed. Please deploy first as a Vercel Preview Deployment and test the photo tool, address generator, simulator, language switcher, articles, video, and browser back button before promoting to production.

Deployment
----------
Use the files in this ZIP as the project root. Keep the existing Vercel project settings and custom domains. Deploy as a Preview first; do not delete or replace the original project.
