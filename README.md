# Resume Display Embed Code

This repository contains the embed code for the resume display feature on donaldleads.com.

## File Structure

- `resume-embed-dev.html` - Development version (uses `-dev` suffix IDs)
- `resume-embed-prod.html` - Production version (standard IDs)
- `resumes.json` - Resume data

## Workflow

### Making Changes

1. **Edit `resume-embed-dev.html`** - Make all changes here first
2. **Test on your site** - Paste into the `#resumesdev` section in Carrd
3. **Verify it works** - Check functionality, styling, filters, etc.

### Promoting to Production

When your dev version is tested and ready:

1. **Copy `resume-embed-dev.html`** to a text editor
2. **Find and Replace** the following:
   - `resume-app-dev` → `resume-app`
   - `filters-dev` → `filters`
   - `resume-list-dev` → `resume-list`
   - `specialty-filters-dev` → `specialty-filters`
   - `supported-filters-dev` → `supported-filters`
3. **Save as `resume-embed-prod.html`**
4. **Commit both files** to GitHub
5. **Paste prod version** into `#resumes` section in Carrd

## Key Differences Between Dev and Prod

The ONLY differences between dev and prod versions are the element IDs:
- Dev uses `-dev` suffix to avoid conflicts when both are on the same page
- Prod uses standard IDs

## Important Notes

- Both versions pull from the same `resumes.json` data file
- Keep both files in sync (content-wise), only IDs should differ
- Always test in dev before pushing to prod
- Carrd.co strips indentation, so don't worry about formatting

## Version History

Track your changes here:

### 2025-12-06
- Initial setup with dev/prod split
- Fixed querySelectorAll syntax bug
- Changed header from "Profile #X" to "Profile: Name"
- Removed redundant Name field
- Moved reset icon to left of category labels

---

*Maintained by donaldleads*
