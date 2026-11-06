# miz-site-assets

Static code for the MIZ Experts Webflow site, served through jsDelivr.

| File | Used by | Load URL |
| --- | --- | --- |
| `miz-home.min.js` | new-home page (staging) | `https://cdn.jsdelivr.net/gh/fagirym-sketch/miz-site-assets@v3/miz-home.min.js` |
| `miz-hub.min.js` | division hubs and service pages (Regulatory first) | `https://cdn.jsdelivr.net/gh/fagirym-sketch/miz-site-assets@v10/miz-hub.min.js` |
| `miz-hub.css`, `miz-hub-loader.min.js` | About, Work and Insights pages and their templates (from v8) | `https://cdn.jsdelivr.net/gh/fagirym-sketch/miz-site-assets@v10/miz-hub.css`, `.../miz-hub-loader.min.js` |

## Rules

- Webflow always loads a **version tag** (`@v1`, `@v2`, …), never `@main` or `@latest`.
- Every change ships as a **new tag**. Never move or reuse an existing tag: jsDelivr caches a tag for good.
- The Webflow loader also checks each file's SHA-384 hash (`integrity`), so a file that changes
  without a matching update in Webflow is blocked rather than run. The page then shows its content
  without motion, instead of running unreviewed code.
- Files here are build output. The readable sources live in the project's `webflow/new-home/`
  folder (`new-home/hero.js`, `new-home/sections.js`, `hub/hub.js`); edit those, rebuild, and tag a new version.

## Versions

| Tag | Change |
| --- | --- |
| v1 | Hero, logo strip, services marquee, Three chapters, Why MIZ, round-3 motion |
| v2 | Leadership cards: line icon draws in, name rises, desktop hover; insights reveal only |
| v3 | Key figures: calm count-up from 0 (1.2 s, ease-out) with label fade, plays once; replaces the scramble |
| v4 | Adds `miz-hub.min.js`: Regulatory hub and service pages (header states, pathway motif, pathway timeline, 300+ count-up, reveals, CTA lines). `miz-home.min.js` unchanged from v3 |
| v5 | `miz-hub.min.js`: adds the Division Chapters section (the other two divisions with the home chapters' 3D line forms, text reveal, service hover; stills under reduced motion). `miz-home.min.js` unchanged from v3 |
| v6 | `miz-hub.min.js`: adds the Technology & Intelligence hub (network motif, kicker scramble, reactive dot grid, service anchors with a sticky navigator and scroll-spy, per-service reveals). The loader also loads ScrambleTextPlugin. Regulatory pages stay on v5 until moved on purpose. `miz-home.min.js` unchanged from v3 |
| v7 | `miz-hub.min.js`: adds the Marketing & Creative hub (waves-and-planes hero with a kinetic headline, client logo loop, pinned work showcase with swipe on touch, service image mask reveals, process line, magnetic buttons). Used on /marketing only; /tech stays on v6 and the Regulatory pages on v5. `miz-home.min.js` unchanged from v3 |
| v8 | `miz-hub.min.js`: adds the About, Work and Insights pages (converging-lines hero, key figures count-up, Leadership cards, division filter for case study and article lists, cover mask reveals). New files `miz-hub.css` (page CSS) and `miz-hub-loader.min.js` (page loader), so these pages hold only a few lines of custom code. /marketing stays on v7, /tech on v6, the Regulatory pages on v5. `miz-home.min.js` unchanged from v3 |
| v9 | `miz-hub.min.js`, `miz-hub.css`, `miz-hub-loader.min.js`: add the Contact page (honeypot, dropdown safeguard, focus on the form result, map loads on scroll, form and map styles). Used on the new Contact page only; About, Work and Insights stay on v8, /marketing on v7, /tech on v6, Regulatory on v5. `miz-home.min.js` unchanged from v3 |
| v10 | Contact page: the dropdown safeguard reads its options from the field wrapper, because Webflow does not keep custom attributes on a select. Used on the new Contact page only; v9 was not used by any published page |
