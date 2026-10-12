Hazard Hunt SEO update: extinguisher consolidation, 5 colour-band pages, internal links
Built on your latest repo zip. Contains ONLY new or changed files; copy them over the repo root.

NEW (6): blog/yellow-, cream-, red-, black-, blue-band-fire-extinguisher.html, vercel.json
REWRITTEN: blog/fire-extinguisher-colours-uk.html (now also holds the colour chart)
CHANGED: index.html (static guide links on the home screen only; game code untouched), sitemap.xml,
         blog/index.html, plus "Related guides" blocks and tighter meta descriptions on the other articles.

STEP 1: copy files over the repo root, replacing existing ones.
STEP 2: delete the retired page (the redirect in vercel.json covers its URL):
  git rm blog/fire-extinguisher-colour-chart.html
STEP 3:
  git add -A
  git commit -m "Consolidate extinguisher pages, add colour-band guides, internal links, redirect"
  git push

AFTER DEPLOY (Vercel):
  1. Open /blog/fire-extinguisher-colour-chart.html: it should land on /blog/fire-extinguisher-colours-uk.html.
  2. Search Console: Sitemaps -> resubmit sitemap.xml. URL Inspection -> Request indexing for the 6 pages
     (colours-uk and the five *-band-fire-extinguisher pages).
  3. Host check (important): Search Console shows your pages under www.hazardhunt.online, but every canonical,
     sitemap entry and og:url says hazardhunt.online (no www). In Vercel > Domains pick ONE as primary and
     redirect the other to it, then tell me which so I can align the canonicals.
