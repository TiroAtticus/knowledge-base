# Canvas Course Access - Feb 7, 2026

## Courses Enrolled

1. **Contracts** (LAW 6311)
2. **Legal Analysis & Persuasion** (LAW 6211)
3. **Civil Procedure II** (LAW 6212)
4. **American Constitutional Order** (LAW 6313)
5. **Property** (LAW 6310)

## Access Method

- **URL:** https://faulkner.instructure.com/
- **Authentication:** Microsoft SSO (matthew.rufca@faulkner.edu)
- **Browser:** OpenClaw autonomous browsing

## Important Rules

✅ **ALLOWED:**
- View assignments
- Check due dates
- Read course materials
- Pull syllabi
- Extract deadlines

❌ **PROHIBITED:**
- Submit assignments
- Post comments
- Send messages
- Upload content
- Any visible changes

## Automation Strategy

**Morning Routine:**
1. Navigate to Canvas dashboard
2. Check calendar view for due dates
3. Extract assignments from next 7 days
4. Compare with calendar events
5. Include in morning briefing

**Code Pattern:**
```python
def check_canvas_assignments():
    browser.navigate("https://faulkner.instructure.com/calendar")
    screenshot()
    extract_text(".assignment")
    parse_due_dates()
    return upcoming_assignments
```

## Next Steps

1. ✅ Courses identified
2. ⏳ Extract all upcoming due dates
3. ⏳ Create automated morning check
4. ⏳ Track deadline completion

---

*Last updated: Feb 7, 2026*
*Status: Access confirmed, automation in progress*
