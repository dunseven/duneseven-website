# Dune Seven 1.3.0 drop — 9 changed files

Drag the CONTENTS of this folder (not the folder itself) into GitHub:
repo → Add file → Upload files → drop everything → commit to main.
GitHub replaces the existing files at the same paths. Netlify redeploys automatically.

Changed:
- index.html — hero + meta now include shift-work rosters; routines card is roster-first; "Five ways in" with the new Shift work card; nav + footer links
- adhd-planner, mental-load, burnout-recovery, postpartum-planner — nav + footer links, Shift work added to "Also read"
- you-know-your-energy — nav link (this page has no Built-for footer, nothing else touched)
- pricing — Pro card and FAQ now read "repeating routines (My roster + weekdays)"; prices untouched, $69.99 confirmed
- shift-worker-planner/index.html — REBUILT on the shared styles.css template (replaces the standalone-styled version); GTM included, FAQ structured data included
- sitemap.xml — new page added at 0.9; you-know-your-energy added (it was missing entirely)

After deploy: check duneseven.com.au on your phone — Shift work should appear in the nav on every page — then request indexing for /shift-worker-planner/ in Search Console.

Housekeeping (separate, whenever): the repo contains "index (1).html" through "index (6).html", "files (3).zip", preview-home-v10.html, story-section.html and a duplicate terms.html. These all deploy to the public site. Worth deleting from GitHub when you have a minute.
