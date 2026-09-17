---
name: meeting-notes-to-actions
description: >-
  Use when Shimi (or the team) pastes raw meeting notes, a transcript, WhatsApp/Slack
  dump, or messy Hebrew/English bullets and needs decisions + action items with owners
  and deadlines — not a full discussion summary.
---

# Meeting notes → decisions + action items

## Goal
Turn messy notes into **only**:
1. Decisions made
2. Action items (owner, deadline, dependency, status)
3. Open questions

Do **not** narrate the whole discussion. Skip small talk and repeated debate.

## Input you will get
- Raw notes / transcript / bullet dump (Hebrew and/or English)
- Optional: known people and their roles
- Optional: default timezone `Asia/Jerusalem`

If owner names are unclear, use the best short name from the notes and mark `(לא ודאי)`.
If no deadline was said, write `טרם נקבע` and suggest a reasonable default in parentheses only as a suggestion, clearly labeled.

## Output format (Hebrew)

```markdown
## החלטות
- ...

## משימות
| משימה | בעלים | דדליין | תלות | סטטוס |
|---|---|---|---|---|
| ... | ... | ... | ... | פתוח |

## שאלות פתוחות
- ...

## מה לא נכלל (בכוונה)
- נושאים שדובר עליהם בלי החלטה
```

## Rules
- One row per actionable task; verb-first (`לשלוח`, `לתקן`, `לאשר`).
- Prefer concrete tasks over vague ones (`לחשוב על שיווק` → ask or drop into open questions).
- Never invent attendees, commitments, or dates that were not in the notes.
- If the notes are empty of decisions, say so and list at most 3 clarifying questions.
- Keep the whole reply scannable in under ~60 seconds.

## Optional follow-up
After delivering the table, ask **one** question only if a critical owner or deadline is missing.
