# Deploying the SEO update and submitting to search engines

## 1. Deploy
1. In your local `tecera-site` repo, copy in every file from this package (overwrite when asked).
   Keep your existing `assets/images/` files, including `favicon.ico.png`.
2. Commit and push:
   git add .
   git commit -m "Pre-rendered pages, structured data, sitemap and AI-crawler files"
   git push origin main
3. After Vercel deploys (about 30 seconds), check in a browser:
   - https://tecerabiz.com/about , /life-sciences , /resources , /privacy-policy each load the right page
   - https://tecerabiz.com/sitemap.xml , /robots.txt , /llms.txt , /llms-full.txt open as plain files
   - Right-click > View Page Source on /about: the title should say "About Tecera"

## 2. Google Search Console (search.google.com/search-console)
1. Add property > Domain > tecerabiz.com. Verify with the DNS TXT record in GoDaddy.
2. Sitemaps > submit `sitemap.xml`.
3. URL Inspection > enter each of the five URLs > Request Indexing.
4. Check structured data: https://search.google.com/test/rich-results with /life-sciences (FAQ) and / (Organization).

## 3. Bing Webmaster Tools (bing.com/webmasters)
Bing's index feeds ChatGPT search and Microsoft Copilot.
1. Sign in > "Import from Google Search Console" (fastest), or add the site and verify by DNS.
2. Sitemaps > submit https://tecerabiz.com/sitemap.xml
3. URL Submission > submit the five URLs.

## 4. Social preview check
Paste https://tecerabiz.com into the LinkedIn Post Inspector (linkedin.com/post-inspector) to refresh the share image.

## 5. Keep it current
When a page changes, update its `<lastmod>` in sitemap.xml and, if relevant, llms.txt / llms-full.txt.
