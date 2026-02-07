# How to Use the Perception-Action Loop

**Last verified:** 2026-02-07
**Tools required:** peekaboo, Claude vision (haiku or sonnet), exec
**Estimated time:** Varies per task

## What Is It

The perception loop lets Tiro "see" the screen and act on what's visible — like a human looking at a monitor and clicking/typing. It bridges the gap between text-only reasoning and visual GUI control.

## The Loop

```
1. CAPTURE  → Take a screenshot
2. ANALYZE  → Send to vision model to understand what's visible
3. DECIDE   → Determine what action to take
4. ACT      → Execute via Peekaboo or AppleScript
5. VERIFY   → Capture again to confirm action worked
6. RETRY    → If verification fails, adjust and try again (max 3)
```

## Step 1: Capture

```bash
# Full screen
peekaboo capture screen

# Specific app window
peekaboo capture window --app "Safari"

# Specific region (x, y, width, height)
peekaboo capture region --x 0 --y 0 --w 800 --h 600
```

## Step 2: Analyze

Send the captured image to a vision-capable model. Claude Haiku 4-5 and Sonnet 4-5 both support image input.

When analyzing, ask specific questions:
- "What app is visible? What page/screen is shown?"
- "Where is the [button/field/link] I need to click?"
- "Is there an error message visible?"
- "What text is shown in [specific area]?"

## Step 3: Decide

Based on the visual analysis:
- Identify the target UI element
- Determine the action (click, type, scroll, hotkey)
- Plan the coordinates or accessibility path

## Step 4: Act

```bash
# Click at coordinates
peekaboo click --x 500 --y 300

# Type text (into focused field)
peekaboo type "search query"

# Keyboard shortcut
peekaboo hotkey --keys "cmd+l"  # Focus address bar

# Scroll
peekaboo scroll --direction down --amount 5
```

## Step 5: Verify

Take another screenshot and check:
- Did the expected change happen?
- Is the correct page/screen showing?
- Any error messages?

## Step 6: Retry

If verification fails:
1. Analyze what went wrong
2. Adjust coordinates or approach
3. Try again (max 3 attempts)
4. If still failing, alert Matt and write a retrospective

## When to Use Perception Loop vs Other Tools

| Situation | Best Tool |
|-----------|-----------|
| App has AppleScript support | AppleScript (more reliable) |
| Web page interaction | Browser tool (CSS selectors) |
| App has no API/scripting | Peekaboo perception loop |
| Need to read visual content | Peekaboo + vision model |
| Need to understand screen context | Peekaboo capture → vision |

## Common Patterns

### Opening an app and navigating
1. `osascript scripts/open-app.applescript "AppName"` (or `peekaboo open`)
2. Wait 2 seconds for app to load
3. Capture screen to verify app is open
4. Navigate using hotkeys or clicks

### Filling out a form
1. Capture the form to identify all fields
2. Click first field
3. Type value
4. Tab to next field (or click it)
5. Repeat until form is complete
6. Capture to verify before submitting

### Reading information from screen
1. Capture the relevant window
2. Send to vision model with specific extraction prompt
3. Parse the model's response
4. Store extracted data in memory files

## Safety

- Never submit financial/legal forms without Matt's approval
- Always verify before clicking "Send", "Submit", "Delete", "Confirm"
- If unsure what a button does, ask Matt
- Log all significant UI actions in today's memory file
