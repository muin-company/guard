# MUIN Guard Deployment Status

## ✅ Completed Steps

### 1. Repository Setup
- **GitHub Repository:** https://github.com/muin-company/guard
- **Local Path:** /Users/mj/github/guard
- **Branch:** main
- **Status:** Active and pushed

### 2. Landing Page
- **File:** index.html
- **Design:** Dark theme matching muin.company
- **Font:** Inter (via Google Fonts)
- **Accent Color:** #10b981 (green)
- **Features:**
  - Hero section with "MUIN Guard" title
  - Status badge: "Pending Chrome Web Store Review" (amber dot)
  - Email signup form (Formspree integration)
  - 4 feature cards (Suspicious Prompt Detection, Data Protection, Real-Time Alerts, Privacy First)
  - GitHub CTA section
  - Footer matching muin.company style
- **Mobile Responsive:** Yes
- **Dependencies:** None (single HTML file)

### 3. GitHub Pages
- **Enabled:** ✅
- **Source:** main branch, root directory
- **Custom Domain:** guard.muin.company (via CNAME file)
- **HTTPS:** Will be enforced after DNS propagation
- **URL:** https://github.com/muin-company/guard (temp: http://guard.muin.company/)

### 4. Documentation
- **README.md:** Project overview and links
- **DNS Setup Guide:** ~/muin/docs/guard-dns-setup.md
- **CNAME File:** guard.muin.company

## ⏳ Pending Steps (Requires ONE)

### DNS Configuration
DNS records need to be added to point guard.muin.company to GitHub Pages.

**Required A Records:**
```
guard.muin.company → 185.199.108.153
guard.muin.company → 185.199.109.153
guard.muin.company → 185.199.110.153
guard.muin.company → 185.199.111.153
```

**Optional AAAA Records (IPv6):**
```
guard.muin.company → 2606:50c0:8000::153
guard.muin.company → 2606:50c0:8001::153
guard.muin.company → 2606:50c0:8002::153
guard.muin.company → 2606:50c0:8003::153
```

See full instructions: `~/muin/docs/guard-dns-setup.md`

### Post-DNS Steps
1. Wait for DNS propagation (5-60 minutes)
2. Verify DNS: `dig guard.muin.company`
3. Enable HTTPS in GitHub Pages settings (after certificate provision)
4. Test: https://guard.muin.company

## Extension Details
- **Name:** MUIN Guard
- **Extension ID:** ogcbbgplejkkfbaionhljljdcbbafkkj
- **Status:** Pending Chrome Web Store Review
- **Privacy:** All monitoring happens locally in browser

## Email Signup
- **Provider:** Formspree
- **Endpoint:** https://formspree.io/f/xpwzgkvq (same as main MUIN site)
- **Hidden Field:** product=MUIN Guard (to differentiate from main site signups)

## Design Compliance
✅ Matches muin.company exactly
✅ Dark theme (#0a0a0a background)
✅ Inter font
✅ Green accent (#10b981)
✅ No AI vibes (per docs/style-guide.md)
✅ Mobile responsive
✅ Single page, no dependencies

## Links
- **Landing Page:** https://guard.muin.company (pending DNS)
- **GitHub:** https://github.com/muin-company/guard
- **Parent Site:** https://muin.company
- **Blog:** https://blog.muin.company

---

**Created:** 2026-02-06
**Last Updated:** 2026-02-06
**Status:** Ready for DNS configuration
