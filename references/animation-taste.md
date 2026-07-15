# Animation & Design Taste

Based on Emil Kowalski's design engineering philosophy. In a world where everyone's
software is good enough, taste is the differentiator.

## Core Philosophy

**Taste is trained, not innate.** Good taste is a trained instinct: the ability to see
beyond the obvious and recognize what elevates. Study why the best interfaces feel the
way they do. Reverse engineer animations. Inspect interactions.

**Unseen details compound.** Most details users never consciously notice. That is the
point. The aggregate of invisible correctness creates interfaces people love without
knowing why.

**Beauty is leverage.** People select tools based on overall experience, not just
functionality. Good defaults and good animations are real differentiators.

## The Animation Decision Framework

Before writing any animation code, answer these in order:

### 1. Should this animate at all?

| Frequency | Decision |
|-----------|----------|
| 100+ times/day (keyboard shortcuts, command palette) | No animation. Ever. |
| Tens of times/day (hover effects, list navigation) | Remove or drastically reduce |
| Occasional (modals, drawers, toasts) | Standard animation |
| Rare/first-time (onboarding, celebrations) | Can add delight |

Never animate keyboard-initiated actions. They're repeated hundreds of times daily.

### 2. What is the purpose?

Valid purposes only: spatial consistency (toast enters/exits same direction), state
indication (morphing button shows state change), explanation (shows how a feature
works), feedback (button scales on press), preventing jarring changes (elements
appearing without transition feel broken).

If the purpose is just "it looks cool" and it's seen often, don't animate.

### 3. What easing?

- Element entering or exiting? **ease-out** (starts fast, feels responsive)
- Moving/morphing on screen? **ease-in-out** (natural acceleration/deceleration)
- Hover/color change? **ease**
- Constant motion (marquee, progress)? **linear**
- Default: **ease-out**

**Use custom easing curves.** Built-in CSS easings are too weak:
```css
--ease-out: cubic-bezier(0.23, 1, 0.32, 1);
--ease-in-out: cubic-bezier(0.77, 0, 0.175, 1);
--ease-drawer: cubic-bezier(0.32, 0.72, 0, 1);
```

**Never use ease-in for UI.** It starts slow, making the interface feel sluggish.

### 4. How fast?

| Element | Duration |
|---------|----------|
| Button press feedback | 100-160ms |
| Tooltips, small popovers | 125-200ms |
| Dropdowns, selects | 150-250ms |
| Modals, drawers | 200-500ms |
| Marketing/explanatory | Can be longer |

Rule: UI animations under 300ms. 180ms dropdown feels more responsive than 400ms.

## Component Polish Rules

### Buttons must feel responsive
Add `transform: scale(0.97)` on `:active`. Subtle (0.95-0.98) with 160ms ease-out.

### Never animate from scale(0)
Nothing in the real world disappears completely. Start from `scale(0.95)` with
`opacity: 0`. Even barely-visible initial scale makes entrance feel natural.

### Popovers: origin-aware
Popovers scale from their trigger, not center. Use `transform-origin` from Radix/Base
UI CSS variables. Exception: modals keep `transform-origin: center` (not anchored).

### Tooltips: skip delay on subsequent hovers
First tooltip delays. Once one is open, adjacent tooltips open instantly with no
animation. Feels faster without defeating the initial delay purpose.

### Asymmetric enter/exit timing
Pressing should be slow when deliberate (hold-to-delete: 2s linear). Release always
snappy (200ms ease-out). Slow where user decides, fast where system responds.

### Stagger animations
Multiple elements entering together: stagger 30-80ms between items. Keep delays short;
long delays feel slow. Never block interaction during stagger.

## Spring Animations

Use springs for: drag with momentum, elements that feel "alive", interruptible
gestures, decorative mouse-tracking. Springs maintain velocity when interrupted (CSS
animations restart from zero).

Apple's approach: `{ type: "spring", duration: 0.5, bounce: 0.2 }`
Keep bounce subtle (0.1-0.3). Avoid bounce in most UI contexts.

## Performance Rules

### Only animate transform and opacity
These skip layout and paint, running on GPU. Animating padding, margin, height, width
triggers all three rendering steps.

### CSS animations beat JS under load
CSS animations run off main thread. When the browser is busy, Framer Motion animations
(requestAnimationFrame) drop frames. CSS stays smooth. Use CSS for predetermined
animations; JS for dynamic, interruptible ones.

### Framer Motion hardware acceleration
Shorthand properties (x, y, scale) are NOT hardware-accelerated. Use full transform:
```jsx
// NOT hardware accelerated
<motion.div animate={{ x: 100 }} />
// Hardware accelerated
<motion.div animate={{ transform: "translateX(100px)" }} />
```

### CSS transitions over keyframes for dynamic UI
Transitions can be interrupted and retargeted. Keyframes restart from zero. For
rapidly-triggered interactions (toasts, toggles), transitions are smoother.

### Use WAAPI for programmatic CSS animations
Web Animations API: JavaScript control with CSS performance. Hardware-accelerated,
interruptible, no library needed.

## Advanced Techniques

### clip-path for animation
`clip-path: inset()` is one of the most powerful animation tools. Use for: tab color
transitions (duplicate + clip active), hold-to-delete (reveal overlay), image reveals
on scroll, comparison sliders.

### Blur to mask imperfect transitions
When crossfade feels off, add subtle `filter: blur(2px)` during transition. Bridges
the visual gap between two states. Keep under 20px (expensive in Safari).

### @starting-style for CSS entry animations
Modern CSS element entry without JavaScript:
```css
.toast {
  opacity: 1; transform: translateY(0);
  transition: opacity 400ms ease, transform 400ms ease;
  @starting-style { opacity: 0; transform: translateY(100%); }
}
```

## Gesture & Drag

- Momentum-based dismissal: calculate velocity, dismiss if > 0.11 regardless of distance
- Damping at boundaries: the more you drag past the edge, the less it moves
- Pointer capture: once dragging starts, capture all pointer events
- Multi-touch protection: ignore additional touch points after drag begins
- Friction over hard stops: allow overdrag with increasing resistance

## Review Checklist

| Issue | Fix |
|-------|-----|
| `transition: all` | Specify exact properties |
| `scale(0)` entry | Start from `scale(0.95)` with `opacity: 0` |
| `ease-in` on UI element | Switch to `ease-out` or custom curve |
| `transform-origin: center` on popover | Set to trigger location (modals exempt) |
| Animation on keyboard action | Remove entirely |
| Duration > 300ms on UI element | Reduce to 150-250ms |
| Hover without media query | Add `@media (hover: hover) and (pointer: fine)` |
| Keyframes on rapid trigger | Use CSS transitions |
| Same enter/exit speed | Make exit faster than enter |
| Elements all appear at once | Add stagger (30-80ms) |
| No :active state on button | Add `transform: scale(0.97)` |

## The Sonner Principles (Building Loved Components)

1. **Developer experience is key.** Minimal setup. Insert once, use from anywhere.
2. **Good defaults matter more than options.** Most users never customize.
3. **Handle edge cases invisibly.** Pause timers on hidden tabs, fill gaps between
   stacked elements, capture pointer during drag. Users never notice, and that's right.
4. **Match motion to mood.** Playful = bouncier. Professional dashboard = crisp and fast.
5. **Review with fresh eyes.** Check animations next day. Play in slow motion.
