# Nielsen's 10 Heuristics Scoring Guide

Score each heuristic 0-4. Be honest: 4 means genuinely excellent, not "good enough."
Most real interfaces score 20-32 out of 40.

## 1. Visibility of System Status
Keep users informed through timely feedback.
Check: loading indicators, action confirmations, progress indicators, navigation state,
inline form validation.
- 0: No feedback; user is guessing
- 1: Rare feedback; most actions produce no response
- 2: Partial; some states communicated, major gaps
- 3: Good; most operations give clear feedback, minor gaps
- 4: Every action confirms, progress always visible

## 2. Match Between System and Real World
Speak the user's language. Natural, logical order.
Check: familiar terminology, logical info order, recognizable icons, domain-appropriate
language, natural reading flow.
- 0: Pure tech jargon, alien to users
- 1: Mostly confusing; requires expertise to navigate
- 2: Mixed; some plain language, some jargon
- 3: Mostly natural; occasional term needs context
- 4: Speaks the user's language throughout

## 3. User Control and Freedom
Clear "emergency exit" from unwanted states.
Check: undo/redo, cancel buttons, clear navigation back, easy filter/search clearing,
escape from multi-step processes.
- 0: Users get trapped; no way out
- 1: Difficult exits; obscure paths
- 2: Some exits; main flows have escape, edge cases don't
- 3: Good; can exit and undo most actions
- 4: Full control; undo, cancel, back, escape everywhere

## 4. Consistency and Standards
Same words, situations, and actions mean the same thing.
Check: consistent terminology, same actions = same results, platform conventions,
visual consistency, consistent interaction patterns.
- 0: Inconsistent everywhere; feels stitched together
- 1: Many inconsistencies
- 2: Partially consistent; main flows match, details diverge
- 3: Mostly consistent; occasional deviation
- 4: Fully consistent; cohesive, predictable

## 5. Error Prevention
Prevent problems before they happen.
Check: destructive action confirmation, constraints preventing invalid input, smart
defaults, clear labels, autosave/draft recovery.
- 0: Errors easy to make; no guardrails
- 1: Few safeguards
- 2: Common errors caught, edge cases slip
- 3: Most error paths blocked proactively
- 4: Errors nearly impossible through smart constraints

## 6. Recognition Rather Than Recall
Minimize memory load. Make things visible.
Check: visible options, contextual help, recent items, autocomplete, labels on icons.
- 0: Heavy memorization required
- 1: Many hidden features, few visible cues
- 2: Main actions visible, secondary features hidden
- 3: Most things discoverable
- 4: Everything discoverable; no memorization needed

## 7. Flexibility and Efficiency of Use
Accelerators speed up expert interaction.
Check: keyboard shortcuts, customization, recent/favorites, bulk actions, power user
features that don't complicate basics.
- 0: One rigid path
- 1: Limited flexibility
- 2: Basic keyboard support, limited bulk actions
- 3: Good keyboard nav, some customization
- 4: Multiple paths, power features, customizable

## 8. Aesthetic and Minimalist Design
Every element serves a purpose.
Check: only necessary info visible, clear hierarchy, purposeful color, no decorative
clutter, focused layouts.
- 0: Overwhelming; everything competes equally
- 1: Cluttered; hard to find what matters
- 2: Main content clear, periphery noisy
- 3: Mostly clean; minor visual noise
- 4: Every element earns its pixel

## 9. Help Users Recover from Errors
Plain language, precise problem identification, constructive solution.
Check: plain language errors, specific problem identification, actionable recovery,
errors near source, non-blocking error handling.
- 0: Cryptic errors or no message
- 1: "Something went wrong" with no guidance
- 2: Names problem but not the fix
- 3: Identifies problem and offers next steps
- 4: Pinpoints issue, suggests fix, preserves user work

## 10. Help and Documentation
Easy to find, task-focused, concise.
Check: searchable help, contextual help, task-focused organization, scannable content,
accessible without leaving context.
- 0: No help available
- 1: Help exists but hard to find or irrelevant
- 2: Basic FAQ/docs, not contextual
- 3: Searchable, mostly task-focused
- 4: Right info at the right moment

## Score Bands

| Range | Rating | Meaning |
|-------|--------|---------|
| 36-40 | Excellent | Minor polish only; ship it |
| 28-35 | Good | Address weak areas, solid foundation |
| 20-27 | Acceptable | Significant improvements needed |
| 12-19 | Poor | Major UX overhaul required |
| 0-11 | Critical | Redesign needed; unusable |

## Issue Severity

| Priority | Name | Description |
|----------|------|-------------|
| P0 | Blocking | Prevents task completion. Fix immediately. |
| P1 | Major | Significant difficulty or confusion. Fix before release. |
| P2 | Minor | Annoyance, workaround exists. Fix in next pass. |
| P3 | Polish | Nice-to-fix, no real user impact. Fix if time permits. |

Tip: "Would a user contact support about this?" If yes, at least P1.
