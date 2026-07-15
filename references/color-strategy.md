# Color Strategy

## The Strategy Axis

Pick a strategy before picking colors. Four steps on the commitment axis:

### Restrained
Tinted neutrals + one accent at 10% or less of the surface. Product default; brand
minimalism. The accent's rarity is the point; its scarcity is what makes it read as
decisive rather than noisy.

### Committed
One saturated color carries 30-60% of the surface. Brand default for identity-driven
pages. When committed, don't hedge with neutrals around the edges. Commit.

### Full Palette
3-4 named color roles, each used deliberately. Brand campaigns, product data
visualization. Each role earns its place.

### Drenched
The surface IS the color. Brand heroes, campaign pages. A single saturated color
across a hero is not excess; it's voice.

The "one accent at 10%" rule is Restrained only. Committed, Full palette, and Drenched
exceed it on purpose. Don't collapse every design to Restrained by reflex.

## OKLCH

Use OKLCH for all new colors. Benefits: perceptually uniform, wide-gamut, intuitive.

Key rule: reduce chroma as lightness approaches 0 or 100. High chroma at extremes
looks garish.

Never use `#000` or `#fff`. Tint every neutral toward the brand hue (chroma 0.005-0.01).

## Theme Decision

Dark vs light is never a default. Not dark "because tools look cool dark." Not light
"to be safe."

Write one sentence of physical scene: who uses this, where, under what ambient light,
in what mood. If the sentence doesn't force the answer, add detail.

Bad: "Observability dashboard" (doesn't force an answer).
Good: "SRE glancing at incident severity on a 27-inch monitor at 2am in a dim room"
(forces dark).

Run the sentence, not the category.

## State-Rich Semantic Colors

Product interfaces need a full semantic vocabulary:
- hover, focus, active, disabled, selected
- loading, error, warning, success, info

Standardize these across the entire surface. Accent color for primary actions, current
selection, and state indicators only; not decoration.

## Named References

Before picking a strategy, name a real reference:
"Klim Type Foundry orange drench", "Stripe purple-on-white restraint", "Liquid Death
acid-green full palette", "Mailchimp yellow full palette."

Unnamed ambition becomes beige.

## Product vs Brand Color

- **Product**: defaults to Restrained. A single surface can earn Committed, but
  Restrained is the floor. Accent for primary actions and state only.
- **Brand**: has permission for Committed, Full palette, and Drenched. Use them.
  A beige-and-slate landing page ignores the register.

Palette IS voice. A calm brand and a restless brand should not share palette mechanics.
Don't converge across projects.
