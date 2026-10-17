# miz-site-assets

Static code for the MIZ Experts Webflow site, served through jsDelivr.

| File | Used by | Load URL |
| --- | --- | --- |
| `miz-home.min.js` | new-home page (staging) | `https://cdn.jsdelivr.net/gh/fagirym-sketch/miz-site-assets@v1/miz-home.min.js` |

## Rules

- Webflow always loads a **version tag** (`@v1`, `@v2`, …), never `@main` or `@latest`.
- Every change ships as a **new tag**. Never move or reuse an existing tag: jsDelivr caches a tag for good.
- The Webflow loader also checks each file's SHA-384 hash (`integrity`), so a file that changes
  without a matching update in Webflow is blocked rather than run. The page then shows its content
  without motion, instead of running unreviewed code.
- Files here are build output. The readable sources live in the project's `webflow/new-home/`
  folder (`hero.js`, `sections.js`); edit those, rebuild, and tag a new version.
