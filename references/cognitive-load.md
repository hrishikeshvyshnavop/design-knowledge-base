# Cognitive Load Assessment

Cognitive load is the total mental effort required to use an interface. Overloaded users
make mistakes, get frustrated, and leave.

## Three Types

### Intrinsic Load: The Task Itself
Complexity inherent to the task. Can't eliminate, but can structure it.
Manage by: breaking complex tasks into steps, providing scaffolding (templates, defaults,
examples), progressive disclosure, grouping related decisions.

### Extraneous Load: Bad Design
Mental effort from poor design choices. Eliminate ruthlessly. Pure waste.
Common sources: confusing navigation, unclear labels, visual clutter, inconsistent
patterns, unnecessary steps between intent and result.

### Germane Load: Learning Effort
Mental effort building understanding. This is good cognitive load.
Support by: progressive disclosure, consistent patterns, feedback that confirms
understanding, onboarding through action not text walls.

## The 8-Item Checklist

Evaluate the interface against these:

1. **Single focus**: Can the user complete the primary task without distraction?
2. **Chunking**: Is information in digestible groups (4 items or fewer per group)?
3. **Grouping**: Are related items visually grouped (proximity, borders, background)?
4. **Visual hierarchy**: Is it immediately clear what's most important?
5. **One thing at a time**: Can the user focus on one decision before the next?
6. **Minimal choices**: Are decisions simplified (4 or fewer visible options)?
7. **Working memory**: Must the user remember info from a previous screen?
8. **Progressive disclosure**: Is complexity revealed only when needed?

**Scoring**: 0-1 failures = low (good). 2-3 = moderate (address soon). 4+ = critical.

## The Working Memory Rule

Humans hold 4 items or fewer in working memory (Cowan, 2001).

At any decision point, count simultaneous options/actions/information:
- 4 or fewer: manageable
- 5-7: pushing it; group or use progressive disclosure
- 8+: overloaded; users will skip, misclick, or abandon

Practical limits:
- Navigation menus: 5 or fewer top-level items
- Form sections: 4 or fewer fields per group before a visual break
- Action buttons: 1 primary, 1-2 secondary, group the rest in a menu
- Dashboard widgets: 4 or fewer key metrics without scrolling
- Pricing tiers: 3 or fewer options

## Common Violations

1. **Wall of Options**: 10+ choices, no hierarchy. Fix: group, highlight recommended,
   progressive disclosure.
2. **Memory Bridge**: Must remember step 1 info at step 3. Fix: keep context visible.
3. **Hidden Navigation**: Must build mental map. Fix: show current location always.
4. **Jargon Barrier**: Technical language forces translation. Fix: plain language.
5. **Visual Noise Floor**: Everything same weight. Fix: clear hierarchy.
6. **Inconsistent Pattern**: Same actions work differently. Fix: standardize.
7. **Multi-Task Demand**: Process multiple simultaneous inputs. Fix: sequence the steps.
8. **Context Switch**: Jump between screens for one decision. Fix: co-locate info.
