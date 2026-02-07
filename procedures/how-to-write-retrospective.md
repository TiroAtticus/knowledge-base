# How to Write a Retrospective

**Last verified:** 2026-02-07
**Tools required:** file_write
**Estimated time:** 5 minutes

## When to Write One

- A task failed or produced unexpected results
- A workflow broke (gateway down, config invalid, skill error)
- You made a mistake that could recur
- Matt reported something wrong with your output

## Steps

1. **Create the file:**
   - Path: `knowledge-base/retrospectives/YYYY-MM-DD-<short-description>.md`
   - Example: `2026-02-08-email-triage-missed-urgent.md`

2. **Fill in the template:**

   ```markdown
   # [What Went Wrong] - [Date]

   ## What Happened
   Brief description of the failure. Be specific.

   ## Root Cause
   Why it happened. Dig one level deeper than the symptom.

   ## Impact
   What was affected. Quantify if possible (downtime, missed messages, wrong data).

   ## Fix Applied
   What was done to resolve it.

   ## Prevention
   What should be done differently next time to prevent recurrence.

   ## Procedure Updated?
   - [ ] Updated relevant procedure in `knowledge-base/procedures/`
   - [ ] Updated SOUL.md or AGENTS.md if needed
   - [ ] Shared learning with Matt if significant
   ```

3. **Update the related procedure** (if one exists) with the failure mode and fix

4. **Log in today's memory file** that you wrote a retrospective

## Quality Check

A good retrospective answers: "If I wake up fresh tomorrow with no memory of this, will this file tell me exactly what to avoid and why?"
