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
i18n.js      — translation tables + language switcher + form handling
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

## Notes

- The enquiry form opens the visitor's email client with a pre-filled message
  (subject + every field, labelled in the visitor's language) addressed to
  `CONTACT_EMAIL` in `i18n.js`, then shows the on-page "thank you". No backend is
  needed. Change the recipient by editing `CONTACT_EMAIL`. (If you'd prefer a
  hosted form that emails silently without opening a mail app, swap in a service
  like Formspree.)
- Contact details (`+34 600 000 000`, `hola@chefpajti.es`) are placeholders —
  the email address is used both in the header link and as the form recipient.

## Deployment

Published from the `main` branch (root) via GitHub Pages. Push to `main` and the
site updates within a minute or two.
