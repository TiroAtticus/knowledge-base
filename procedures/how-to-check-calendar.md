# How to Check Calendar

**Last verified:** 2026-02-07
**Tools required:** exec (gog CLI), AppleScript (fallback)
**Estimated time:** 1 minute

## Steps

1. Get today's events:
   ```bash
   gog calendar events primary --today
   ```

2. Get tomorrow's events:
   ```bash
   gog calendar events primary --tomorrow
   ```

3. Get next 7 days (for weekly planning):
   ```bash
   gog calendar events primary --days 7
   ```

4. For each event, note:
   - Time and duration
   - Location (if any)
   - Attendees (if any)
   - Whether Matt needs prep time

5. Cross-reference with MEMORY.md deadlines:
   - Academic deadlines from course syllabi
   - Hey Spotless appointments
   - Personal events

6. Log the check in `memory/heartbeat-state.json`

## Fallback: AppleScript

If gog is unavailable:
```bash
osascript scripts/get-calendar-events.applescript
```

## Alert Thresholds

- **Event in < 2 hours** → WhatsApp alert immediately
- **Event tomorrow morning** → Include in evening wrap-up
- **Event in 3-7 days** → Include in morning briefing

## Common Failures

- **No calendar access** → Re-run `gog calendar auth`
- **Wrong calendar** → Check calendar ID (might be non-primary)
