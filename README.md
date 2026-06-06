# Coyote Gold — pitch site

Password-gated single-page pitch site. Password: `coyotes`
(change it via the `SITE_PASSWORD` constant in the `<script>` block of index.html)

## Files
- `index.html` — the whole site (HTML/CSS/JS in one file)
- `art/` — all imagery, organized by type:
  - `art/coyote-gold-hero.png` — hero key art
  - `art/logo-coyote-gold.png` — logo (gate + footer)
  - `art/icons/` — 11 inline header icons
  - `art/cards/` — character baseball cards
  - `art/locations/` — establishing location art
  - `art/objects/` — props (medallion, map, mitt)
  - `art/lore/` — real-LA-history clippings
  - `art/hero/` — pennant, gold coins, LA Times clipping

## Deploying (Cloudflare Pages)
1. Push this repo to GitHub.
2. Cloudflare dashboard -> Workers & Pages -> Create -> Pages -> Connect to Git -> pick this repo.
3. Build settings: Framework preset = None, Build command = (blank), Output directory = `/`.
4. Save & Deploy. Confirm it loads at the *.pages.dev URL.
5. Pages project -> Custom domains -> add `coyotes.thecampbrand.com` (Cloudflare auto-creates the DNS record since the domain is in your account).

## ICONS — instruction for Claude Code
I've uploaded a zip of 11 icon files into the repo. Please:
1. Unzip them into `art/icons/`, overwriting the existing placeholder files there.
2. The 11 icons should be named: icon-first-pitch, icon-reading-signs, icon-deep-in-count,
   icon-lucky-charm, icon-hot-streak, icon-corked-bat, icon-stealing-signs,
   icon-seventh-stretch, icon-last-strike, icon-extra-innings, icon-bottom-ninth.
3. If the files are .png (not .svg), update index.html so every `<img class="hicon" ...>`
   reference points to the .png version instead of .svg. If they're already .svg with those
   exact names, no HTML change is needed.
4. If any unzipped filenames differ from the list above (number prefixes, different words),
   rename them to match the exact names so the wiring picks them up.
5. Commit and push.
