# Ninefold â€” Vedic Numerology

A static single-file numerology site: a free Life Path number widget on the landing page plus a
per-number profile page for each of the nine core Life Path numbers, leading visitors toward a
paid Vedic reading.

## What's here

- `index.html` â€” the landing page with the free "Life Path Finder" widget, the
  tiered reading offers, and a booking/briefing form.
- `number-1.html` â€¦ `number-9.html` â€” one profile page per Life Path number. Each is
  data-driven: all number-specific copy lives in a single `PAGE` object near the top of the file,
  so content is easy to edit per number without touching the layout.

The widget on the landing page reduces a birth date to its Life Path number and links out to the
matching `number-N.html` profile.

## Tech

- Plain HTML + CSS + vanilla JS, no build step, no backend.
- Dark, gold-and-ink aesthetic (Fraunces / Inter / IBM Plex Mono).
- Designed to be served from any static host (GitHub Pages, Vercel, Netlify).

## Status

Early-stage prototype. Brand finalised as **Ninefold**. Payment links, the live
booking form endpoint (Formspree), and real testimonials are placeholders to be filled in.

> Readings are for entertainment and personal reflection purposes only.
