# Rafi A Pets — website

A fast, single-page website for **Rafi A Pets**, a 24-hour pet store on Kagmari Road, Tangail.
Plain HTML, CSS and a little JavaScript — no build step, no framework.

**Live preview (this repo):** `https://sikdershakib.github.io/uddogpoint/rafi-a-pets/`

---

## What's inside

```
rafi-a-pets/
├── index.html          ← the whole site (styles + scripts inline)
├── assets/
│   ├── favicon.svg
│   ├── cockatiel.jpg       ← hero + featured card (from the shop's own photo)
│   ├── budgies.jpg         ← featured card
│   ├── lovebirds.jpg       ← featured card
│   └── shop-listing.jpg    ← the shop's Google-listing photo collage (About section)
└── README.md
```

Sections: hero → ways to shop → shop categories → the birds → about →
how ordering works → reviews → FAQ → visit/contact (map + WhatsApp form) → footer.

## Business details used (from the Google listing)

| Field | Value |
|---|---|
| Name | Rafi A Pets |
| Category | Pet store |
| Address | Kagmari Rd, Tangail 1900, Bangladesh |
| Plus code | 6WQ3+MF Tangail |
| Phone | 01709-518395 (`+8801709518395`) |
| Hours | Open 24 hours, every day |
| Rating | 5.0 from 2 Google reviews |
| Ways to shop | In-store shopping · In-store pick-up · Delivery |

These appear in the page copy, the "Visit" section, the WhatsApp links (`wa.me/8801709518395`),
the Google Maps embed and the `PetStore` structured data at the bottom of `index.html`.

## Photos

The images are **the shop's own** — cropped out of the photo collage on its Google listing
(cockatiel, budgerigars, lovebirds). No stock photography and no AI-generated animals.

⚠️ **Resolution is low.** The original upload was only 408 × 408 px, so each bird panel is
about 200 px wide. They have been upscaled and sharpened for the web, and the layout keeps
them at sizes where they still look clean — but they will never be crisp on a large screen.
**Ask the owner for the original camera photos** (ideally 1200–2000 px wide). Drop them in
with the same filenames and the whole site sharpens up with no code changes.

Best crops for each slot:

| File | Use | Ideal source |
|---|---|---|
| `cockatiel.jpg` | Hero + featured card | portrait, whole bird or head-and-body |
| `budgies.jpg` | Featured card | square or landscape |
| `lovebirds.jpg` | Featured card | square or landscape |
| `shop-listing.jpg` | About section | square, any shop/bird photo |

## Before it goes live — checklist

1. **Replace the sample reviews.** The three review cards in the Reviews section are
   placeholders (flagged with an HTML comment). Keep the real 5.0 / 2-review summary and
   paste in the customer's actual words — or delete the cards and keep the rating card.
2. **Get the original photos** from the owner (see above).
3. **Confirm WhatsApp.** The enquiry form and floating button assume the phone number is
   on WhatsApp. If not, switch the links to `tel:` or Messenger/IMO.
4. **Confirm product claims.** Copy mentions cockatiels, budgerigars, lovebirds, bird seed,
   dog/cat food, cages and aquarium supplies — trim anything the shop doesn't stock.
5. **Delivery wording.** Currently "local delivery around Tangail, confirm by phone" — keep
   it open until the owner sets a radius and charge.
6. **Map pin.** The embed searches "Rafi A Pets, Kagmari Rd, Tangail 1900". Once the shop
   claims its Google Business Profile, swap in the exact place link.
7. **Update the canonical / `og:url`** if the site moves to its own domain.

## Editing quickly

- **Phone number:** search for `01709-518395` and `8801709518395` (replace all).
- **Address / hours:** search for `Kagmari Rd` and `Open 24 hours`.
- **Colours:** design tokens at the top of the `<style>` block —
  `--forest: #0E3B2B`, `--amber: #E7A03C`, `--cream: #FBF6ED`.
- **Fonts:** Fraunces (headings) + Manrope (body), Google Fonts.
- **Icons:** Font Awesome 6 via cdnjs.

## Deploying

This repo already deploys to GitHub Pages on every push to `main`, so this page goes live
at `/rafi-a-pets/` once merged. For the client's own address, pick one:

- **Own repo + GitHub Pages** (free): push this folder to a dedicated repo, enable Pages.
- **Netlify / Cloudflare Pages** (free, custom domain): drag-and-drop the folder, no build command.
- **Custom domain** e.g. `rafiapets.com` — point it at the host and update the canonical URL.

## Notes

- No cookies, no analytics, no tracking scripts, nothing stored — the form simply opens WhatsApp.
- Accessible touches: semantic headings, focus rings, `aria` labels, `prefers-reduced-motion`.
- SEO: descriptive title/meta, Open Graph tags, `PetStore` JSON-LD with address, hours and rating,
  alt text on every image.
