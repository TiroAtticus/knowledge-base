# How to Do Morning Briefing

**Last verified:** 2026-02-07
**Tools required:** exec (gog CLI), web search, browser (optional)
**Estimated time:** 3-5 minutes
**Schedule:** 7:00 AM daily via cron

## Steps

1. **Check Calendar** (see `how-to-check-calendar.md`):
   ```bash
   gog calendar events primary --today
   gog calendar events primary --tomorrow
   ```

2. **Check Email** (see `how-to-check-email.md`):
   ```bash
   gog gmail search "is:unread newer_than:1d" --max 20
   ```

3. **Check Weather** (Matt is in Montgomery, Alabama):
   - Use web search: "weather Montgomery AL today"
   - Note if rain/extreme temps (affects golf, commute)

4. **Check Deadlines** from MEMORY.md:
   - Use `memory_search("deadline")` or `memory_search("due")`
   - Cross-reference with today's date
   - Flag anything due within 72 hours

5. **Review Yesterday's Memory** (`memory/YYYY-MM-DD.md`):
   - Any incomplete tasks from yesterday?
   - Any follow-ups needed?

6. **Compose Briefing** using this template:
   ```
   Good morning Matt ☀️

   TODAY [Day, Date]:
   • [Calendar events with times]
   • [Deadlines approaching]

   PRIORITIES:
   1. [Most important/urgent task]
   2. [Second priority]
   3. [Third priority]

   HEADS UP:
   • [Urgent emails, if any]
   • [Weather note, if relevant]
   • [Anything else noteworthy]
   ```

7. **Send via WhatsApp** to Matt

8. **Log** to today's `memory/YYYY-MM-DD.md`

## Quality Checklist

- [ ] Calendar checked (today + tomorrow)
- [ ] Email scanned (urgent flagged)
- [ ] Weather checked
- [ ] Deadlines cross-referenced
- [ ] Yesterday's loose ends addressed
- [ ] Briefing sent to WhatsApp
- [ ] Memory file updated

## Common Failures

- **No calendar data** → Fallback to MEMORY.md deadlines only
- **gog auth expired** → Note in briefing: "Calendar access needs re-auth"
- **Empty day** → Still send: "Light day today. Good time for [proactive suggestion]"
