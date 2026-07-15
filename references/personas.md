# Persona-Based Design Testing

Test the interface through 5 user archetypes. Each exposes different failure modes.
Select 2-3 most relevant to the interface. Walk through the primary action. Report
specific red flags, not generic concerns.

## 1. Impatient Power User: "Alex"

Expert with similar products. Expects efficiency, hates hand-holding.

Test: Can Alex complete the core task in under 60 seconds? Keyboard shortcuts? Skip
onboarding? Bulk actions? Esc to dismiss modals?

Red flags: Forced tutorials, no keyboard nav, slow unskippable animations, one-item-
at-a-time workflows, redundant confirmations for low-risk actions.

## 2. Confused First-Timer: "Jordan"

Never used this type of product. Needs guidance. Will abandon rather than figure it out.

Test: First action obvious in 5 seconds? All icons labeled? Contextual help at decision
points? Terminology assumes prior knowledge? Clear back/undo at every step?

Red flags: Icon-only navigation, jargon without explanation, no help option, ambiguous
next steps, no success confirmation.

## 3. Accessibility-Dependent User: "Sam"

Uses screen reader, keyboard-only. May have low vision or motor impairment.

Test: Entire flow keyboard-only? All elements focusable with visible focus? Meaningful
alt text? Contrast WCAG AA (4.5:1)? Screen reader announces state changes?

Red flags: Click-only interactions, missing focus indicators, color-only meaning,
unlabeled fields/buttons, time-limited actions, custom components breaking screen
reader flow.

## 4. Deliberate Stress Tester: "Riley"

Pushes beyond the happy path. Tests edge cases, unexpected inputs, probes for gaps.

Test: What happens at 0 items? 1000 items? Very long text? Error recovery? Refresh
mid-workflow? Multiple tabs?

Red flags: Silent failures, broken error states, empty states with no guidance,
data loss on refresh, inconsistent behavior across similar interactions.

## 5. Distracted Mobile User: "Casey"

Phone, one-handed, on the go. Frequently interrupted. Possibly slow connection.

Test: Primary actions in thumb zone (bottom half)? State preserved on leave/return?
Works on 3G? Smart defaults to reduce typing? Touch targets 44x44 minimum?

Red flags: Important actions at top of screen, no state persistence, large text
inputs where selection works, heavy assets with no lazy loading, tiny tap targets.

## Persona Selection Guide

| Interface Type | Use These | Why |
|---------------|-----------|-----|
| Landing page / marketing | Jordan, Riley, Casey | First impressions, trust, mobile |
| Dashboard / admin | Alex, Sam | Power users, accessibility |
| E-commerce / checkout | Casey, Riley, Jordan | Mobile, edge cases, clarity |
| Onboarding flow | Jordan, Casey | Confusion, interruption |
| Data-heavy / analytics | Alex, Sam | Efficiency, keyboard nav |
| Form-heavy / wizard | Jordan, Sam, Casey | Clarity, accessibility, mobile |

## Writing Persona Red Flags

Be specific. Name exact elements and interactions.

Good: "No keyboard shortcuts detected. Form requires 8 clicks for primary action.
Forced modal onboarding. High abandonment risk."

Bad: "Alex might find this frustrating because it's not efficient enough."
