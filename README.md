# Mettle — landing page

**Files:** `Mettle Landing.dc.html` · `assets/` (mark, og-card, kashish, sudhanshu, khwahish) · `image-slot.js`

## Before it goes live — 5 blockers

1. **Domain.** `REPLACE-WITH-DOMAIN` appears in the canonical link, all og/twitter tags and the JSON-LD (`@id`, `url`, `logo`, `og:image`). Find and replace.
2. **Form endpoint.** Both forms (the modal and the inline panel in *start your journey now*) hold answers in memory and send nothing. Wire `send()` in the logic class to your endpoint.
3. **Calendly length.** The embed points at `/30min` but every mention on the page says **15 minutes**. Change the Calendly event or change the copy — right now they disagree.
4. **Currency.** Prices publish as **AUD, GST-inclusive where applicable**. You never confirmed AUD. If the tiers are INR this is the most damaging error on the page.
5. **Legal.** No privacy, terms or refund pages exist, and the footer no longer links to any. You cannot take card payments without them. Registered entity name, ABN/ACN and address are still `[NEEDS REAL DATA]` in the bottom strip.

## Remaining `[NEEDS REAL DATA]` markers

- Sidhant's LinkedIn link (Kashish's is live). His photo is a drag-and-drop slot — drop a file on it and it persists.
- Job title, employer and a verification link for Khwahish and Sudhanshu. Their quotes are currently unverifiable by a reader.
- Form endpoint note inside both form panels.
- Footer entity details.

## Claims you must be able to substantiate

Under Australian Consumer Law s18 every figure below is a representation you may be asked to prove. Keep the underlying records.

- **500+** students coached in India · **80+** companies students have joined · **1:1** consulting · **~2 months** to a signed offer
- Kashish: 1 of 17 chosen by a panel of Deans · 500+ firms · 1,750+ placed · 1,000+ offers in 3 days · 30+ interviews at ~90%
- Sidhant / Skill Turtle: ~500 students placed
- **Up to 60% off.** This implies a list price people genuinely pay. If most clients get the discount, the $199–$1,199 prices become the fiction — that is the pricing claim the ACCC acts on. Safer framing if you want it: "packages start at $199, and we scale the price to your situation on the call."

## Page order

header (About · Program · Pricing + both CTAs, with the pinned offer ticker) → hero → a system built to get you hired (2×2) → how it works → packages → CTA band → the founders' story → the numbers → client stories → start your journey now (calendar + form side by side) → we would rather lose the sale → FAQ → footer

## Built in

- Sora display (all-lowercase), IBM Plex Sans body, IBM Plex Mono labels. Black ramp `#0A0A0A` / `#000` / `#050505`, one cream band, neon `#FFE83D`.
- Every text colour measured above 4.5:1. Tap targets ≥44px. Motion respects `prefers-reduced-motion`.
- Stats live as real values in the HTML and count up from there, so a JS failure shows the right number.
- FAQ JSON-LD mirrors the visible FAQ verbatim — **if you edit an answer, edit both.**
- Two independent form states, so the modal and the inline form never overwrite each other's confirmation.

## Self-critique

**What I'd change with more time:** the proof is thin for a page built on being checkable — two quotes with no employer and no link. A page like this converts on one verifiable outcome, so the highest-value next task is getting one client's LinkedIn announcement onto it, not any further design work.

**The aesthetic risk:** black plus one neon yellow is the pattern I was told to avoid. You asked for neon and it is your logo colour, so it is your call rather than mine; I kept the glow to three places (primary buttons, and nowhere else structural) and used the yellow as flat ink everywhere else so it reads as one decision instead of a page-wide sheen.
