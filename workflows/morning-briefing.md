# Morning Briefing Workflow

## Timing
- 7:00 AM daily

## Steps
1. Check calendar for the day
2. Scan emails (Gmail via gog CLI)
3. Check Canvas for deadlines
4. Generate priority tasks
5. Send briefing to Matt via WhatsApp

## Template
```
Good morning! ☀️

TODAY [DATE]:
- [Events from calendar]
- [Deadlines]

PRIORITIES:
1. [Most important task]
2. [Second priority]
3. [Third priority]

WEATHER: [if relevant]
```

## Automated Commands
```bash
gog calendar events primary --today
gog gmail search "is:unread newer_than:1d"
```
