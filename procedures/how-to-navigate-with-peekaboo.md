# How to Navigate macOS UI with Peekaboo

**Last verified:** 2026-02-07
**Tools required:** peekaboo (bundled skill), exec
**Estimated time:** Varies

## Core Commands

### 1. See What's on Screen
```bash
# Full screen capture
peekaboo capture screen

# Specific window
peekaboo capture window --app "Safari"

# List all windows
peekaboo list windows
```

### 2. Find UI Elements
```bash
# Get accessibility tree for an app
peekaboo inspect --app "Safari"

# Find a specific element
peekaboo find --text "Submit" --app "Safari"
```

### 3. Interact with UI
```bash
# Click at coordinates
peekaboo click --x 500 --y 300

# Click a specific element
peekaboo click --element "Submit Button"

# Type text
peekaboo type "Hello world"

# Keyboard shortcut
peekaboo hotkey --keys "cmd+t"  # New tab

# Scroll
peekaboo scroll --direction down --amount 3
```

### 4. App Control
```bash
# Open an app
peekaboo open --app "Safari"

# Focus a window
peekaboo focus --app "Safari"

# Close a window
peekaboo hotkey --keys "cmd+w"
```

## Perception-Action Loop

For any UI task, follow this pattern:

1. **Capture** → Take a screenshot to understand current state
2. **Analyze** → Send screenshot to vision model (Claude Sonnet) to understand what's visible
3. **Plan** → Decide what action to take based on what's visible
4. **Act** → Execute the action via Peekaboo
5. **Verify** → Take another screenshot to confirm the action worked
6. **Retry** → If verification fails, adjust and try again (max 3 retries)

## Common App Coordinates (update as discovered)

Track commonly-used UI element positions in TOOLS.md to speed up future interactions.

## Common Failures

- **Element not found** → App might not be in focus. Run `peekaboo focus --app "AppName"` first
- **Wrong coordinates** → Window may have moved. Always capture first, then act
- **Permission denied** → macOS accessibility permissions needed. System Preferences → Privacy → Accessibility → enable OpenClaw
- **App not running** → Use `peekaboo open --app "AppName"` to launch first

## Best Practices

- Always capture before acting (never assume screen state)
- Use accessibility tree (`inspect`) over coordinates when possible
- Coordinates are fragile — save them to TOOLS.md but verify each session
- AppleScript is preferred over Peekaboo for apps that support it (more reliable)
