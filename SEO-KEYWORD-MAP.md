# Dune Seven — SEO keyword map (v1.3.0 hard launch)

One page, one intent. No two pages target the same primary keyword — that's what causes cannibalisation.

---

## / (Home)
**Primary:** ADHD planner app
**Secondary:** daily planner app ADHD, energy planner, planner for overwhelm
**H1:** Plan around your energy, not your guilt.
**Job:** brand + conversion. Sends traffic out to the four pillars.

## /adhd-planner/
**Primary:** ADHD planner app Australia
**Secondary:** executive dysfunction app, time blindness app, planner for planning paralysis, task initiation app, ADHD planner free
**H1:** An ADHD planner that works with your brain, not against it
**Intent:** high — people actively searching for a tool.

## /mental-load/
**Primary:** mental load app
**Secondary:** mental load of motherhood, invisible labour, mental load tracker, app to reduce mental load
**H1:** A place to put the mental load down
**Intent:** mixed informational/commercial. Strong social-share page.

## /burnout-recovery/
**Primary:** burnout recovery planner
**Secondary:** planner for overwhelm, low energy planner, planner for when you're overwhelmed, gentle productivity app
**H1:** Planning through burnout, when the list is the problem
**Intent:** informational-leaning. Longest tail, least competition.

## /postpartum-planner/
**Primary:** postpartum planner app
**Secondary:** baby brain, postpartum brain fog, planner for new mums, fourth trimester organisation
**H1:** Postpartum, with a brain that isn't quite yours yet
**Intent:** high emotional resonance. Your best organic-social page.

## /pricing/
**Primary:** Dune Seven Planner pricing
**Secondary:** free ADHD planner app, ADHD planner lifetime
**Job:** conversion + comparison shoppers.

---

## What was fixed technically

1. **Canonical mismatch.** The old site canonicalised to `www.duneseven.com.au` while serving from `duneseven.com.au`. Authority was split across two hostnames. Now standardised on non-www, with a 301 in `_redirects` enforcing it.
2. **Single-page architecture.** One page can rank for one cluster. Six pages, internally cross-linked, target six.
3. **Structured data.** Organization, MobileApplication with all four offers, FAQPage on every page, BreadcrumbList on subpages. FAQ schema is what wins the expanded result in Google.
4. **hreflang en-AU + x-default** on every page.
5. **Core Web Vitals:** font preconnect, non-blocking font load on home, `loading="lazy"` on below-fold images, explicit width/height to stop layout shift, immutable cache headers on static assets.
6. **Accessibility floor:** skip link, visible focus rings, `prefers-reduced-motion` respected, single H1 per page, semantic landmarks.

## Deploy

1. Drop these files at the repo root, preserving folder structure.
2. Keep your existing `og-image.jpg`, `app-icon-64.png`, `angela-chloe-1024.jpg` and `privacy-policy` in place — the pages reference them.
3. Re-add your GTM snippet (`GTM-WHG8SCQM`) to `<head>` on all six pages before pushing. I left it out rather than risk a malformed container tag.
4. Commit, push, Netlify builds.
5. In Search Console: submit `https://duneseven.com.au/sitemap.xml`, then request indexing on each of the four pillar URLs individually. Don't wait for the crawl.

## Still to build (parked, not forgotten)

- `/support` page — App Store review requires a reachable support URL
- Blog cluster feeding each pillar (3 posts per pillar is the target)
- Terms of Service page, now that there are paid tiers
