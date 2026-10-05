# Google Ads (App Campaign, iOS) — Simple IAP Strategy for Doc Scanner

**App:** Doc Scanner: PDF Scan & OCR (iOS, id 6759896516)  |  **Prepared:** 2026-10-05
**Companion docs:** `iap-campaign-competitor-analysis.md` (competitor research), `Doc-Scanner-IAP-Campaign-Plan.docx` (Apple Ads / Meta / TikTok plan)

---

## 1. What the competitors teach us (and why Google is channel #3, not #1)

| Competitor | Where they buy users | Lesson for Google Ads |
|---|---|---|
| CamScanner | Apple Ads + Custom Product Pages (official Apple case study), broad social | Google is not their lead iOS channel; conquest on "cam scanner" is cheaper on Apple Ads than on Google. |
| iScanner | Paywall-first, social humour creative, deal sites | Their creative works because it shows a paperwork pain in 2 seconds. Copy the format, not the paywall. |
| ScanGuru / Scan Shot | Meta + TikTok video, $6.99/week economics | They can pay $3–4 per install. On Google iOS, do not fight them on broad "scanner app" clicks; win on message (no weekly, no watermark). |
| Adobe Scan / Scanner Pro | Almost no paid UA | "adobe scan" and "scanner pro" intent is cheap everywhere, but Google App Campaigns do not take keywords, so this advantage is used in Apple Ads, not here. |
| Microsoft Lens (retired Dec 2025) | n/a | Orphaned users search on Google and YouTube for a replacement. This is the one audience Google reaches better than Apple Ads. |

**Why Google is third:** iOS App Campaigns are measured only through SKAdNetwork (no keyword control, 8-campaign cap per app, tCPI or tCPA only), so in-app purchase attribution is the weakest of the four channels. Use it for incremental reach on YouTube, Discover and Search once Apple Ads has proven that installs turn into payers.

---

## 2. Country targeting

| Phase | Countries | Language | Why | Target CPI | Target cost per trial |
|---|---|---|---|---|---|
| 1 (start) | United States | English | Highest ARPU; where every competitor earns most; Apple Ads data already exists to compare against | $3.50 | $35 |
| 2 (+3 weeks if Phase 1 hits goal) | United Kingdom, Canada, Australia | English | Same creative, 80–85% of US bids; tax deadlines Jan 31 (UK), Apr 30 (CA), Jun 30 (AU) | $3.00 | $30 |
| 3 (after localisation) | Germany, France | German, French | Need translated assets and store listing | $2.50 | $25 |
| Skip | India, Brazil, Mexico | — | Low iOS ARPU; Google volume there is Android-heavy | — | — |

Run **one campaign per country group** (US; GB+CA+AU; DE; FR) so bids and budgets stay separate. Never mix the US with lower-ARPU countries in one campaign, or Google will spend where clicks are cheapest.

---

## 3. Campaign setup

| Setting | Value |
|---|---|
| Campaign type | App campaign → App installs → iOS → Doc Scanner |
| Start | **Option A (recommended):** January 12 2027, after Apple Ads Gate B proves install-to-paid ≥ 5%. **Option B (parallel test now):** start October 20 2026 at $30/day, tCPI only, US only. |
| Conversion source | Firebase (Google Analytics for Firebase SDK 12.12.1+) with **on-device conversion measurement** enabled; events: `first_open`, `first_scan`, `paywall_view`, `trial_start`, `in_app_purchase`. Mark `trial_start` as the primary conversion in Google Ads. Alternative: AppsFlyer/Adjust as the conversion source if you already use an MMP. |
| SKAdNetwork schema | Let Google Ads manage the SKAN conversion value schema through Firebase; map `trial_start` and `in_app_purchase` as the highest values. |
| Bidding, weeks 1–3 | **Target cost per install (tCPI) $3.50** (US). Daily budget at least 50× tCPI = **$175/day** if you want Google's learning to finish in 2 weeks; minimum viable **$50/day** (accept a 3–4 week learning phase). |
| Bidding, week 4 onward | Switch to **Target cost per action (tCPA) on `trial_start` = $35** (US) once the campaign has ≥ 10 trial conversions per day for 7 days; if it never reaches that, stay on tCPI and judge on RevenueCat cost per trial instead. Daily budget at least 10× tCPA = $350/day at full scale; $100/day minimum. |
| Goal for the IAP | Cost per trial ≤ $35 → with 35% trial-to-paid, cost per payer ≤ $100 on Google (vs $55–70 target on Apple Ads). Accept the higher number only while 12-month projected ROAS stays ≥ 100%; otherwise cut Google and move the budget to Apple Ads. |
| Locations / languages | Per section 2; language = English (US campaign) |
| Ad schedule | All day; review after 4 weeks |
| Devices | iPhone and iPad (cannot exclude iPad in App campaigns; fine for scanner intent) |
| Naming | DS_US_GG_APP_TCPI → rename to DS_US_GG_APP_TCPA after the switch |

**Bid ladder by country (tCPI / tCPA):** US $3.50 / $35 · GB $3.00 / $30 · CA $2.80 / $28 · AU $2.80 / $28 · DE $2.50 / $25 · FR $2.30 / $23.

**Weekly rules (keep it simple):**
1. Do not touch bids or budget for the first 14 days.
2. After that, if cost per trial (from RevenueCat, not Google's modelled number) is under $28, raise budget 20% per week.
3. If cost per trial is over $45 for two weeks, lower tCPA 10%; if still over after two more weeks, pause the campaign.
4. Replace the lowest-rated asset (Google shows "Low" performance labels) every two weeks.

---

## 4. Ad assets

### 4.1 Headlines (max 30 characters, use 5; the rest are swaps)

| # | Headline | Chars | Angle (competitor gap) |
|---|---|---|---|
| 1 | Scan to PDF in One Tap | 22 | Core task |
| 2 | No Watermark Scanner App | 24 | CamScanner, Scanner Pro, iScanner free tiers |
| 3 | OCR: Paper to Editable Text | 27 | Adobe paywalls Word export |
| 4 | Unlimited Free Scans | 20 | ScanGuru, TapScanner caps |
| 5 | Sign PDFs on Your iPhone | 24 | Task intent |
| swap | Scanner App, No Sign-Up | 23 | Adobe forced account |
| swap | Scans Stay on Your Phone | 24 | Privacy vs cloud apps |
| swap | $29.99/Year, Not $7/Week | 24 | ScanGuru / iScanner weekly (allowed on Google, not on Apple Ads) |
| swap | Scan Receipts for Tax Season | 28 | Jan 15 – Apr 15 only |

### 4.2 Descriptions (max 90 characters, use 5)

| # | Description | Chars |
|---|---|---|
| 1 | Scan documents, receipts and IDs to clean PDFs. Free, unlimited, no watermark. | 78 |
| 2 | Turn paper into editable text with on-device OCR. Export to Word. No account needed. | 84 |
| 3 | The honest scanner: unlimited free scans, one simple Pro plan, cancel anytime. | 78 |
| 4 | Sign, fill and share PDFs without a printer. Fast auto-crop and shadow removal. | 79 |
| 5 | Tax season ready: batch-scan receipts, organise in folders, export to Excel. | 76 |
| swap | Microsoft Lens is retired. Scan whiteboards, cards and docs to Word or PDF free. | 80 |
| swap | Private by design: nothing is uploaded. Scan IDs and medical forms with confidence. | 83 |

### 4.3 Image creatives (upload all three ratios; Google needs them for Discover, YouTube and Display)

| Size | Ratio | Visual | On-image text (keep under 20% of area) |
|---|---|---|---|
| 1200 × 628 | 1.91:1 landscape | Phone scanning a receipt, clean PDF appearing on the right | "Scan to PDF. No watermark." |
| 1200 × 1200 | 1:1 square | Split: left = watermarked page (generic, no competitor logo), right = clean Doc Scanner page | "Free means free." |
| 1200 × 1500 | 4:5 portrait | OCR demo: paper → editable text with cursor | "Paper to Word in 3 seconds. Offline." |
| 1200 × 628 (seasonal) | 1.91:1 | Pile of receipts → tidy "Tax 2026" folder | "Receipts scanned. Done." |
| 320 × 50, 300 × 250 (optional) | banners | App icon + one line | "Scanner app with no watermark" |

Style rules: real iPhone frame, actual app UI (not mock-ups), one message per image, app icon in a corner, no competitor names or logos, no "App of the Day" or ranking claims.

### 4.4 Videos (upload to YouTube as unlisted; Google needs all three orientations)

Each script in three cuts: **15 s** (main), **6 s bumper**, and **30 s** (YouTube in-stream). Orientations: 9:16 (1080×1920), 16:9 (1920×1080), 1:1 (1080×1080). Captions burned in; app visible within 1.5 seconds; end card = app icon + "Download on the App Store".

**Video 1 — "Free means free" (no watermark)**

| Time | Visual | On-screen text / voice-over |
|---|---|---|
| 0–2 s | Close-up of a scanned page with a big faded "Scanned with …" watermark across it | "Your free scanner put THIS on your document?" |
| 2–6 s | Hand opens Doc Scanner, scans the same page; auto-crop snaps, shadow disappears | "Doc Scanner. Unlimited scans. No watermark." |
| 6–11 s | Export → clean PDF → share to Mail | "Free means free." |
| 11–15 s | End card with icon and store badge | "Doc Scanner: PDF Scan & OCR. Download free." |

**Video 2 — "Stop paying weekly" (price contrast; competitor weekly economics)**

| Time | Visual | On-screen text / voice-over |
|---|---|---|
| 0–2 s | Phone showing a generic weekly paywall "$6.99 / week" (no logos) | "Seven dollars a week… to scan a receipt?" |
| 2–7 s | Swipe to Doc Scanner: scan 3 receipts in a row, one tap each | "Doc Scanner scans unlimited pages free." |
| 7–12 s | Simple paywall screen: "Pro $29.99 / year, 7-day free trial, cancel anytime" | "Pro is $29.99 a year. Shown up front. Cancel anytime." |
| 12–15 s | End card | "The honest scanner app." |

**Video 3 — "Nothing leaves your phone" (privacy; vs forced account and cloud)**

| Time | Visual | On-screen text / voice-over |
|---|---|---|
| 0–2 s | Finger flips Airplane Mode on | "No signal. Watch this." |
| 2–8 s | Scan a passport/ID card, run OCR, text appears, copy to Notes, all offline | "Scan. OCR. Export. All on your iPhone." |
| 8–12 s | Settings screen: no login prompt; "No account needed" | "No sign-up. No cloud upload. Nothing leaves your phone." |
| 12–15 s | End card | "Doc Scanner. Private by design." |

**Seasonal video 4 — "Tax receipts in 60 seconds"** (Jan 15 – Apr 15): kitchen table, pile of receipts → batch scan → "Tax 2026" folder → Export to Excel → end card "Scan receipts for tax season".

**Lens replacement video 5** (always on, low budget): "Microsoft Lens stopped working in December 2025" → whiteboard scan, business card, document to Word → "Here's what to use instead."

---

## 5. Budget and expected results (US, after switching to tCPA)

| Item | Value |
|---|---|
| Daily budget | $100 (test) → $350 (scale) |
| Monthly spend at scale | ~$10,500 |
| Installs at $3.50 CPI | ~3,000 |
| Trials at 10% | ~300 (cost per trial ~$35) |
| Payers at 35% trial-to-paid + 1% direct | ~135 (cost per payer ~$78) |
| 12-month projected net proceeds at $68.90 per payer | ~$9,300 (ROAS ~90%) |

Reading: Google on iOS is roughly break-even at benchmark numbers. It earns its place only if (a) Google's modelled conversions and RevenueCat cohorts agree within 20%, and (b) the campaign lifts organic installs (YouTube and Discover reach) by more than Apple Ads does at the same spend. Check both at the 8-week mark and cut if either fails.

---

## 6. Setup checklist

- [ ] Firebase SDK 12.12.1+ in the app; `trial_start` and `in_app_purchase` events sent from the StoreKit purchase handler; on-device conversion measurement enabled.
- [ ] Google Ads linked to Firebase; `trial_start` imported as a conversion; SKAN schema managed by Google Ads.
- [ ] YouTube channel with the 5 videos × 3 orientations uploaded (unlisted).
- [ ] 5 headlines, 5 descriptions, 5 images (3 ratios + 2 seasonal) uploaded; seasonal assets scheduled.
- [ ] Campaign DS_US_GG_APP_TCPI created with tCPI $3.50, budget $50–175/day, US, English.
- [ ] Calendar reminder: day 14 first review; day 28 tCPA switch decision; week 8 keep-or-cut decision.
