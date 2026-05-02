# CVJobMatch Landing Pages Deployment

This repository contains SEO landing pages for **CVJobMatch.ai**.

The landing pages must be deployed to **Vercel**, because Vercel is the platform currently controlling and serving the main `cvjobmatch.ai` website.

## Goal

Deploy all SEO landing pages so they are live on:

https://www.cvjobmatch.ai/

Each landing page should have its own clean URL, for example:

https://www.cvjobmatch.ai/resume-keywords-for-icu-nurse  
https://www.cvjobmatch.ai/resume-keywords-for-marine-electrician  
https://www.cvjobmatch.ai/not-getting-interviews  

## Owner

Tico will handle the deployment.

## Important SEO Requirements

Each landing page should keep:

- A unique `<title>`
- A unique `<meta name="description">`
- A correct canonical URL
- Clean URL structure without `.html` when possible
- Article schema where included
- FAQPage schema where included
- Internal links to related pages
- CTA links pointing to the main CVJobMatch tool or relevant matching page
- Mobile-friendly viewport settings

## URL Format

Use clean URLs:

/resume-keywords-for-icu-nurse  
/resume-keywords-for-investment-analyst  
/maritime-resume-guide  
/not-getting-interviews  

Avoid mixing formats such as:

/resume-keywords-for-icu-nurse.html

Unless the current Vercel setup requires `.html`.

## Deployment Platform

Deploy using **Vercel**.

The project connected to Vercel is the one that controls:

cvjobmatch.ai  
www.cvjobmatch.ai  

## Deployment Checklist

Before deploying, confirm that:

- [ ] All landing pages are added to the correct Vercel project
- [ ] URLs match the canonical URLs in each page
- [ ] No duplicate canonical URLs exist
- [ ] Internal links are working
- [ ] CTA links are working
- [ ] Pages return HTTP 200
- [ ] No important page is accidentally blocked by `robots.txt`
- [ ] `sitemap.xml` is updated whenever pages are added, removed, renamed, or changed
- [ ] The updated `sitemap.xml` is deployed with the site
- [ ] Google Search Console can discover the new URLs
- [ ] The updated sitemap is submitted in Google Search Console after deployment

## Sitemap Requirement

Every time landing pages are added, removed, renamed, or updated, the sitemap must also be updated.

The sitemap should be available at:

https://www.cvjobmatch.ai/sitemap.xml

Each important landing page should be included in the sitemap with the final canonical URL.

Example sitemap entry:

<url>
  <loc>https://www.cvjobmatch.ai/resume-keywords-for-icu-nurse</loc>
  <lastmod>2026-05-02</lastmod>
</url>

Use the real deployment date for `<lastmod>`.

## Google Search Console

After deployment:

1. Open Google Search Console
2. Submit the updated sitemap:

https://www.cvjobmatch.ai/sitemap.xml

3. Inspect several new or updated URLs
4. Request indexing for important pages
5. Check for indexing errors after a few days
6. Confirm that Google can read the canonical URL correctly

## Suggested Folder Structure

Depending on the existing project setup, landing pages can be placed in a structure like:

/pages
  /resume-keywords-for-icu-nurse
  /resume-keywords-for-marine-electrician
  /resume-keywords-for-investment-analyst
  /not-getting-interviews
  /maritime-resume-guide

Or, if the project is static HTML:

/public
  resume-keywords-for-icu-nurse.html
  resume-keywords-for-marine-electrician.html
  resume-keywords-for-investment-analyst.html
  not-getting-interviews.html
  maritime-resume-guide.html

If using static `.html` files, make sure Vercel routing or redirects support the clean canonical URLs.

## Recommended Vercel Redirects

If files are deployed as `.html`, add redirects so clean URLs work:

{
  "redirects": [
    {
      "source": "/resume-keywords-for-icu-nurse.html",
      "destination": "/resume-keywords-for-icu-nurse",
      "permanent": true
    }
  ]
}

Also make sure the clean URL serves the correct page.

## Internal Linking

These landing pages are important for programmatic SEO. They should not be deployed as disconnected pages with no internal links.

Every page should be reachable through internal links from hub pages such as:

/resume-keywords-for-jobs  
/healthcare-resume-keywords  
/maritime-resume-keywords  
/finance-resume-keywords  
/ats-resume-checker  

## Final SEO Deployment Steps

After each deployment:

- [ ] Confirm Vercel deployment succeeded
- [ ] Open several landing pages manually
- [ ] Check canonical URLs
- [ ] Check internal links
- [ ] Check CTA links
- [ ] Open `https://www.cvjobmatch.ai/sitemap.xml`
- [ ] Confirm new or updated URLs are listed
- [ ] Submit sitemap in Google Search Console
- [ ] Request indexing for priority pages
- [ ] Monitor Google Search Console for coverage and indexing issues

## Deployment Responsible

Tico is responsible for deploying the landing pages to Vercel and making sure the updated `sitemap.xml` is submitted in Google Search Console.
