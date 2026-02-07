# How to Check Email

**Last verified:** 2026-02-07
**Tools required:** exec (gog CLI), web fetch (fallback)
**Estimated time:** 1-2 minutes

## Steps

1. Check unread emails from the last 24 hours:
   ```bash
   gog gmail search "is:unread newer_than:1d" --max 20
   ```

2. For each unread email, assess priority:
   - **URGENT**: From professors, law school admin, Maddie, Hey Spotless clients
   - **IMPORTANT**: Assignment-related, deadline mentions, interview follow-ups
   - **NORMAL**: Everything else
   - **SKIP**: Newsletters, promotions, automated notifications

3. If urgent emails found, summarize and send to Matt via WhatsApp immediately

4. Log the check in `memory/heartbeat-state.json`:
   ```json
   { "lastChecks": { "email": <unix_timestamp> } }
   ```

5. Update today's memory file with any significant emails

## Email Accounts

- **Primary:** MatthewRufca@gmail.com (via gog CLI)
- **School:** Matthew.Rufca@faulkner.edu (check via web if accessible)

## Common Failures

- **gog not found** → Run `which gog` to verify installation, check PATH
- **Auth expired** → Run `gog auth login` to re-authenticate
- **Rate limited** → Wait 5 minutes, retry

## Priority Keywords

Scan subject lines for: "due", "deadline", "urgent", "ASAP", "grade", "assignment", "exam", "interview", "payment", "invoice"
