# PairSync Support Site - Deployment Guide

**Status:** Phase 1 MVP - Ready for GitHub Pages deployment  
**Purpose:** Instructions for deploying to GitHub Pages for Apple App Store submission  
**Created:** March 4, 2026

---

## Phase 1 MVP - Files Completed ✅

### Core Files
- [x] `_config.yml` - Jekyll configuration
- [x] `.gitignore` - Git ignore rules
- [x] `robots.txt` - Search engine indexing
- [x] `README.md` - Homepage (comprehensive)

### Getting Started
- [x] `getting-started/what-is-pairsync.md` - Complete overview

### Legal (CRITICAL for Apple)
- [x] `legal/terms-of-service.md` - Complete Terms of Service
- [x] `legal/privacy-policy.md` - Complete Privacy Policy
- [x] `legal/disclaimers.md` - Complete general disclaimers
- [x] `legal/risk-disclosure.md` - Detailed risk disclosure

### Support
- [x] `support/contact-us.md` - Contact information
- [x] `support/report-bug.md` - Bug reporting
- [x] `support/feature-request.md` - Feature requests

**Total Files:** 11 markdown files + 3 config files = **14 files**  
**Total Content:** ~40,000 words

---

## Deployment Steps

### Step 1: Initialize Git Repository

```powershell
# Navigate to the PairSync-Pro directory
cd C:\Dev\pairsync\PairSync-Pro

# Initialize git repository
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit - Phase 1 MVP Support Site"
```

### Step 2: Create GitHub Repository

**Option A: Via GitHub Web Interface**
1. Go to https://github.com/new
2. Repository name: `PairSync-Pro`
3. Description: "Official support and documentation for PairSync mobile app"
4. Visibility: **Public** (required for GitHub Pages)
5. Do NOT initialize with README (we already have one)
6. Click "Create repository"

**Option B: Via GitHub CLI** (if installed)
```powershell
gh repo create PairSync-Pro --public --source=. --remote=origin --description "Official support and documentation for PairSync mobile app"
```

### Step 3: Push to GitHub

```powershell
# Add remote (replace 'markm0705' with your GitHub username)
git remote add origin https://github.com/markm0705/PairSync-Pro.git

# Push to main branch
git branch -M main
git push -u origin main
```

**Authentication:**
- Use your GitHub Personal Access Token when prompted
- Ensure the token has `repo` permissions

### Step 4: Enable GitHub Pages

1. Go to repository: https://github.com/markm0705/PairSync-Pro
2. Click **Settings** (top right)
3. Scroll to **Pages** (left sidebar)
4. Under "Source":
   - Select branch: `main`
   - Select folder: `/ (root)`
5. Click **Save**
6. Wait 2-5 minutes for deployment

### Step 5: Verify Deployment

**Your site will be live at:**
```
https://markm0705.github.io/PairSync-Pro/
```

**Test these URLs:**
- Homepage: https://markm0705.github.io/PairSync-Pro/
- What is PairSync: https://markm0705.github.io/PairSync-Pro/getting-started/what-is-pairsync
- Terms: https://markm0705.github.io/PairSync-Pro/legal/terms-of-service
- Privacy: https://markm0705.github.io/PairSync-Pro/legal/privacy-policy
- Contact: https://markm0705.github.io/PairSync-Pro/support/contact-us

**All should load within 2-3 minutes of enabling GitHub Pages.**

---

## Step 6: Submit to Apple App Store Connect

1. Log in to App Store Connect: https://appstoreconnect.apple.com
2. Navigate to your PairSync app
3. Go to **App Information**
4. Find **Support URL** field
5. Enter: `https://markm0705.github.io/PairSync-Pro/`
6. Click **Save**

**That's it! Your support URL is now live and ready for Apple review.**

---

## Optional Enhancements (Post-MVP)

### Custom Domain (Later)

If you want `support.pair-sync.com` instead of GitHub subdomain:

1. Add `CNAME` file to repository:
```
support.pair-sync.com
```

2. Configure DNS with your domain registrar:
```
Type: CNAME
Name: support
Value: markm0705.github.io
```

3. In GitHub Pages settings, add custom domain: `support.pair-sync.com`

4. Enable "Enforce HTTPS"

### Analytics (Optional)

Add Google Analytics to track site visitors:

1. Get Google Analytics ID (e.g., G-XXXXXXXXXX)
2. Add to `_config.yml`:
```yaml
google_analytics: G-XXXXXXXXXX
```

3. Jekyll theme will auto-add tracking code

### Search (Future)

For site search functionality:
- Option 1: Algolia DocSearch (free for open source docs)
- Option 2: Lunr.js (client-side search)
- Option 3: Google Custom Search

---

## Maintenance & Updates

### Making Changes

**To update content:**

```powershell
# Navigate to repo
cd C:\Dev\pairsync\PairSync-Pro

# Make your edits to markdown files
# (use VS Code or any text editor)

# Commit changes
git add .
git commit -m "Update [description of what you changed]"

# Push to GitHub
git push origin main

# GitHub Pages will auto-rebuild (takes 1-2 minutes)
```

### Adding New Pages

1. Create new `.md` file in appropriate folder
2. Add frontmatter:
```yaml
---
title: Page Title
description: Page description for SEO
---
```
3. Write content in Markdown
4. Commit and push
5. Link from other pages

---

## Troubleshooting

### Site not loading after 10 minutes
- Check GitHub Actions tab for build errors
- Verify Pages is enabled in Settings
- Clear browser cache and try incognito mode

### 404 errors on pages
- Check file paths (case-sensitive on Linux servers)
- Verify all links use relative paths
- Ensure files have `.md` extension (not `.markdown`)

### Links not working
- GitHub Pages auto-converts `.md` to `.html`
- Links can omit `.md` extension (will still work)
- Use relative links (e.g., `../legal/terms-of-service`)

### Styling looks wrong
- Check `_config.yml` syntax (YAML is whitespace-sensitive)
- Try different Jekyll theme (e.g., `theme: jekyll-theme-cayman`)
- View source to see if CSS is loading

---

## Phase 2 & 3 Content (Future)

**Once Apple approves, continue building:**

### Phase 2 - Core Documentation (1 week)
- Complete all Getting Started guides (installation, first-login, etc.)
- Complete all Features documentation
- Add screenshots and diagrams

### Phase 3 - Educational Content (ongoing)
- Build out Education section
- Add Troubleshooting guides
- Expand FAQ sections

---

## Pre-Deployment Checklist

**Before submitting to Apple, verify:**

- [ ] All legal pages load correctly
- [ ] Contact email (mark@pair-sync.com) is correct
- [ ] Phone number (+61 408 881 692) is correct
- [ ] Apple reviewer test account credentials are visible on homepage
- [ ] All internal links work (no 404s)
- [ ] Site loads on mobile (test on iPhone)
- [ ] No placeholder text (all "TODO" items completed for Phase 1)
- [ ] HTTPS enabled (GitHub Pages provides free SSL)

---

## Success Metrics

**How to know if successful:**

✅ Site loads in < 2 seconds  
✅ All Phase 1 URLs return 200 OK  
✅ Mobile-responsive (test on actual iPhone)  
✅ Apple reviewer can find contact info in < 30 seconds  
✅ Legal pages are comprehensive and clear  
✅ **Apple app approval within 7 days** 🎉

---

## Contact for Deployment Help

**If you encounter issues:**

**Email:** mark@pair-sync.com  
**Subject:** "GitHub Pages Deployment Issue"

**Or:**
- GitHub Pages docs: https://docs.github.com/en/pages
- Jekyll docs: https://jekyllrb.com/docs/

---

## Post-Deployment Actions

**After site is live:**

1. ✅ Test all URLs manually
2. ✅ Submit support URL to App Store Connect
3. ✅ Build iOS binary with updated App Store listing
4. ✅ Submit app for review
5. ⏳ Wait for Apple approval (typically 1-7 days)
6. 🎉 Celebrate when approved!
7. 📝 Begin Phase 2 content (if time permits)

---

## Version History

**v1.0 - March 4, 2026**
- Initial Phase 1 MVP
- 11 content files
- Ready for Apple submission

---

**Deployment prepared by:** AI Assistant  
**Final review needed by:** PairSync team  
**Ready to deploy:** YES ✅

---

**Next command to run:**

```powershell
cd C:\Dev\pairsync\PairSync-Pro
git init
git add .
git commit -m "Initial commit - Phase 1 MVP"
```

Then follow steps 2-6 above.

**Good luck with your App Store submission! 🚀**
