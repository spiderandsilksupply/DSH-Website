# Dubai Silk Holdings — Website

A multi-page marketing site for Dubai Silk Holdings (DSH), a joint venture developing
natural spider silk for regenerative medicine and luxury fashion.

## Pages

| Page | File |
|------|------|
| Home | `home.dc.html` |
| About | `about.dc.html` |
| Projects | `projects.dc.html` |
| Technology | `technology.dc.html` |
| Investors | `investors.dc.html` |
| Medical | `medical.dc.html` |
| Fashion & Luxury | `fashion.dc.html` |
| Silk Supply | `silk-supply.dc.html` |
| Contact | `contact.dc.html` |

Shared components imported by every page:

- `Header.dc.html` — fixed nav with scroll-aware background
- `Footer.dc.html` — site footer

## Tech

The pages use a small client-side "DC" runtime (`support.js`) that renders the
`<x-dc>` template against React (loaded from CDN at runtime) and resolves
`<dc-import>` component references by fetching the sibling `.dc.html` files.
`image-slot.js` provides the fillable image placeholders on the About page.

## Running locally

The runtime resolves components with `fetch()`, so the site must be served over
HTTP (not opened as `file://`):

```bash
python3 -m http.server 8300
```

Then open http://localhost:8300/home.dc.html
