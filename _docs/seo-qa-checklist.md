# Cherry Creek Machine — SEO QA Checklist
## Run this before every deploy

### Every New Page Must Have:
- [ ] Unique `<title>` tag (50–65 characters, includes primary keyword + "Tulsa, OK" + "Cherry Creek Machine")
- [ ] Unique `<meta name="description">` (140–160 characters)
- [ ] One `<h1>` tag per page — includes primary keyword and geo
- [ ] `<link rel="canonical">` pointing to https://ccmachine.com/[slug]/ (non-www, trailing slash)
- [ ] NO `<meta name="robots" content="noindex">` unless it's a utility page (thank-you, etc.)
- [ ] Added to sitemap.xml (unless noindex)
- [ ] JSON-LD schema block (minimum: BreadcrumbList for inner pages; FAQPage for service pages)
- [ ] OG tags (og:title, og:description, og:image, og:url)
- [ ] Internal link from at least one other page on the site
- [ ] Nav or footer link if it's a primary page

### Redirect Rules (_redirects):
- [ ] Old URLs redirect 301 to new canonical URL
- [ ] No redirect chains (A→B→C — always fix to A→C)
- [ ] /quote and /contact point to /request-a-quote/

### Domain Consistency:
- [ ] All canonical tags use https://ccmachine.com/ (non-www)
- [ ] All sitemap URLs use https://ccmachine.com/ (non-www)
- [ ] netlify.toml has www→non-www 301 redirect

### Images:
- [ ] OG image hosted at https://ccmachine.com/og-image.jpg (not on Squarespace CDN)
- [ ] All below-fold images have loading="lazy"

### Form/CTA:
- [ ] Primary CTA points to /request-a-quote/
- [ ] Netlify form has data-netlify="true" and unique name attribute

### After Deploy:
- [ ] Submit updated sitemap in Google Search Console
- [ ] Request indexing for new/updated pages via GSC URL Inspection
- [ ] Validate schema at https://validator.schema.org/
- [ ] Test meta tags at https://metatags.io/
- [ ] Run PageSpeed Insights on mobile: https://pagespeed.web.dev/
