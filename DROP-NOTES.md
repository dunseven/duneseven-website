# DUN-103 + DUN-89 audit drop — 9 September 2026

Upload: GitHub → Add file → Upload files → drag the CONTENTS of this folder
(not the folder itself) to the repo root. Commit to `main`. Wait 2 minutes for Netlify.

## Files in this drop (12)
| File | What changed |
| -- | -- |
| about/index.html | Instagram → @dune_seven_adhd_planner (footer + Organization sameAs); `motto_viewed` GA4 dataLayer event when "We are human because you are." is on screen |
| index.html | Instagram fix (footer + sameAs); Lifetime Offer schema now carries `priceValidUntil: 2026-12-31` (matches /pricing/) |
| pricing/index.html, adhd-planner/, mental-load/, burnout-recovery/, privacy-policy.html | Instagram link fix |
| postpartum-planner/index.html, shift-worker-planner/index.html | Instagram fix; `&mdash;` inside FAQ JSON-LD replaced with a real em dash (Google reads JSON-LD literally — it was showing "&mdash;" in rich results) |
| burnout-recovery/index.html | `&amp;` inside BreadcrumbList JSON-LD → "&" |
| _redirects | `/terms.html` → `/terms/` 301 (the stale duplicate is retired) |
| sitemap.xml | lastmod 2026-09-09 on every changed page |
| DROP-NOTES.md | this file |

## Delete from the repo root (GitHub → file → trash). Upload does not do this.
- `terms.html` — stale duplicate: canonical pointed at www, still said "premium features" and "one-time purchase", no GTM, no Twitter card. Flagged 7 Sep, still live. The redirect above covers the URL either way.

## GTM — 2 minutes, one time (makes `motto_viewed` reach GA4)
1. GTM container GTM-WHG8SCQM → Triggers → New → Custom Event → Event name `motto_viewed` → save.
2. Tags → New → Google Analytics: GA4 Event → Measurement ID G-QE5808CHPM → Event name `motto_viewed` → parameter `motto_placement` = `{{Event}}`-free value `about_closer` (or leave params off) → trigger = the one above → save → Publish.
3. Realtime in GA4 (property 484774482): open /about/, scroll to the closing line → `motto_viewed` appears.

## After deploy — checked, not assumed
1. https://duneseven.com.au/terms.html → lands on /terms/
2. Footer "Instagram" on any page → opens @dune_seven_adhd_planner
3. Rich Results Test on /shift-worker-planner/ and /postpartum-planner/ — FAQ answers show "—", not "&mdash;"
4. Search Console → URL inspection → request indexing on /about/
5. PageSpeed Insights on /about/ (Core Web Vitals)
