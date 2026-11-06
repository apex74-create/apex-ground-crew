# LIBRARY ADMISSION LOG — JOB AGC-FRONT-END

Opened at build time, per the Design Desk determination (companion requirement).
Build date: Nov 6, 2026 (night job). Page: Apex Ground Crew front end (index.html).

## Inbound admissions

| Item | Detail |
|---|---|
| Font family | Public Sans (Google Fonts) — humanist sans, current set at build time |
| Form admitted | Variable font, latin subset, WOFF2, self-hosted in this repo at `fonts/public-sans-latin.woff2` |
| Weights used | 400 (text) and 700 (display/labels/button) — two weights, from the one variable file |
| Source | https://fonts.gstatic.com/s/publicsans/v21/ijwRs572Xtc6ZYQws9YVwnNGfJ4.woff2 (latin block of the css2 response for Public Sans wght 400;700) |
| Size | 26,832 bytes |
| SHA-256 | 5ed4d31c988e73b258894244f209069ebe77dc7e564861954b21198b6de90d68 |
| Runtime calls | Zero — the file is served from this repo with the page; no font fetch to Google or any CDN per visitor |

## Internal (no admission — written in-house, page-inline)

- CSS: hand-written, inline in index.html (custom properties, backdrop-filter with flat opaque fallback). No external stylesheet, no framework.
- JavaScript: the page's pre-existing inline script, unchanged byte-for-byte (FormSubmit AJAX + mailto fallback). No new script admitted; no third-party JS.

## Outbound inventory (finished page, per visitor)

- The form's own submission to FormSubmit (AJAX POST), and the visitor-initiated mailto fallback if that fetch fails. That is the page's function, unchanged from the pre-Glass House page.
- Everything else: zero calls out. No analytics, no CDN, no external images.

**Security Detail posture:** one named inbound admission (above), pinned by hash; self-host preference met in full.
