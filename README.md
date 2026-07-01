# ChefAtHome — Pajti Imre, Private Chef 🍽️

Marketing site for **Pajti Imre**, a private chef serving villas across
**Murcia, the Costa Cálida & Costa Blanca** in Spain. Framework-free static
site, served with GitHub Pages.

**Live site:** https://ronyoka.github.io/ChefAtHome/

## Languages

The site ships in **8 languages**, chosen for the region's international clientele.
On first visit the language is picked from the browser, then remembered in
`localStorage`; visitors can switch any time from the selector in the header.

| Code | Language | | Code | Language |
|------|----------|---|------|----------|
| `en` | English (default) | | `fr` | Français (Belgium) |
| `es` | Español | | `da` | Dansk (Denmark) |
| `de` | Deutsch | | `no` | Norsk (Norway) |
| `nl` | Nederlands (Holland) | | `hu` | Magyar |

## Structure

```
index.html   — the page (inline styles, semantic sections, data-i18n hooks)
i18n.js      — translation tables + language switcher
images/      — 17 photos (extracted from the original design bundle)
```

Hungarian is the copy baked directly into `index.html`; every other language is
swapped in from the `I18N` table in `i18n.js`. To add a language, add one entry
to that table and one `<option>` to the `#langSelect` dropdown.

## Local preview

```bash
python -m http.server 8000
# then open http://localhost:8000
```

## Contact

There is no contact form — visitors reach the chef directly from the contact
section and the hero:

- **WhatsApp** — `https://wa.me/34605342806`
- **Phone** — `tel:+34605342806` (+34 605 34 28 06)
- **Email** — `mailto:hola@chefpajti.es` (placeholder address — replace with the real one)

The right-hand side of the contact section is a decorative inline SVG (a covered
dish with a place setting). To change the number, update the `wa.me` / `tel:`
links in `index.html`; to change the email, update the `mailto:` links.

## Deployment

Published from the `main` branch (root) via GitHub Pages. Push to `main` and the
site updates within a minute or two.
