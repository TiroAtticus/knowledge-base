# Config Validation: String vs Number Types - 2026-02-07

## What Happened
After modifying `openclaw.json` to add compaction settings and browser config, the gateway refused to start. Error: `Config validation failed: maxTokens: Invalid input: expected number, received string`.

## Root Cause
A Node.js script that modified the JSON config accidentally converted numeric values to strings. JSON.parse/stringify preserved them, but the intermediate manipulation introduced string types where numbers were expected.

## Impact
- Gateway was down for ~10 minutes
- No messages could be sent/received during downtime
- Required manual intervention to fix

## Fix Applied
Ran a targeted Node.js script to `parseInt()` all `maxTokens` fields across all model providers and the `softThresholdTokens` compaction field.

## Prevention
When writing Node.js scripts that modify openclaw.json:
1. **Always validate types after modification** — check that numbers are `typeof === 'number'`
2. **Use explicit `Number()` casts** when setting numeric config values
3. **Run `openclaw doctor` after any config change** to validate before restarting
4. **Keep a backup**: `cp openclaw.json openclaw.json.bak` before any modification

## Procedure Updated?
- [x] This retrospective documents the pattern
- [x] Future config modification scripts should include type validation
- [ ] Could add a pre-restart config validation step to procedures
