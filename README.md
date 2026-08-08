# Ninefold — Vedic Numerology

A static single-file numerology site: a free Life Path number widget on the landing page plus a
per-number profile page for each of the nine core Life Path numbers, leading visitors toward a
paid Vedic reading.

## What's here

- `index.html` — the landing page with the free "Life Path Finder" widget, the
  tiered reading offers, and a booking/briefing form.
- `number-1.html` … `number-9.html` — one profile page per Life Path number. Each is
  data-driven: all number-specific copy lives in a single `PAGE` object near the top of the file,
  so content is easy to edit per number without touching the layout.
- `privacy-policy.html`, `terms.html`, `cookie-policy.html` — the legal pages (Privacy, Terms &
  Conditions, and Cookie Policy covering the GA4 + Microsoft Clarity trackers).
- `blog.html` — the Journal index. Data-driven from the `POSTS` array near the top; the newest
  post is promoted automatically to the featured card.
- `blog/_post-template.html` — the template to copy for each new blog post (see below).
- `blog/*.html` — individual blog posts, one self-contained file each.

The widget on the landing page reduces a birth date to its Life Path number and links out to the
matching `number-N.html` profile.

## Publishing a blog post (daily posts, ~a minute each)

Each post is a single HTML file in `blog/` (no build step, nothing to install). To publish:

1. **Copy the template:** `blog/_post-template.html` → `blog/<your-slug>.html`.
2. **Fill in the meta** at the top of `<head>` (title, description, canonical URL, and the
   JSON-LD structured-data block) and **write the article body** between the
   `START` / `END` comments. Reuse the styled helpers (callouts, tables, pull-quotes) and drop the
   `read-box` CTA in once or twice so readers can book.
3. **Register it on the index:** in `blog.html`, add one line to the `POSTS` array
   (newest line on top). The index sorts and features it automatically.
4. **Add the URL to `sitemap.xml`.**

Because the site is static, once the file lands on the host it's live immediately — no deploy step
beyond pushing the git commit.

## Tech

- Plain HTML + CSS + vanilla JS, no build step, no backend.
- Dark, gold-and-ink aesthetic (Fraunces / Inter / IBM Plex Mono).
- Designed to be served from any static host (GitHub Pages, Vercel, Netlify).

## Status

Early-stage prototype. Brand finalised as **Ninefold**. Payment links, the live
booking form endpoint (Formspree), and real testimonials are placeholders to be filled in.

> Readings are for entertainment and personal reflection purposes only.
