# Living Manna Privacy Policy & Support Pages Redesign Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build world-class, clean, Apple-inspired Privacy Policy and Support pages for Living Manna that fulfill Apple App Store and Google Play Store requirements and strictly list only production Bible versions (KJV, Amharic 1954, ERV, NASV).

**Architecture:** Standalone, dependency-free vanilla HTML5 + CSS with embedded responsive Apple-style design tokens, adaptive light/dark mode support, clean SVG iconography, and semantic structure across `privacy-policy.html`, `support.html`, and `index.html`.

**Tech Stack:** Semantic HTML5, Vanilla CSS3 (CSS Custom Properties, Flexbox, CSS Grid, media queries for `prefers-color-scheme`), zero external runtime dependencies.

## Global Constraints
- Target bundle IDs: `com.livingmanna.livingManna` (iOS App Store) and `com.livingmanna.livingmanna` (Google Play Store).
- Contact email: `tesfayegirma360@gmail.com`.
- Only production Bible translations from `.env.production` are to be listed: King James Version (KJV), Amharic 1954 (የድሮ ትርጉም), Easy-to-Read Version™ (ERV), New Amharic Standard Version™ (NASV / አማ01 / አዲሱ መደበኛ ትርጕም). Disabled versions (`ENABLE_AMP`, `ENABLE_NLT`, `ENABLE_NST`) must NOT appear.
- 100% on-device privacy guarantee — zero analytics, zero trackers, zero ads, zero user accounts, zero remote telemetry.
- Seamless responsive design across mobile, tablet, and desktop with automatic light/dark mode adaptation.

---

### Task 1: Create Apple-Style Shared Design System & Structure for `privacy-policy.html`

**Files:**
- Modify: `pages/privacy-policy.html`

**Interfaces:**
- Consumes: Production translations from `app/.env.production` and `app/lib/data/constants/bible_versions.dart`.
- Produces: Fully redesigned, Apple-inspired `privacy-policy.html` with clean typography, navigation header, summary nutrition cards, and legal sections.

- [ ] **Step 1: Write Apple-style CSS and HTML structure for `privacy-policy.html`**
Include:
  - Apple SF Pro / system font stack, high-contrast dark/light mode palette with CSS custom properties.
  - Sticky frosted header with Living Manna badge and navigation links (`Privacy Policy`, `Support`).
  - Hero header with Last Updated timestamp and "Privacy at a Glance" Apple-style nutrition labels (Data Used to Track You: None; Data Linked to You: None; 100% On-Device).
  - Explicit section on identity and store identifiers (`com.livingmanna.livingManna` and `com.livingmanna.livingmanna`).
  - Section on "Information We Do Not Collect" (no accounts, no telemetry, no tracking, no ads).
  - Section on "Information Stored On Your Device" (reading progress, bookmarks, notes, highlights, reading plans, reading stats, preferences).
  - Section on "Device Permissions" (iOS & Android notifications, photo library / storage for verse wallpapers, local alarms).
  - Section on "Data Export & Sharing" (user-initiated JSON backups and system share sheet).
  - Section on "Bible Translation Copyrights" strictly listing only production translations:
    - King James Version (KJV) — Public domain.
    - Amharic 1954 (የድሮ ትርጉም) — Bible Society of Ethiopia (`https://www.biblesociety.et`).
    - Easy-to-Read Version™ (ERV) — © 2006 Bible League International (`https://www.bibleleague.org`).
    - New Amharic Standard Version™ (NASV / አማ01) — © 2001, 2024 Biblica, Inc. (`https://www.biblica.com`).
  - Section on Children's Privacy (COPPA & GDPR-K compliant).
  - Section on Data Deletion & Security (100% local data control).
  - Section on Contact & Inquiries (`tesfayegirma360@gmail.com`).
  - Apple-style subtle footer.

- [ ] **Step 2: Verify `privacy-policy.html` syntax and content**
Verify that:
  - All tags are closed properly.
  - No references to AMP, NLT, or NST exist in the file.
  - All four production versions (KJV, Amharic 1954, ERV, NASV) are present with their exact copyright text.
  - Both iOS and Android store package IDs are documented.

- [ ] **Step 3: Commit `privacy-policy.html`**
```bash
git add pages/privacy-policy.html
git commit -m "feat: redesign privacy policy page with Apple-style UI and production translations"
```

---

### Task 2: Redesign `support.html` into a World-Class Apple-Style Support Hub

**Files:**
- Modify: `pages/support.html`

**Interfaces:**
- Consumes: Shared Apple-style styling tokens from Task 1.
- Produces: Modern, responsive Support Hub with categorized FAQ cards, widget troubleshooting, data transfer instructions, and direct support contact actions.

- [ ] **Step 1: Write Apple-style CSS and HTML structure for `support.html`**
Include:
  - Matching Apple-style design tokens, typography, and dark/light mode CSS.
  - Matching sticky header navigation linking to Privacy Policy and Support.
  - Support Hero with prominent direct email button (`tesfayegirma360@gmail.com`) and pre-filled subject template guidance.
  - Diagnostic checklist card for reporting issues (Device model, OS version, App build version from Settings).
  - Categorized FAQ cards with clean typography and icons:
    - **Offline Usage & Bible Downloads**: Details on bundled zero-network reading and search.
    - **Translations & Content**: Information on available production translations (KJV, Amharic 1954, ERV, NASV) and how to report translation errata.
    - **Data, Backups & Migration**: Step-by-step instructions on transferring notes, bookmarks, and reading plans to a new device using JSON backup/restore.
    - **Home Screen Widgets**: Clear troubleshooting guide for iOS WidgetKit and Android AppWidgets when daily verse updates lag.
  - Privacy commitment callout linking to `privacy-policy.html`.
  - Apple-style minimalist footer.

- [ ] **Step 2: Verify `support.html` syntax and content**
Verify that:
  - All links work correctly.
  - Support questions directly answer the key user concerns (widgets, backups, translation requests).
  - Navigation between `privacy-policy.html` and `support.html` is seamless.

- [ ] **Step 3: Commit `support.html`**
```bash
git add pages/support.html
git commit -m "feat: redesign support hub with Apple-style UI and comprehensive FAQ"
```

---

### Task 3: Update `index.html` as a Sleek Apple-Style Landing Hub

**Files:**
- Modify: `pages/index.html`

**Interfaces:**
- Consumes: Navigation structure for `privacy-policy.html` and `support.html`.
- Produces: Polished Apple-style entry portal that directs visitors to either the Privacy Policy or Support Hub, while maintaining fast canonical redirection.

- [ ] **Step 1: Write clean Apple-style landing in `index.html`**
Include:
  - Clean Living Manna logo / icon badge.
  - Clear cards linking to **Privacy Policy** and **Support Hub**.
  - Matching typography and auto light/dark theme styling.

- [ ] **Step 2: Verify `index.html`**
Verify that:
  - Links properly navigate to `privacy-policy.html` and `support.html`.

- [ ] **Step 3: Commit `index.html`**
```bash
git add pages/index.html
git commit -m "feat: update index landing page with Apple-style portal"
```

---

### Task 4: Complete Verification & Visual Validation

**Files:**
- Test all files in `pages/`

- [ ] **Step 1: Verify translation flags against `.env.production`**
Run automated grep check to ensure AMP, NLT, and NST are not present in `pages/` and that ERV, NASV, KJV, and Amharic 1954 are present.

- [ ] **Step 2: Verify HTML validity and link integrity**
Check all internal anchor links and mailto triggers.

- [ ] **Step 3: Final git commit & clean tree check**
```bash
git status
```
