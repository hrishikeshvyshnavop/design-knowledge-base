# UX Writing

## Button Labels

Never "OK", "Submit", or "Yes/No". Use specific verb + object:

| Bad | Good | Why |
|-----|------|-----|
| OK | Save changes | Says what happens |
| Submit | Create account | Outcome-focused |
| Yes | Delete message | Confirms the action |
| Cancel | Keep editing | Clarifies what cancel means |
| Click here | Download PDF | Describes destination |

For destructive actions, name the destruction: "Delete 5 items" not "Delete selected".

## Error Messages: The Formula

Every error answers: (1) What happened? (2) Why? (3) How to fix it?

| Situation | Template |
|-----------|----------|
| Format error | "[Field] needs to be [format]. Example: [example]" |
| Missing required | "Please enter [what's missing]" |
| Permission denied | "You don't have access to [thing]. [What to do instead]" |
| Network error | "We couldn't reach [thing]. Check your connection and [action]." |
| Server error | "Something went wrong on our end. [Alternative action]" |

Don't blame the user: "Please enter a date in MM/DD/YYYY format" not "You entered an
invalid date."

## Empty States Are Opportunities

1. Acknowledge briefly
2. Explain the value of filling it
3. Provide a clear action

"No projects yet. Create your first one to get started." not "No items."

## Voice vs Tone

Voice is your brand personality, consistent everywhere.
Tone adapts to the moment:

| Moment | Tone |
|--------|------|
| Success | Celebratory, brief: "Done! Your changes are live." |
| Error | Empathetic, helpful: "That didn't work. Here's what to try..." |
| Loading | Reassuring: "Saving your work..." |
| Destructive confirm | Serious, clear: "Delete this project? This can't be undone." |

Never use humor for errors. Users are already frustrated.

## Accessibility in Writing

- Link text must stand alone: "View pricing plans" not "Click here"
- Alt text describes information: "Revenue increased 40% in Q4" not "Chart"
- `alt=""` for decorative images
- Icon buttons need `aria-label`

## Translation Planning

German is ~30% longer than English. Allocate space. Keep numbers separate. Use full
sentences as single strings. Avoid abbreviations. Give translators context.

## Consistency

Pick one term. Stick with it:

| Inconsistent | Consistent |
|--------------|------------|
| Delete / Remove / Trash | Delete |
| Settings / Preferences / Options | Settings |
| Sign in / Log in | Sign in |
| Create / Add / New | Create |

## Loading States

Be specific: "Saving your draft..." not "Loading...". For long waits, set expectations
or show progress.

## Confirmation Dialogs

Most are design failures; consider undo instead. When you must: name the action, explain
consequences, use specific labels ("Delete project" / "Keep project", not "Yes" / "No").
