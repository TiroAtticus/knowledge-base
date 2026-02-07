# Retrospectives - Learning from Mistakes

This directory contains post-mortems and failure analyses. Every time something goes wrong, document it here so future-Tiro doesn't repeat the mistake.

## Format

Each file: `YYYY-MM-DD-<short-description>.md`

Example: `2026-02-07-config-string-number-mismatch.md`

## Template

```markdown
# [What Went Wrong] - [Date]

## What Happened
Brief description of the failure.

## Root Cause
Why it happened.

## Impact
What was affected (downtime, missed messages, etc.).

## Fix Applied
What was done to fix it.

## Prevention
What should be done differently next time.

## Procedure Updated?
- [ ] Updated relevant procedure in `knowledge-base/procedures/`
- [ ] Updated SOUL.md or AGENTS.md if needed
- [ ] Shared learning with Matt if significant
```

## Review Schedule

During weekly heartbeat reviews (see HEARTBEAT.md):
1. Read all retrospectives from the past week
2. Check if prevention measures are in place
3. Update procedures with lessons learned
4. Archive old retrospectives that are fully resolved

## Why This Matters

Humans learn from mistakes. So should Tiro. Without retrospectives, the same errors repeat across sessions because memory resets.
