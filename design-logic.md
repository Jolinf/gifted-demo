# Gifted Homes and Apartments: design logic

Status: full storefront, 3 apartments. Built 13 Nov 2026. It replaces giftedhomesandapartments.com; the owner agreed to the change.
The only demo part is the Ezrahaus 360° tour, a preview built from existing photos and video.

## 0. Personality brief
- Feeling words: calm, warm, assured. Never: loud.
- Customer moment: someone on their phone planning a Lagos stay, checking whether the place looks as good as the post.
- The place: a Lekki apartment at night, with warm LED coves, chandeliers, and grey and wood finishes.
- Pace: slow.
- Identity comes from Gifted's existing brand, taken from their current site:
  - Logo: the roofline mark plus "GIFTED HOMES & APARTMENTS". It is recoloured to cream for dark backgrounds.
  - Colours: navy #1E2A3B, cream #F6F2EC, copper #9A5A31 (main action colour) and gold #C9A46A (accent).
  - Type: Marcellus for display, Outfit for body.
- TELDEV choices:
  - a dark navy canvas
  - a gold rule under the name
  - "Every stay, a gift." (a shortened form of their line "Every stay should feel like a gift")
  - a 6-second hero loop of the real Ezrahaus living room

## 1. Structure
- Page: splash → hero (name, tagline, line, Reach out, Explore shortlets) → 3 listing cards → footer.
- Footer contents: WhatsApp, phone, email, Instagram, TikTok, office, hours, homeowner management.
- Feed (#stay/<slug>):
  - one apartment per screen
  - photos swipe sideways
  - key facts over a bottom tint
  - Check availability (WhatsApp, apartment named), Take the tour (Ezrahaus only; "Tour coming soon" disabled on the others), Full details
  - ends with a "Not sure which one?" card
- Details sheet:
  - specs and price
  - About and Features (from Gifted's own listings)
  - Good to know (from their FAQ)
  - area-only map link
  - Airbnb link where listed (secondary action only)

## 2. Content sources
- All listing data comes from giftedhomesandapartments.com/api/properties (public), read on 13 Nov 2026.
- Dropped as out of scope: Paystack online booking, the reviews form, and the multi-page navigation.
- The current site lists no published reviews, so there is no reviews section.
- Exact street addresses (Jeyden's is public on the old site) are not shown, by the shortlet rule. The area is shown; the address goes out after booking.

## 3. Tour (Ezrahaus)
- Pannellum 2.5.6 (MIT), self-hosted. 9 partial views:
  - 8 come from single camera photos reprojected
  - the kitchen is stitched from video frames
- Their site has no extra Ezrahaus media: the same photo set and no video.
- Labelled "Preview tour built from existing photos and video. Views are partial."

## 4. Data loading
- On arrival: hero still, logo and 3 card photos.
- Hero loop (~0.7 MB): portrait only, after load; skipped under Save-Data or reduced motion.
- Feed: an apartment's photos load only when its screen is shown, plus the first photo of the next one.
- Tour: code and panoramas load only on "Take the tour", one room at a time.

## 5. Open items
- WhatsApp: +234 904 516 5367 (confirmed by Joshua, 14 Nov 2026). It is also the phone number in the footer.
- The office address differs on their own site: G1/G2 Shonny Highway vs 4 Olatunbosun Street, both in Shonibare Estate, Maryland. The page shows "Shonibare Estate, Maryland" and uses their Maps link.
- Ezrahaus is listed with 3 bathrooms but the same 250 m² as the others. Confirm the sizes.
