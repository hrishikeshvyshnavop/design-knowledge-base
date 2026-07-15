# Brand vs Product Register

## Brand Register

When design IS the product: landing pages, marketing, campaigns, portfolios, long-form.
A visitor's impression is the thing being made.

### Brand slop test
If someone could say "AI made that" without hesitation, it failed. The bar is
distinctiveness. A visitor should ask "how was this made?" not "which AI made this?"

### Brand typography
- Distinctive font choices. Use the reflex-reject list.
- Display serif + sans body for editorial; one committed sans for tech; warmer pairings
  for consumer; rule-breaking for creative.
- Modular scale with fluid `clamp()` for headings.

### Brand color
- Permission for Committed, Full palette, and Drenched strategies. Use them.
- A beige-and-slate landing page ignores the register.
- Color carries the brand. Don't hedge with neutrals.

### Brand layout
- Asymmetric compositions. Break the grid intentionally.
- Alternative: a strict visible grid as voice (brutalist / Swiss).
- Don't default to centering everything. Centered-stack hero with card grids = template.

### Brand permissions (things product can't afford)
- Ambitious first-load motion: reveals, scroll-triggered, typographic choreography.
- Single-purpose viewports: one dominant idea per fold.
- Typographic risk: enormous display, unexpected italics, hand-drawn headlines.
- Art direction per section: different visual worlds if the narrative demands it.

### Brand bans (on top of shared bans)
- Monospace as lazy "technical" shorthand on non-technical brands.
- Large rounded-corner icons above every heading.
- All-caps body copy (reserve for short labels).
- Timid palettes and average layouts. Safe = invisible.
- Zero imagery on briefs that imply it (restaurant, hotel, food, travel, fashion).
- Defaulting to editorial-magazine aesthetics on non-editorial briefs.

---

## Product Register

When design SERVES the product: app UIs, dashboards, admin, tools, authenticated
surfaces. The user is in a task.

### Product slop test
Not "would someone say AI made this." The test: would a user fluent in the category's
best tools (Linear, Figma, Notion, Raycast) trust this interface, or pause at every
subtly-off component? The bar is earned familiarity.

### Product typography
- System fonts are legitimate.
- One family is often right. No display/body pairing needed.
- Fixed rem scale, not fluid. Tighter ratio: 1.125-1.2.

### Product color
- Defaults to Restrained. Accent for primary actions and state only.
- State-rich semantic vocabulary is mandatory.
- A second neutral layer for sidebars, toolbars, panels.

### Product layout
- Predictable grids. Consistency IS an affordance.
- Standard navigation: top bar, side nav, breadcrumbs, tabs. Don't reinvent for flavor.
- Responsive = structural (collapse sidebar), not fluid typography.

### Product components
- Every interactive component has all 8 states.
- Skeleton states for loading, not spinners.
- Empty states that teach, not "nothing here."
- Consistent affordances across the surface.

### Product motion
- 150-250ms. Users are in flow; don't make them wait.
- State conveyance only. No decoration.
- No orchestrated page-load sequences.

### Product bans (on top of shared bans)
- Decorative motion that doesn't convey state.
- Inconsistent components across screens.
- Display fonts in labels, buttons, data.
- Reinventing standard affordances for flavor.
- Heavy color on inactive states.

### Product permissions
- System fonts and familiar defaults.
- Standard navigation patterns.
- Density: many rows, many labels, when users need it.
- Consistency over surprise.
