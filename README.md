# Party Services & Rentals — Advertising & More

Single-file landing page for the party services & rentals offering, built to belong
100% to the `advertisingandmore.com` brand language (same section grammar, eyebrows,
sentence-case headlines with a gold tail, and the agency's own CTA wording).

Everything — styles, scripts, photographs, icons — is inlined in `index.html`, so the
page runs with **no build step, no dependencies and no network calls**.

---

## Publish on GitHub Pages

1. Create a new repository and upload `index.html` (+ this README).
2. **Settings → Pages → Source: Deploy from a branch → `main` / `root`**.
3. The page is served at `https://<user>.github.io/<repo>/`.

`index.html` is the entry point, so no extra configuration is needed.

## Run locally

Open `index.html` in any modern browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

## Page structure

| # | Section | Eyebrow | Headline |
|---|---------|---------|----------|
| 1 | Hero | Games, performers & foyer attractions | Party Services & Rentals |
| 2 | Trusted brands | Trusted by these brands, & more… | — (flat brand-blue band, two-row logo slider) |
| 3 | Featured Experiences | Featured Experiences | The moments everyone remembers. |
| 4 | Why Choose Us | Why choose us | More than just rentals. |
| 5 | Our 15 Favourites | Our 15 favourites | Start with the crowd pleasers |
| 6 | Full inventory | What we do — the full inventory | 100 ways to make your event unforgettable. |
| 7 | Party recipes | Not sure where to start? | Start with a party recipe. |
| 8 | Drinks / meeting | The drinks are on us | Book a happy meeting. |
| 9 | FAQ | Questions & answers | Everything you might be wondering. |
| 10 | Testimonials | Kind words | Booked by the brands you already know. |
| 11 | How we work | How we work | From Idea to Incredible, Together. |
| 12 | Enquiry | Start your enquiry | Let's plan your event over coffee. |
| 13 | Closing band | Our work | The Ultimate Party Playground. |
| 14 | Footer | — | — |

## Interactive features

- **100-item catalogue** with 10 category filter tabs + "See more" pagination.
- **Wishlist** — the round `+` buttons on the Top 15 cards, the catalogue cards and
  the party recipes. State lives in `localStorage` under
  `am-party-wishlist-preview-v1` and is mirrored into the floating tray, the drawer
  and the enquiry form's service list.
- **Brand strip** — one flat brand-blue band (#0049A8) with two logo rows gliding in
  opposite directions. The track re-duplicates its logo sets on every resize so the
  loop is seamless at any width (it used to be narrower than the screen).
- **Party recipes** — one click adds five matching catalogue items to the wishlist.
- **Top 15 cards** — round `+` adds to the wishlist (gold check → pink heart), plus a
  "Quick Specs" accordion. Each card carries a brand-gold AI-generated category icon.
- **FAQ accordion** — single-open, `aria-expanded` wired, animated height.
- **Section decks** — most descriptions fold inside their headline; click to reveal,
  it collapses on scroll or after 5 seconds. Featured Experiences is the exception:
  its description sits permanently under the title.
- **Enquiry form** — 165 fields incl. country picker, services multiselect and
  investment tiers.

## Technical notes

- One file, ~12 MB, because every image is a base64 data URI (portable and offline-safe).
- The hero uses the client-supplied 3:1 artwork: above 1280 px the hero takes the
  photograph's own proportion so its cream copy panel lines up with the copy column;
  below that the scene fills the band and the readable veil keeps the light copy crisp.
- No external fonts, CDNs or tracking scripts.
- Verified on Chromium at 1440 / 1180 / 1024 / 768 / 390 / 360 / 320 px with zero
  horizontal overflow and zero console errors.

## Credits

Design and copy aligned to [advertisingandmore.com](https://advertisingandmore.com/).
The hero artwork was supplied by the client.
Imagery for the Featured Experiences mosaic, the Top 15 category icons, the Why
Choose Us icons and the closing playground band was purpose-generated for this page.
