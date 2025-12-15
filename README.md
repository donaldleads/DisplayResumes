# Production Resume Gallery Setup

## Files Overview

### 1. HTML Embed Code
**File:** `resume-embed-prod.html`
**Location on site:** donaldleads.com/#resumes
**Purpose:** Main production resume gallery with request form

### 2. GitHub JSON File
**File:** `resumes.json` (already exists in your repo)
**URL:** https://raw.githubusercontent.com/donaldleads/DisplayResumes/main/resumes.json
**Purpose:** Contains all production resumes data

## Key Differences from Dev Version

| Aspect | Dev Version | Prod Version |
|--------|-------------|--------------|
| HTML IDs | All have `-dev` suffix | No suffix (e.g., `resume-app`, `filters`) |
| Site Location | #resumesdev | #resumes |
| JSON Source | Same file (resumes.json) | Same file (resumes.json) |
| Webhook URL | Same (both use production flow) | Same |

## Important Notes

⚠️ **Both dev and prod currently use the SAME resumes.json file**

This means:
- Changes to resumes.json appear on BOTH dev and prod pages
- You're currently using #resumesdev for testing
- When ready to go live, you'll use #resumes with this prod code

## Going Live Checklist

1. ✅ Test the dev version thoroughly at #resumesdev
2. ✅ Verify all resumes display correctly
3. ✅ Test the request form submission
4. ✅ Confirm emails are sent correctly
5. ⬜ When ready: Paste `resume-embed-prod.html` into Carrd embed at #resumes
6. ⬜ Test production page
7. ⬜ Update any links pointing to the resume gallery

## Future Consideration: Separate Dev/Prod JSON Files

If you want completely separate dev and prod environments in the future, you could:

1. Create `resumes-dev.json` in GitHub
2. Update dev version to point to `resumes-dev.json`
3. Keep `resumes.json` for production only
4. Test changes in dev, then promote to prod when ready

For now, using one file for both is simpler and fine for your use case.
