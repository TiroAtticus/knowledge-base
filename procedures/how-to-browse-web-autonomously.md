# How to Browse the Web Autonomously

**Last verified:** 2026-02-07
**Tools required:** browser tool, exec (fallback)
**Estimated time:** Varies

## Browser Profiles

- **`openclaw`** (default) — Dedicated browser profile for Tiro. Use for autonomous browsing. Doesn't interfere with Matt's Chrome sessions.
- **`chrome`** — Matt's actual Chrome. Use Chrome extension relay to control existing tabs. Good for interacting with sites where Matt is already logged in.

## Basic Navigation

### Open a URL
```
browser.navigate({ url: "https://example.com" })
```

### Take a Screenshot
```
browser.screenshot()
```

### Get Page Content (DOM snapshot)
```
browser.snapshot()
```

### Click an Element
```
browser.click({ selector: "#submit-button" })
browser.click({ text: "Sign In" })
browser.click({ x: 500, y: 300 })
```

### Type into a Field
```
browser.click({ selector: "#email-field" })
browser.type({ text: "MatthewRufca@gmail.com" })
```

### Scroll
```
browser.scroll({ direction: "down", amount: 500 })
```

## Workflow: Check Canvas for Assignments

1. Navigate to Canvas login page
2. Screenshot to verify page loaded
3. Check if already logged in (look for dashboard)
4. If not logged in: use stored credentials or alert Matt
5. Navigate to assignments/calendar
6. Snapshot the page to extract assignment data
7. Parse deadlines and update MEMORY.md

## Workflow: Check Housecall Pro Dashboard

1. Navigate to Housecall Pro
2. Screenshot the dashboard
3. Extract today's scheduled jobs
4. Note any new bookings or messages
5. Summarize for Matt in morning briefing

## Session Management

- The `openclaw` browser profile persists cookies between sessions
- If a site requires re-authentication, alert Matt via WhatsApp
- Store login status in `memory/heartbeat-state.json`

## Common Failures

- **Page not loaded** → Wait 2-3 seconds, retry screenshot
- **Login required** → Send Matt a WhatsApp asking for credentials or approval
- **Captcha** → Cannot solve. Alert Matt.
- **Timeout** → Increase wait time, check internet connectivity

## Security Rules

- NEVER store plaintext passwords in workspace files
- Use the browser profile's cookie storage for sessions
- Alert Matt before logging into any new service
- Don't submit forms with financial/legal impact without approval
