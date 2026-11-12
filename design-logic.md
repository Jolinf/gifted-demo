# Gifted: design logic (demo)

Status: pitch demo, one apartment (Ezra Courts). Built 12 Nov 2026. Not for public release until the sample data is replaced.

## 0. Personality brief
- Feeling words: calm, warm, assured. Never: loud.
- Customer moment: someone on their phone planning a Lagos stay, checking whether the place looks as good as the post.
- The place: the apartment at night, warm LED coves and a crystal chandelier against grey and wood.
- Pace: slow.
- Levers:
  - Colour: navy and red, from the Kabana brand (client asked to keep it and change only the name). Red only on WhatsApp actions and the ribbon.
  - Type: Montserrat for the wordmark and UI, Cormorant Garamond italic for the tagline and section titles.
  - Shape: pills, thin hairlines.
  - Signature: a red ribbon under the GIFTED wordmark ("Every stay, a gift.").
  - Motion: slow fades, a 6-second muted hero loop of the real living room.
- The Kabana keyhole "A" is not used: it is Kabana's mark, not Gifted's.

## 1. Structure (agreed with Joshua)
Splash → hero (name, tagline, descriptor, Reach out, Explore shortlets) → listing cards → footer.
"Explore shortlets" and "More info" open a full-screen feed (#stay/ezra-courts):
- one apartment per screen, swiping up moves to the next one
- photos swipe sideways
- the key facts sit over a bottom tint
- Check availability (WhatsApp), Take the tour, Full details (bottom sheet)
The feed ends with a "more apartments on the way" card.

## 2. Tour
- Viewer: Pannellum 2.5.6 (MIT), self-hosted in /vendor. Chosen over Photo Sphere Viewer because these are partial panoramas, and Pannellum clamps the view to the image edges.
- Sources: no 360° capture exists. 8 stops are single photos reprojected to partial equirectangular images (about 70 to 97 degrees wide). The kitchen is stitched from video frames (19 to 31 s), about 144 degrees wide, and is softer than the rest.
- Labelled in the viewer: "Demo tour built from existing photos and video. Views are partial."
- Room links (#tour/ezra-courts/<room>) follow the walk-through video's route. The bathroom has no adjacency claim.

## 3. Data loading
- On arrival: hero still (~170 KB) and the card photo.
- Hero loop (~0.7 MB): starts after page load, portrait screens only; skipped under Save-Data or reduced motion.
- Feed photos: load only when the feed opens, then lazily as the visitor swipes.
- Tour: Pannellum and the panoramas (~0.4 to 0.7 MB per room) load only on "Take the tour", one room at a time.

## 4. Sample data (replace before going live)
- Rate ₦180,000/night, caution ₦100,000, 1-night minimum
- Check-in 2 pm, check-out 12 pm
- House rules
- WhatsApp number: +234 704 231 7680 (given by Joshua, 12 Nov 2026), set as WA_NUMBER in index.html.
- No Instagram handle.
- Amenities: confirmed by Joshua on 12 Nov 2026.
