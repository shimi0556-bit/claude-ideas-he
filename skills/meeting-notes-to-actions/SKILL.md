---
name: meeting-notes-to-actions
description: >-
  Convert raw meeting notes, transcripts, WhatsApp/Slack dumps, or messy
  Hebrew/English bullets into decisions and an action table (owner, deadline,
  dependencies, status) — not a full discussion summary. Use when the user
  says סיכום ישיבה, משימות מהישיבה, action items, meeting notes, פרוטוקול,
  או להפוך הערות להחלטות/בעלים/דדליין.
---

# Meeting notes → decisions + action items

## Why
Raw notes bury commitments. A fixed table makes owners and deadlines scannable in under a minute and stops vague “נחשוב על זה” from looking like real work.

## Do this
1. Read the notes once. Extract **only** decisions, actionable tasks, and open questions.
2. Skip small talk, repeated debate, and topics with no decision.
3. Build the Hebrew output exactly in the format below.
4. Ask **at most one** follow-up question — only if a critical owner or deadline is missing.

## Output format (always)

```markdown
## החלטות
- ...

## משימות
| משימה | בעלים | דדליין | תלויות | סטטוס |
|---|---|---|---|---|
| ... | ... | ... | ... | פתוח |

## שאלות פתוחות
- ...

## מה לא נכלל (בכוונה)
- נושאים שדובר עליהם בלי החלטה
```

## Ambiguity rules
- Owner missing or unclear → `לא צוין` (do not invent names).
- Deadline not stated → `טרם נקבע` (optional suggested date only in parentheses, labeled `הצעה:`).
- Vague item (“לחשוב על שיווק”) → move to **שאלות פתוחות** or rewrite as a concrete verb-first task if the notes support it.
- Never invent attendees, commitments, or dates that were not in the notes.
- Default timezone: `Asia/Jerusalem` unless the notes say otherwise.
- Task text: verb-first Hebrew (`לשלוח`, `לתקן`, `לאשר`).

## Example

**Input (raw):**
> דיברנו על העלאת המצגת. שימי אמר שישלח ליוסי עד יום רביעי. לא החלטנו על התקציב. מישהו צריך לבדוק את הלוגו.

**Output:**

```markdown
## החלטות
- שימי ישלח את המצגת ליוסי עד יום רביעי

## משימות
| משימה | בעלים | דדליין | תלויות | סטטוס |
|---|---|---|---|---|
| לשלוח את המצגת ליוסי | שימי | יום רביעי | — | פתוח |
| לבדוק את הלוגו | לא צוין | טרם נקבע | — | פתוח |

## שאלות פתוחות
- מה מחליטים לגבי התקציב?

## מה לא נכלל (בכוונה)
- דיון כללי על המצגת בלי פרטים נוספים
```
