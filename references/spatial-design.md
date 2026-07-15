# Spatial Design

## Spacing Systems

Use 4pt base, not 8pt. 8pt is too coarse; you'll need 12px constantly.
Scale: 4, 8, 12, 16, 24, 32, 48, 64, 96px.

Name tokens semantically (`--space-sm`, `--space-lg`), not by value (`--spacing-8`).
Use `gap` instead of margins for sibling spacing; eliminates margin collapse.

## Grid Systems

### Self-Adjusting Grid
`repeat(auto-fit, minmax(280px, 1fr))` for responsive grids without breakpoints.
For complex layouts, use named grid areas and redefine at breakpoints.

### Container Queries
Viewport queries are for page layouts. Container queries are for components:

```css
.card-container { container-type: inline-size; }
@container (min-width: 400px) {
  .card { grid-template-columns: 120px 1fr; }
}
```

A card in a narrow sidebar stays compact; the same card in main content expands.

## Visual Hierarchy

### The Squint Test
Blur your eyes (or screenshot and blur). Can you identify:
- The most important element?
- The second most important?
- Clear groupings?

If everything looks the same weight, you have a hierarchy problem.

### Multiple Dimensions
Don't rely on size alone. Combine:

| Tool | Strong | Weak |
|------|--------|------|
| Size | 3:1 ratio or more | Less than 2:1 |
| Weight | Bold vs Regular | Medium vs Regular |
| Color | High contrast | Similar tones |
| Position | Top/left (primary) | Bottom/right |
| Space | Surrounded by whitespace | Crowded |

Best hierarchy uses 2-3 dimensions at once.

## Cards Are Not Required

Cards are overused. Spacing and alignment create grouping naturally. Use cards only when:
content is truly distinct and actionable, items need visual comparison in a grid, or
content needs clear interaction boundaries. Never nest cards inside cards.

## Optical Adjustments

- Text at `margin-left: 0` looks indented due to letterform whitespace; use negative
  margin (-0.05em) to optically align.
- Geometrically centered icons look off-center. Play icons shift right, arrows shift
  toward their direction.

## Touch Targets vs Visual Size

Buttons can look small but need 44px minimum touch targets. Use padding or
pseudo-elements to expand the hit area.

## Depth & Elevation

Semantic z-index scale: dropdown (100), sticky (200), modal-backdrop (300), modal (400),
toast (500), tooltip (600). Never arbitrary numbers.

Shadows should be subtle. If you can clearly see it, it's probably too strong.
Flat by default. Shadows appear only on hover or deliberate elevation.
