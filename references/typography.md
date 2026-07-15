# Typography

## Font Selection Procedure (Brand Work)

Every project. Never skip.

1. Write three concrete brand-voice words. Not "modern" or "elegant" but "warm and
   mechanical and opinionated" or "calm and clinical and careful." Physical-object words.
2. List the three fonts you'd reach for by reflex. If any appear on the reflex-reject
   list, reject them; they are training-data defaults that create monoculture.
3. Browse a real catalog (Google Fonts, Pangram Pangram, Future Fonts, Adobe Fonts, ABC
   Dinamo, Klim, Velvetyne) with the three words in mind. Find the font as a physical
   object: a museum caption, a 1970s terminal manual, a fabric label, a concert poster.
4. Cross-check. "Elegant" is not necessarily serif. "Technical" is not necessarily sans.
   If the final pick matches the original reflex, start over.

## Reflex-Reject List (Brand Work)

Training-data defaults. Ban for brand register. Look further:

Fraunces, Newsreader, Lora, Crimson, Crimson Pro, Crimson Text, Playfair Display,
Cormorant, Cormorant Garamond, Syne, IBM Plex Mono, IBM Plex Sans, IBM Plex Serif,
Space Mono, Space Grotesk, Inter, DM Sans, DM Serif Display, DM Serif Text, Outfit,
Plus Jakarta Sans, Instrument Sans, Instrument Serif.

These are fine for product register (Inter, system-ui stacks). The ban is for brand
work where distinctiveness matters.

## Product UI Typography

- System fonts are legitimate. `-apple-system, BlinkMacSystemFont, system-ui, sans-serif`
- One family is often right. Product UIs don't need display/body pairing.
- Fixed rem scale, not fluid. Clamp-sized headings don't serve product UI.
- Tighter scale ratio: 1.125-1.2 between steps.
- Line length still 65-75ch for prose. Tables can run denser.

## Type Scale

Use modular scale with fluid `clamp()` for headings, 1.25 ratio or more between steps.
Flat scales (1.1x apart) read as uncommitted.

Minimum hierarchy:
- Display / Hero: largest, lightest weight, reserved for one moment
- Heading: section-level
- Title / Subheading: subsection
- Body: 1rem, 1.6 line-height
- Supporting: 0.875rem, captions and metadata
- Label: weight 500, uppercase for CTAs
- Micro: 0.6875rem, metadata

## Line Height

- Body: 1.6. Not 1.5, not 1.7. This is the readability decision.
- Light text on dark backgrounds: add 0.05-0.1 to line-height.

## Pairing by Register

- Editorial / luxury: display serif + sans body
- Tech / dev tools: one committed sans with strong weight contrast
- Consumer / food / travel: warmer pairings, humanist sans + display serif
- Creative studios: rule-breaking welcome. Mono-only, display-only, or custom

Two families minimum is the rule only when the voice needs it. One well-chosen
family with weight/size contrast is stronger than a timid pair.

## Saturated Aesthetic Lanes (Brand)

Currently oversaturated families to avoid in greenfield brand work:

- **Editorial-typographic**: Display serif + italic + mono labels + ruled separators +
  monochromatic restraint. By 2026, every Stripe-adjacent brand has landed here.
