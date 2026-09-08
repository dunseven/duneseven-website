# DUN-89 Part B — website drop, 7 September 2026

Upload: GitHub → Add file → Upload files → drag the CONTENTS of this folder
(not the folder itself) to the repo root. Commit to `main`. Wait 2 minutes for Netlify.

## Files in this drop (12)
| File | What changed |
| -- | -- |
| index.html | "Energy Mirror" → "The full Month — your energy story, gently reflected" (feature card + JSON-LD); Reset my day added to Free list; stray `category:"one-time"` removed from Offer schema |
| pricing/index.html | Pro card, FAQ and FAQ schema: "Energy Mirror" → full Month language; Reset my day added to Free card + FAQ |
| adhd-planner/index.html | Feature card heading + body |
| burnout-recovery/index.html | Feature card heading + body |
| mental-load/index.html | Feature card heading + body |
| shift-worker-planner/index.html | Feature card + "What does it cost?" FAQ |
| you-know-your-energy/index.html | Twitter card, og:image, BreadcrumbList schema, GTM noscript added |
| terms/index.html | "premium features" → "Pro features"; "one-time purchase" → "single purchase"; Twitter card + GTM noscript added |
| privacy-policy.html | "one-time Lifetime purchase" → "Lifetime purchase"; Twitter card + og:image added |
| sitemap.xml | lastmod set on every changed page; privacy-policy had none |
| og-image.jpg | NEW — every page already pointed at this file; it did not exist |
| DROP-NOTES.md | this file (safe to leave in repo or delete) |

## Delete from the repo root (GitHub → file → trash). Not done by upload.
- `files (3).zip`
- `sitemap (1).xml`
- `terms.html` (old duplicate — /terms/ is canonical; this one differs)
- `pillar-1-you-know-your-energy-blog (1).md`
- `privacy-policy-corrections.md`
- `story-section.html`

## After deploy — the ticket's "checked, not assumed" list
1. https://duneseven.com.au/og-image.jpg loads
2. Share https://duneseven.com.au/pricing/ into iMessage/Slack — image card appears
3. Search the live pricing page for "Energy Mirror" — zero hits
4. GA4 realtime (property 484774482) shows your visit
5. Search Console → URL inspection → request indexing on /pricing/ and /
6. PageSpeed Insights on / and /pricing/ (Core Web Vitals)
