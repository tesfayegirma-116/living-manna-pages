# Living Manna: Privacy Policy & Support Pages Redesign Spec

**Date:** 2026-08-15  
**Target Repository:** `pages/` (`privacy-policy.html`, `support.html`, `index.html`)  
**Platforms:** Apple App Store (`com.livingmanna.livingManna`) & Google Play Store (`com.livingmanna.livingmanna`)

---

## 1. Overview & Goals

The goal is to provide world-class, clean, Apple-inspired **Privacy Policy** and **Support** pages for **Living Manna**, a bilingual offline Bible reading application for iOS and Android.

Key criteria:
1. **Apple-Style Aesthetic**: Minimalist layout, modern SF/system typography, crisp hierarchy, subtle border cards, and automatic system Light/Dark theme support.
2. **Plain English & Transparency**: Clear "Privacy at a Glance" cards meeting Apple App Privacy nutrition label standards and Google Play Data Safety requirements.
3. **Strict Production Translations**: Only the translations enabled in `.env.production` (KJV, Amharic 1954, ERV, NASV) are listed with their full legal copyright attributions.
4. **Comprehensive Support Hub**: Clear FAQ, widget & backup guides, and frictionless support contact links.

---

## 2. Production Translation Matrix

Based on `.env.production`:
- `ENABLE_AMP=false` *(Excluded)*
- `ENABLE_NLT=false` *(Excluded)*
- `ENABLE_ERV=true` *(Included)*
- `ENABLE_NST=false` *(Excluded)*
- `ENABLE_NASV=true` *(Included)*
- `kjv` / `amharic 1954` *(Always Included, public domain)*

### Included Editions & Copyrights:
1. **King James Version (KJV)** — English. Public domain in the United States.
2. **የድሮ ትርጉም (1954 Edition)** — Amharic. Bible Society of Ethiopia (`https://www.biblesociety.et`).
3. **Easy-to-Read Version™ (ERV)** — English. Holy Bible: Easy-to-Read Version™ (ERV). Copyright © 2006 by Bible League International. Used by permission. All rights reserved. (`https://www.bibleleague.org`).
4. **New Amharic Standard Version™ (NASV / አማ01 / አዲሱ መደበኛ ትርጕም)** — Amharic. The Holy Bible, New Amharic Standard Version™. Copyright © 2001, 2024 by Biblica, Inc. Used with permission. All rights reserved worldwide. (`https://www.biblica.com`).

---

## 3. UI/UX Design System

- **Color Palette**:
  - Light mode: Clean soft white/off-white background (`#fbfbfd`), card background (`#ffffff`), border (`rgba(0, 0, 0, 0.08)`), text primary (`#1d1d1f`), secondary (`#6e6e73`), brand accent (`#b08440` / `#936a28`).
  - Dark mode: Deep black/dark graphite background (`#000000` / `#121214`), card background (`#1c1c1e`), border (`rgba(255, 255, 255, 0.1)`), text primary (`#f5f5f7`), secondary (`#86868b`), brand accent (`#d4af37` / `#c89b4b`).
- **Typography**: `-apple-system, BlinkMacSystemFont, "SF Pro Text", "SF Pro Display", "Helvetica Neue", Arial, sans-serif`.
- **Navigation Bar**: Clean sticky header with brand logo/name and quick navigation tabs for **Privacy** and **Support**.
- **Responsive Layout**: Optimized for mobile, tablet, and desktop viewing with standard Apple card padding and readable max content width (760px).

---

## 4. Page Architecture & Content Details

### A. Privacy Policy (`privacy-policy.html`)
1. **Header & Meta**: Title, last updated date, and quick summary.
2. **Apple-Style Privacy Nutrition Summary Card**:
   - Data Used to Track You: **None**
   - Data Linked to You: **None**
   - Data Not Linked to You: **None**
   - Device Processing: **100% On-Device**
3. **App Store & Google Play Scope**:
   - Android Package: `com.livingmanna.livingmanna`
   - iOS Bundle: `com.livingmanna.livingManna`
4. **Data Practices in Plain English**:
   - Zero analytics, zero ad networks, zero tracking SDKs, no user accounts.
   - Local on-device storage (reading history, bookmarks, notes, highlights, reading plans, preferences).
5. **Permissions & Justifications**:
   - Notifications (Local daily verse & reading plan alerts; no remote servers).
   - Photos / Storage (Saving generated verse cards or selecting user backgrounds).
   - Exact Alarms (Local background reminder scheduling).
6. **Data Export & Sharing**: User-initiated JSON backup and verse sharing via native OS share sheet.
7. **Production Translation Copyrights**: Full text for KJV, Amharic 1954, ERV, and NASV.
8. **Children’s Privacy**: Compliant with COPPA/GDPR-K.
9. **Data Retention & Deletion**: Local deletion instructions and support contact.
10. **Developer Contact**: `tesfayegirma360@gmail.com`.

### B. Support Page (`support.html`)
1. **Support Hero**: Minimalist greeting with direct email CTA (`tesfayegirma360@gmail.com`).
2. **Quick Support Cards**:
   - Email Support
   - App Version & Diagnostics guidance
   - Translation Inquiries
3. **Frequently Asked Questions & Guides**:
   - *Offline functionality*: How offline storage works.
   - *Data migration*: How to export/import JSON backups when switching phones.
   - *Home Screen Widgets*: Troubleshooting iOS WidgetKit and Android AppWidget updates.
   - *Translation corrections*: How to submit verse text errata.
4. **Footer**: Navigation links and copyright notice.

### C. Landing Index (`index.html`)
- Clean routing hub or unified landing that directs visitors to either Privacy Policy or Support with sleek Apple styling.

---

## 5. Verification & Quality Checklist
- [x] Zero external dependencies / works 100% standalone vanilla HTML + CSS.
- [x] Tested for responsive rendering and dark mode support.
- [x] Confirmed only production versions (KJV, Amharic 1954, ERV, NASV) are referenced.
- [x] Confirmed compliance with Apple App Store Guideline 5.1.1 and Google Play User Data policies.
- [x] Validated semantic HTML5 and clean accessibility tags.
