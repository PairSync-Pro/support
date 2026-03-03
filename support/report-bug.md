---
title: Report a Bug
description: Help us fix issues by reporting bugs in PairSync
---

# Report a Bug

Found something that's not working right? We want to know! Bug reports help us improve PairSync for everyone.

---

## How to Report a Bug

**Email:** mark@pair-sync.com  
**Subject:** "Bug Report: [Brief Description]"

Example: "Bug Report: App crashes when opening pair details"

---

## Bug Report Template

**Please copy and complete this template:**

```
BUG REPORT

1. SUMMARY
Brief description of the issue (1-2 sentences):


2. DEVICE INFORMATION
- Device Model: (e.g., iPhone 14 Pro)
- iOS Version: (e.g., iOS 17.4)
- App Version: (find in Settings → About)
- Network: WiFi or Cellular?


3. STEPS TO REPRODUCE
How can we recreate the bug?
1. Open the app
2. Navigate to...
3. Tap on...
4. Issue occurs


4. EXPECTED BEHAVIOR
What should have happened?


5. ACTUAL BEHAVIOR
What actually happened instead?


6. FREQUENCY
- Does this happen every time? □ Yes □ No
- If not, how often? (e.g., 3 out of 5 times)


7. SCREENSHOTS / SCREEN RECORDING
(Attach if possible - very helpful!)


8. ERROR MESSAGES
If an error message appeared, what did it say exactly?


9. ADDITIONAL CONTEXT
Any other details that might be relevant?


10. YOUR ACCOUNT EMAIL
(So we can investigate your specific data if needed)
```

---

## Priority Levels

We prioritize bugs based on severity:

### 🔴 Critical (P0) - Immediate Response
- App crashes on launch (unusable)
- Data loss or corruption
- Security vulnerabilities
- Login completely broken
- Payment/subscription system failure

**Expected Fix Time:** 24-72 hours (emergency patch)

---

### 🟠 High Priority (P1) - Fast Response
- Major feature broken (e.g., watchlists don't save)
- Incorrect data displayed (e.g., wrong Z-scores)
- Performance issues making app unusable (extreme lag)
- Subscription not recognized after payment

**Expected Fix Time:** 1-2 weeks (next app update)

---

### 🟡 Medium Priority (P2) - Normal Response
- Minor feature issues (e.g., button doesn't respond sometimes)
- Visual glitches (e.g., text overlap)
- Inconsistent behavior (works sometimes, fails others)
- Non-critical data issues

**Expected Fix Time:** 2-4 weeks (regular update cycle)

---

### 🟢 Low Priority (P3) - Tracked for Future
- Cosmetic issues (e.g., minor alignment problems)
- Typos or text issues
- Nice-to-have improvements
- Edge case scenarios

**Expected Fix Time:** Next major version (months)

---

## What Happens After You Report

1. **Acknowledgment (24-48 hours)**  
   We'll confirm we received your report and ask for any clarifying details.

2. **Investigation**  
   Our team will try to reproduce the issue and investigate the root cause.

3. **Priority Assignment**  
   We'll categorize the bug by severity and prioritize accordingly.

4. **Fix & Testing**  
   Engineers will fix the bug and test thoroughly.

5. **Release**  
   The fix will be included in the next app update (timeline depends on priority).

6. **Notification**  
   We'll email you when the fix is released (if you requested updates).

---

## Tips for Great Bug Reports

**DO:**
- ✅ Be specific and detailed
- ✅ Include steps to reproduce
- ✅ Attach screenshots or screen recordings
- ✅ Mention if it worked before (and when it broke)
- ✅ Test on latest app version before reporting

**DON'T:**
- ❌ Just say "It's broken" without details
- ❌ Report multiple unrelated bugs in one email (separate reports for each)
- ❌ Include sensitive personal info in screenshots (like account balances if you're also using a broker app)

---

## Example of a Good Bug Report

**Subject:** Bug Report: Trade Journal filter by sector not working

**Body:**
```
SUMMARY:
When I try to filter the Trade Journal by sector, the filter doesn't apply and all trades still show.

DEVICE INFO:
- iPhone 13
- iOS 17.2
- PairSync App Version 1.2.5
- WiFi connection

STEPS TO REPRODUCE:
1. Open app and navigate to Trade Journal tab
2. Tap the filter icon (top right)
3. Select "Technology" sector
4. Tap "Apply"
5. Trade Journal still shows all sectors, not just Technology

EXPECTED BEHAVIOR:
Should only show trades from Technology sector pairs.

ACTUAL BEHAVIOR:
All trades from all sectors continue to display.

FREQUENCY:
Happens every time I try to filter by sector (tested 5 times).

SCREENSHOTS:
[Attached: before-filter.png, after-filter.png showing no change]

ERROR MESSAGES:
No error message displayed.

ADDITIONAL CONTEXT:
- Filtering by asset class (Stocks vs Crypto) works fine
- Search by symbol also works
- Only sector filter is broken
- Started happening after yesterday's app update

ACCOUNT EMAIL:
user@example.com
```

**This is perfect!** Clear, detailed, reproducible.

---

## Common Issues & Quick Fixes

Before reporting, try these quick fixes:

### App won't open / keeps crashing
1. Force quit the app (swipe up from app switcher)
2. Restart your iPhone
3. Check for iOS updates (Settings → General → Software Update)
4. Check for PairSync app updates (App Store)
5. Reinstall the app (delete, then re-download)

### Data not loading
1. Check internet connection
2. Pull down to refresh manually
3. Force quit and reopen app
4. Check if market is closed (data updates daily after close)

### Can't log in
1. Verify email and password carefully (case-sensitive)
2. Try "Forgot Password" to reset
3. Check email spam folder for verification email
4. Clear app cache (reinstall if needed)

### Subscription not recognized
1. Tap "Restore Purchases" in Subscription tab
2. Wait 30 seconds (backend sync may be delayed)
3. Restart app
4. Contact support if still not working

**If quick fixes don't work, please report the bug!**

---

## Known Issues

**Current known issues we're working on:**

(This section will be updated as we discover and track issues)

- Example: "Push notifications delayed by 5-10 minutes (investigating)"
- Example: "Indian market pairs not loading (fix coming in v1.2.6)"

Check back here to see if your issue is already known and being addressed.

---

## Feature Requests vs Bugs

**Bug:** Something that's supposed to work but doesn't  
**Feature Request:** Something new you'd like added

**Examples:**

**Bug:**  
"The Z-Score Calculator gives wrong results when I enter negative numbers"  
→ Should work, doesn't work = bug

**Feature Request:**  
"Add a Z-Score history chart to see how Z-Score changed over time"  
→ New functionality = feature request

**For feature requests:** [Click here →](feature-request.md)

---

## Security Vulnerabilities

**If you found a security issue (data leaks, unauthorized access, etc.), DO NOT post publicly.**

**Email:** mark@pair-sync.com  
**Subject:** "SECURITY VULNERABILITY - [Brief Description]"

We'll respond within 48 hours and work with you to resolve it responsibly.

[Learn more about responsible disclosure →](contact-us.md#security-vulnerabilities)

---

## Beta Testing Program

**Want to help test new features before release?**

We're building a beta testing program where users can:
- Try upcoming features early
- Report bugs before they reach production
- Influence feature design

**Interested?** Email mark@pair-sync.com with "Beta Tester Interest" in subject.

---

## Thank You for Helping!

Every bug report makes PairSync better for thousands of users. We genuinely appreciate you taking the time to report issues.

**Bug bounty program?** We're considering offering free subscription months for critical bug discoveries. Stay tuned!

---

**Contact:** mark@pair-sync.com  
**Related:** [Contact Support](contact-us.md) | [Feature Requests](feature-request.md)

*Last Updated: March 4, 2026*
