# Cruz Auto Service

Marketing website for Cruz Auto Service, an auto repair shop in Shakopee, MN.

## Contents

- `index.html` — the complete site. A single self-contained page: all CSS, JavaScript,
  SVG icons, and photos (inline base64 JPEGs) live in this one file, so there are no
  build steps and no external assets to host.

The only external requests the page makes are to Google Fonts (Oswald and Work Sans).

## Sections

| Anchor | Content |
| --- | --- |
| `#services` | Services offered — diagnostics, brakes, electrical, suspension, engine and transmission work |
| `#why` | Why customers choose the shop |
| `#reviews` | Customer reviews |
| `#about` | About the shop |
| `#faq` | Frequently asked questions |
| `#contact` | Location, hours, phone, and the request-service form |

## Running it locally

Open the file directly:

```
open index.html
```

Or serve it over HTTP, which more closely matches production:

```
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying

The site is static, so any static host works. For GitHub Pages, enable Pages for this
repository and point it at the branch root — `index.html` is served as-is.

## Known limitation: the contact form

The request-service form at `#contact` validates input and shows a confirmation message
in the browser, but it does **not** send anything anywhere. Submissions are currently
lost. To actually receive requests, point the form at an email service (Formspree,
Netlify Forms, or similar) or at a backend endpoint — see the note in the `<script>`
block at the bottom of `index.html`.

## SEO

The page includes `AutomotiveBusiness` and `FAQPage` JSON-LD structured data, Open Graph
tags, a meta description, and a canonical URL pointing at `https://www.cruzautoservice.com/`.
Update the canonical URL if the site is deployed elsewhere.
