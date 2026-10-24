# Fleet Video Analysis Portal — Deployment Package

## Where to Publish (Free Options)

### Option 1: GitHub Pages (Recommended — Simplest)
**Cost**: Free  
**Access**: Public URL `https://yourusername.github.io/fleet-analysis-site/`  
**Steps**:
1. Create account at https://github.com (free)
2. Create new repo named `fleet-analysis-site`
3. Upload all files from this folder (`*.html`, `data/`, `assets/`, `reports/`)
4. Go to repo → Settings → Pages → Source: "Deploy from branch" → `main`
5. URL becomes public instantly (usually within 2 minutes)

### Option 2: Netlify Drop (Drag & Drop — No Account Needed)
**Cost**: Free  
**Access**: `https://fleet-analysis-site-xyz.netlify.app/`  
**Steps**:
1. Go to https://app.netlify.com/drop
2. Drag and drop this entire folder into the drop zone
3. Netlify generates a public URL instantly
4. Optionally claim with free account for custom domain

### Option 3: Microsoft Azure Static Web Apps / Cloudflare Pages
**Cost**: Free tier  
Both allow drag-and-drop or GitHub connection with same result.

---

## What This Package Contains
- `index.html` — Main portal with top-10 risk table (24-hour ADAS/DMS analysis)
- `reports/` — Individual vehicle analysis reports (100 most recent clips, week bad-camera report)
- `assets/images/` — Representative original-resolution frames
- `data/` — Structured JSON analysis outputs (optional for interactivity)

## Verification Before Deploy
- [ ] All 100 rows present in `reports/recent100/summary.md`
- [ ] Every embedded image resolves (check `typical_frame` references)
- [ ] Vehicle mapping consistent with `mapping.json` (device code = vehicle ID)
- [ ] No hardcoded counts in verification scripts (all derived from TSV)
- [ ] All checks pass (run `verify_publish.py` + `fault_test.py` if available)

---
*Generated from verified dashcam-analysis output. All percentages audited; false positives (e.g., 55% FCW withdrawn on 096895479219) corrected.*
