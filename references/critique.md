# Design Critique Framework

## Full Critique Process

### Step 1: AI Slop Check
Review against ALL absolute bans from the main skill. Check for: AI color palette,
gradient text, dark glows, glassmorphism, hero-metric layouts, identical card grids,
side-stripe borders. Run both levels of the category-reflex check.

The test: if someone said "AI made this," would you believe them immediately?

### Step 2: Heuristic Scoring
Score Nielsen's 10 heuristics 0-4 each. See heuristics.md.
Present as a table with score and key issue per heuristic.
Total out of 40. Be honest; most real interfaces score 20-32.

### Step 3: Cognitive Load Assessment
Run the 8-item checklist from cognitive-load.md.
Count failures: 0-1 = low (good), 2-3 = moderate, 4+ = critical.
Count visible options at each decision point. Flag if more than 4.
Check for progressive disclosure.

### Step 4: Emotional Journey
- What emotion does this interface evoke? Is that intentional?
- Peak-end rule: is the most intense moment positive? Does it end well?
- Emotional valleys: check for anxiety at high-stakes moments (payment, delete).
  Are there interventions (progress indicators, reassurance, undo)?

### Step 5: Persona Walk-through
Select 2-3 personas from personas.md based on interface type.
Walk through the primary user action as each persona.
Report specific red flags, not generic concerns.

## Report Structure

### 1. AI Slop Verdict
Does this look AI-generated? Overall aesthetic feel, layout sameness, missed
opportunities for personality.

### 2. Heuristic Score Table
| # | Heuristic | Score | Key Issue |
Present all 10. Total and rating band.

### 3. Overall Impression
Brief gut reaction: what works, what doesn't, single biggest opportunity.

### 4. What's Working
2-3 things done well. Be specific about why they work.

### 5. Priority Issues
3-5 most impactful problems, ordered by importance.

For each:
- **[P?] What**: Name the problem
- **Why it matters**: How it hurts users or undermines goals
- **Fix**: Concrete suggestion

### 6. Persona Red Flags
For each selected persona, specific failures found:

"Alex (Power User): No keyboard shortcuts. Form requires 8 clicks for primary action.
Forced modal onboarding."

"Jordan (First-Timer): Icon-only nav in sidebar. Technical jargon in error messages.
No visible help. Will abandon at step 2."

### 7. Minor Observations
Quick notes on smaller issues.

### 8. Questions to Consider
Provocative questions that might unlock better solutions.

## Feedback Rules

- Be direct. Vague feedback wastes time.
- Be specific. "The submit button," not "some elements."
- Say what's wrong AND why it matters to users.
- Give concrete suggestions. Cut "consider exploring..."
- Prioritize ruthlessly. If everything is important, nothing is.
- Don't soften criticism. Honest feedback ships great design.
- Critique the work, not the person.
- Lead with what's working before addressing problems.
