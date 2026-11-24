# StyleKit — Dress Well, Decide Fast

Your wardrobe, planned before the mirror. StyleKit turns the clothes you
already own into outfits in seconds — then tracks wears, laundry and
cost-per-wear, so nothing sits unworn.

**Live:** https://abhiramunni.github.io/stylekit/

## What it does

- **Outfit builder** — pick one piece from each rail (top, bottom, shoes),
  filtered by occasion (Everyday, Interview, Date, Turf, Temple, Travel,
  College) and weather (Hot, Pleasant, Cool, Rain). “Surprise me” shuffles a
  fitting outfit when you cannot decide.
- **Today’s outfit** — a date-based pick from your saved outfits, shown on
  the hero card every morning, with one-tap “I wore this today”.
- **Saved outfits** — name and save any combination; wearing one bumps every
  piece’s wear count and sends the pieces to the laundry basket.
- **Laundry basket** — worn pieces land here; mark them washed (one by one or
  all at once) and they come straight back to the rails. A “wash first” flag
  marks stained pieces.
- **Wardrobe** — all 19 seeded pieces with price, wears and honest
  cost-per-wear (price ÷ wears). Filter by type, ready, in laundry or
  wash-first. Add your own pieces with price and colour.
- **This week** — assign a saved outfit to each of the next 7 days, so
  mornings stop being a decision.
- **Your numbers** — pieces owned, ready now, average cost-per-wear,
  most-worn and least-worn pieces, laundry count, total wears logged.
- **6 style guides** — capsule building, colour matching, interview dressing,
  monsoon shoe care, making clothes last, laundry symbols — plain language,
  no jargon, no shopping links.

## Seeded wardrobe

The starter wardrobe mirrors a real closet: white linen shirt, brown shirt,
Demon Slayer tee, Nike “JUST DO IT.” sweatshirt, Rare Rabbit brown hoodie,
light-blue tee (flagged wash-first — it has a stain), grey jeans, grey check
trousers, black tribal joggers, brown Woodlands, Woodland hiking shoes, Shaq
black shoes, Nike Air Monarch and Vans Old Skool, among others. Three saved
outfits ship with it: The Classic, Brown on Brown and Turf Ready. Use
“Remove samples” in the footer to clear them and start from your own clothes.

## Design

Warm editorial palette (ivory paper, espresso ink, bronze/amber/gold),
Fraunces + Inter, full-screen cinematic intro with tap-to-skip (quick on
return visits), slow Ken Burns drift on the two AI-generated wardrobe photos,
snap-scroll outfit rails, and a 3-step onboarding coach.

## Tech

Single self-contained `index.html` — no backend, no signup, no tracking.
All state lives in `localStorage` under the key `stylekit_v1`. Works offline
after the first load (Google Fonts need a connection on first visit).

## QA

74/74 headless jsdom assertions pass (`node qa-test.js`), `node --check`
clean, zero uncaught JS errors, no pictographic emoji. Hand-verified seed
numbers: 19 items, ₹35,081 total value, 157 total wears, average
cost-per-wear ₹223, most-worn Brown Woodlands (15), least-worn Vans Old
Skool (3), white linen shirt ₹125/wear, The Classic ₹397/wear.

## License

MIT — see `LICENSE`.
