# Interaction Design

## The Eight Interactive States

Every interactive element needs these designed:

| State | When | Visual Treatment |
|-------|------|------------------|
| Default | At rest | Base styling |
| Hover | Pointer over (not touch) | Subtle lift, color shift |
| Focus | Keyboard/programmatic focus | Visible ring |
| Active | Being pressed | Pressed in, darker |
| Disabled | Not interactive | Reduced opacity, no pointer |
| Loading | Processing | Spinner, skeleton |
| Error | Invalid state | Red border, icon, message |
| Success | Completed | Green check, confirmation |

Common miss: designing hover without focus. Keyboard users never see hover states.

## Focus Rings

Never `outline: none` without replacement. Use `:focus-visible` for keyboard-only:

```css
button:focus { outline: none; }
button:focus-visible {
  outline: 2px solid var(--color-accent);
  outline-offset: 2px;
}
```

Focus ring design: high contrast (3:1 minimum), 2-3px thick, offset from element,
consistent across all interactive elements.

## Form Design

- Placeholders aren't labels. They disappear. Always use visible `<label>`.
- Validate on blur, not every keystroke (except password strength).
- Errors below fields with `aria-describedby` connecting them.
- Group fields by topic, not by type.
- 4 or fewer fields per visual group.

## Loading States

- Optimistic updates: show success immediately, rollback on failure. For low-stakes
  actions only (likes, follows), not payments or destructive actions.
- Skeleton screens > spinners. They preview content shape and feel faster.

## Modals: The Inert Approach

Use native `<dialog>` element with `.showModal()` for focus trap + Esc dismiss.
For non-modal overlays, use the Popover API (`popover` attribute) for light-dismiss,
proper stacking, and accessibility.

## Dropdown Positioning

Dropdowns with `position: absolute` inside `overflow: hidden` containers will be
clipped. This is the most common dropdown bug in generated code.

Solutions in order of preference:
1. Popover API (`popover` attribute) for top-layer rendering
2. CSS Anchor Positioning (Chrome 125+)
3. Portal/Teleport to document body
4. `position: fixed` with manual coordinates

Anti-patterns: `position: absolute` inside overflow containers, arbitrary `z-index:
9999`, inline dropdown markup without escape hatch.

## Destructive Actions: Undo > Confirm

Undo is better than confirmation dialogs. Users click through confirmations mindlessly.
Remove from UI immediately, show undo toast, delete after toast expires.
Use confirmation only for: truly irreversible (account deletion), high-cost, or batch.

## Keyboard Navigation

- Roving tabindex for component groups (tabs, menus, radios): one item tabbable,
  arrow keys move within.
- Skip links for keyboard users to bypass navigation.
- Every gesture (swipe, long-press) needs a visible fallback.

## Touch Targets

Minimum 44x44px. Buttons can look small but need large touch targets. Use padding or
pseudo-elements to expand the hit area beyond the visual boundary.
