# Rafi A Pets — website

A fast, single-page website for **Rafi A Pets**, a 24-hour pet store on Kagmari Road, Tangail.
Built as a free demo for the shop — plain HTML, CSS and a little JavaScript, no build step, no framework.

**Live preview (this repo):** `https://sikdershakib.github.io/uddogpoint/rafi-a-pets/`

---

## What's inside

```
rafi-a-pets/
├── index.html          ← the whole site (styles + scripts inline)
├── assets/
│   ├── favicon.svg
│   ├── hero-shop.jpg   ← hero image
│   ├── cockatiel.jpg   ← featured pet / gallery
│   ├── budgies.jpg
│   ├── lovebirds.jpg
│   ├── aquarium.jpg
│   ├── supplies.jpg
│   ├── cages.jpg
│   └── dog-cat.jpg
└── README.md
```

Sections: hero → ways to shop → shop categories → featured birds/fish → about →
gallery (with lightbox) → reviews → FAQ → visit/contact (map + WhatsApp form) → footer.

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
| Opening display | In-store shopping / pick-up / delivery |

These appear in the page copy, the "Visit" section, the WhatsApp links (`wa.me/8801709518395`),
the Google Maps embed and the `PetStore` structured data at the bottom of `index.html`.

## Before it goes live — checklist

1. **Replace the sample reviews.** The three review cards in the Reviews section are
   placeholders (they are flagged with an HTML comment). Keep the real 5.0 / 2-review
   summary, and paste in the customer's actual words once they send them — or delete
   the cards and keep only the rating card.
2. **Swap the photos for the shop's own.** All images are AI-generated stand-ins so the
   demo looks finished. Real photos of the shop front, the birds, the shelves and the
   owner will convert far better. Keep the same filenames in `assets/` and nothing
   else needs to change (hero works best around 5:4, gallery images at least 1200px wide).
   Optimise them to under ~300 KB each.
3. **Confirm WhatsApp.** The "Send on WhatsApp" form and floating button assume the
   phone number is on WhatsApp. If not, change the links to `tel:` or a Messenger/IMO link.
4. **Confirm product claims.** Copy mentions cockatiels, budgerigars, lovebirds,
   freshwater fish, dog/cat food, cages and toys — trim anything the shop doesn't stock.
5. **Delivery wording.** Currently "local delivery around Tangail, confirm cost and area
   by phone" — keep it vague until the owner sets a radius and charge.
6. **Map pin.** The embed searches "Rafi A Pets, Kagmari Rd, Tangail 1900". Once the shop
   claims its Google Business Profile, replace the embed with the exact place link.
7. **Update the canonical / `og:url`** if the site moves to its own domain.

## Editing quickly

- **Phone number:** search for `01709-518395` and `8801709518395` (replace all).
- **Address / hours:** search for `Kagmari Rd` and `Open 24 hours`.
- **Colours:** the design tokens at the top of the `<style>` block —
  `--forest: #0E3B2B`, `--amber: #E7A03C`, `--cream: #FBF6ED`.
- **Fonts:** Fraunces (headings) + Manrope (body), loaded from Google Fonts.
- **Icons:** Font Awesome 6 via cdnjs.

## Deploying

Because this repo already deploys to GitHub Pages on every push to `main`, this page is
already online under `/rafi-a-pets/`. For the client's own address, pick one:

- **Own repo + GitHub Pages** (free): push this folder to `rafi-a-pets/rafi-a-pets` and enable Pages.
- **Netlify / Cloudflare Pages** (free, custom domain): drag-and-drop the folder, no build command.
- **Custom domain** e.g. `rafiapets.com` — point it at the host and update the canonical URL.

## Notes

- No cookies, no analytics, no tracking scripts, nothing stored — the form simply opens WhatsApp.
- Accessible touches: skip-free semantic headings, focus rings, `aria` labels, `prefers-reduced-motion` support.
- SEO: descriptive title/meta, Open Graph tags, `PetStore` JSON-LD with address, hours and rating,
  semantic sections and alt text on every image.
