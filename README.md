# inspiro-website-code

Source code for the redesigned inspiro-club.com (English and Romanian), hosted on HighLevel (SalesProcess).

## How it is deployed

HighLevel has no API for page content, so the site uses a hybrid setup:

- **Shared CSS, JavaScript and icons** live in this repository and are served from the jsDelivr CDN
  (`https://cdn.jsdelivr.net/gh/inspiroclub/inspiro-website-code@<tag>/...`). They are referenced once
  in the website's head tracking code. A new tag plus a one-line version change publishes a design update.
- **Header and footer** are pasted once into a HighLevel global section (Custom Code element).
- **Page bodies** are pasted into a Custom Code element on each page, so search engines and link
  previews see the real content.

## Planned layout

```
assets/      shared CSS, JS, icons, fonts
partials/    header and footer HTML, per language
pages/en/    page bodies, English
pages/ro/    page bodies, Romanian
docs/        audit, research notes, deployment guide
```

## Status

- 2026-11-25: repository created; audit and outreach research done (see the Claude doc
  "inspiro-club.com audit and outreach research"). Design proposals next.
