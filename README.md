[README.md](https://github.com/user-attachments/files/31882829/README.md)
# Ki Communities

A private surf-real-estate community website for the Mentawai Islands, Indonesia — eight beachfront lots directly in front of the "Suicides" break.

Static site, no build step. Plain HTML/CSS/vanilla JS.

## Pages

Each nav item is its own real page (not a single-page app with hash routing):

| File               | Section        |
|---------------------|----------------|
| `index.html`        | Home           |
| `community.html`    | The Community  |
| `surf.html`          | Surf           |
| `rejuvenate.html`    | Rejuvenate     |
| `ownership.html`     | Ownership      |
| `mentawai.html`      | The Mentawais  |
| `enquire.html`       | Enquire        |

All pages share the same header, footer, and color-palette switcher. The current page's nav link is marked with `class="on"`.

## Running locally

No build step — just serve the folder:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/index.html`.

## Notes

- The animated wave-pattern graphics on some pages are drawn on `<canvas>` at load time (`paintPlates()` in the inline script) — no external image assets for those.
- The enquiry form on `enquire.html` opens the visitor's email client with a pre-filled message; there's no backend.
- Deploys as a static site (e.g. Vercel) — no framework, no dependencies, no `package.json`.
