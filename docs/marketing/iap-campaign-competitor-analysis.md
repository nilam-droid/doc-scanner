# Doc Scanner: PDF Scan & OCR — Top-5 Competitor Analysis and IAP Campaign Plan

**App:** Doc Scanner: PDF Scan & OCR (iOS, App Store id 6759896516)
**Prepared:** 2026-10-05
**Scope:** US-first in-app-purchase (IAP) acquisition campaign on iOS, with Apple Ads as the primary channel and Meta / TikTok as phase-2 channels.

> **How this was researched.** Everything below comes from public web sources (App Store listing snippets, Sensor Tower public overview pages, RevenueCat / Adapty / AppTweak / SplitMetrics benchmark reports, Apple developer documentation, vendor blogs, review aggregators). The research environment could not open apps.apple.com, Sensor Tower, or most tracker sites directly, so download and revenue figures are *third-party estimates as shown in search snippets* and should be re-pulled from your Sensor Tower account before going into a deck. Section 8 lists exactly which Sensor Tower reports to pull.

---

## 1. Executive summary

**The category is large, profitable, and monetised through aggressive weekly subscriptions, not download volume.** The nine named iOS scanner apps below gross roughly **$15M/month** combined; CamScanner and iScanner alone are about two-thirds of that. The "weekly-paywall indie" cohort (iScanner, ScanGuru, Scan Shot, Tiny Scanner) earns **$4.50–$25 per download**, which is what lets them outbid everyone on "scanner app" keywords. Adobe Scan and Scanner Pro earn $1.50–$2.50 per download and barely run paid acquisition.

**Top 5 competitors (ranked by estimated iOS revenue):**

| # | App | Developer | Est. iOS monthly downloads / revenue | Paywall style | Headline price |
|---|---|---|---|---|---|
| 1 | CamScanner | INTSIG (China) | 2–3M / $5–7M | Soft paywall, watermark + ads on free | $4.99/wk, $49.99/yr ($35.99 first year) |
| 2 | iScanner | BPMobile / AIBY (US) | 300–400K / $4M | Hard paywall after first scan, 3-day trial | $3.99–4.99/wk, $19.99–20.99/yr |
| 3 | Adobe Scan | Adobe | 700–800K / $2M | Soft paywall, free has no watermark | $9.99/mo, $59.99–69.99/yr, 7-day trial |
| 4 | ScanGuru | Universe Group (Ukraine/Cyprus) | 150–300K / $0.75–1M | Hard-ish paywall, 7-day trial | $6.99/wk, $69.99/yr, $59.99 lifetime |
| 5 | Scanner Pro | Readdle (Ukraine) | ~50K / ~$200K | Soft paywall, watermark on free | $19.99/yr, 7-day trial |

**Where Doc Scanner can win.** Every big player has a loud, documented weakness that shows up in 1-star reviews: CamScanner (trust, watermark, ads, China), iScanner (hard paywall + trial billing complaints), Adobe Scan (forced Adobe ID and cloud upload, 415 MB app), ScanGuru ($6.99/week "deceptive trial" complaints), Scanner Pro (watermark re-appearing, legacy-user backlash). Microsoft Lens was fully retired in December 2025, orphaning free-OCR users. The open position is **"honest, private, lightweight scanner: unlimited scans free with no watermark, pay only for OCR / export / sign, no account required, on-device processing"**.

**Campaign recommendation in one paragraph.** Run Apple Ads Advanced, search results placement only, structured as four campaigns (Brand, Category, Competitor, Discovery) feeding six Custom Product Pages mapped to search intent. Measure install-to-trial-to-paid deterministically through the AdServices attribution token joined to StoreKit 2 transactions in RevenueCat (or Adapty), and use SKAdNetwork / AdAttributionKit conversion values only as a cross-check. Start at **$100/day for 4 weeks**, scale winners to $300–500/day, and layer Meta App Event Optimization on "trial started" in month 3. Target **cost per install ≤ $3.00 on category terms, install-to-paid ≥ 5%, cost per paying subscriber ≤ $60**, against a 12-month Utilities trial-subscriber LTV benchmark of **$68.90** (RevenueCat 2026). Time the first scale-up to **US tax season (mid-January to April 15)**, which is the category's demand peak.

---

## 2. Your app: what we know and what to fix first

| Item | Finding |
|---|---|
| Indexed title for id 6759896516 | **"Cam Scanner - All Doc scanner App"** (Czech storefront page; developer **Kalpesh Pirojiya**; category Productivity; iOS 16+; free with IAP). The title "Doc Scanner: PDF Scan & OCR" from your URL is not yet indexed anywhere, so it is either a very recent rename or a US-only title. Source: https://apps.apple.com/cz/app/cam-scanner-all-doc-scanner/id6759896516?platform=ipad |
| Release date, IAP SKUs, prices, rating | Not found publicly. No third-party estimate page exists yet, which is consistent with a late-2025 release and low volume. |
| Name collisions | "Doc Scanner - PDF Scan & OCR" (id 1592248390), "PDF Scan & OCR: Doc Scanner" (id 6654918235), "Doc Scanner PDF with AI & OCR" (id 6443812062, 4.8 / 512 ratings), "Doc Scan - PDF Scanner" (id 453312964, 4.8 / 14K ratings). Brand-term bidding on "doc scanner" will share traffic with these. |

**Pre-campaign fixes (do these before spending a dollar):**

1. **Settle the title and subtitle.** Keep "Doc Scanner" as the brand. Do not keep "Cam Scanner" in the title: it invites a trademark complaint from INTSIG, it tells Apple Ads relevance that you are a CamScanner clone, and it dilutes your own brand term. Recommended: title `Doc Scanner: PDF Scan & OCR`, subtitle `Scan to PDF, Sign & Export` (30-char limit; the subtitle is shown in every Apple Ads placement and ad assets may not contain price or offer claims).
2. **Confirm category.** Competitors split between Productivity (CamScanner) and Business (iScanner, Adobe Scan, ScanGuru, Scanner Pro). Business has a smaller top-grossing chart that is not dominated by ChatGPT-class apps; moving to Business makes chart visibility achievable sooner.
3. **Lock the SKU ladder and paywall** (Section 6) and configure Promoted In-App Purchases, an introductory offer, and Custom Product Pages (Section 7.2) in App Store Connect.
4. **Ship attribution** (AdServices token + RevenueCat or Adapty + App Store Server Notifications V2) before the first tap is bought (Section 7.3).

---

## 3. Market snapshot

### 3.1 Size and money flow

- Global non-game app IAP reached **$85B in 2025 (+21% YoY)** and surpassed games for the first time; Productivity is named as a growth driver. Source: Sensor Tower State of Mobile 2026, https://sensortower.com/blog/state-of-mobile-2026
- Named iOS scanner apps, Sensor Tower public "last month" estimates (undated snippets, iOS, country as shown):

| App | Downloads | Revenue | Revenue per download |
|---|---|---|---|
| CamScanner | 2–3M | $5–6M | ~$2–3 |
| iScanner (US page) | 400K | $4M | ~$10 |
| Adobe Scan (US page) | 800K | $2M | ~$2.5 |
| ScanGuru (US page) | 200–500K | $900K | ~$2–4.5 |
| Scan Shot (US page) | 70K | $800K | ~$11 |
| Tiny Scanner (US page) | 20K | $500K | ~$25 |
| "Scanner" id 1291962681 (US) | 100K | $400K | ~$4 |
| Genius Scan (US page) | 200K | $300K | ~$1.5 |
| Scanner Pro | 50K | $200K | ~$4 |

Sources: https://app.sensortower.com/overview/388627783 , https://app.sensortower.com/overview/1040093707?country=us , https://app.sensortower.com/overview/1199564834?country=US , https://app.sensortower.com/overview/1040149161?country=us , https://app.sensortower.com/overview/1575194801?country=US , https://app.sensortower.com/overview/595563753?country=US , https://app.sensortower.com/overview/1291962681?country=US , https://app.sensortower.com/overview/377672876?country=us , https://app.sensortower.com/overview/333710667

The spread in revenue per download is the single most important number in this document: it is the ceiling on what each competitor can pay per install, and it is set by the paywall, not by the product.

### 3.2 Subscription benchmarks that apply to a scanner app

| Metric | Value | Source |
|---|---|---|
| Weekly plans' share of all subscription-app revenue | 55.5% in 2025 (43.3% in 2023) | RevenueCat State of Subscription Apps 2026, https://www.revenuecat.com/state-of-subscription-apps |
| Utilities: weekly share of subscription revenue | 73.6% | Adapty 2026, https://adapty.io/blog/utilities-app-subscription-benchmarks/ |
| Utilities: median download-to-trial | 6.5% | RevenueCat 2026 Utilities, https://www.revenuecat.com/state-of-subscription-apps-2026-utilities |
| Utilities: 12-month LTV of a trial subscriber | **$68.90** (highest of any category); trials deliver +85% LTV vs direct purchase in Utilities | same |
| Hard paywall: median download-to-paid | 4.2% (2x freemium); top decile 38.7% | same |
| Hard paywall: Day-35 trial-to-paid | 10.7% vs 2.1% freemium | RevenueCat 2025, https://www.revenuecat.com/state-of-subscription-apps-2025 |
| Global install-to-trial / trial-to-paid | 10.9% / 25.6% | Adapty 2026, https://adapty.io/state-of-in-app-subscriptions/ |
| Weekly + trial 12-month LTV | $49.27 | same |
| Trial cancellations on day 0 (3-day trials) | 55.4% | RevenueCat 2026 |
| Refund rate | 2–5% of payers | RevenueCat 2025 |
| Annual cancellations in month 1 | 35% of all annual cancels; cancelled annual subscribers rarely return | https://9to5mac.com/2026/05/27/new-report-shows-annual-app-subscribers-rarely-return-after-they-cancel/ |
| Apple Ads install-to-paid, Productivity + Utilities (US) | 5.36% | Adapty, https://adapty.io/blog/apple-ads-install-to-paid-rate-benchmarks/ |

### 3.3 Apple Ads cost benchmarks (US, 2025 data published 2026)

| Source | CPT | CPI / CPA | TTR | CR |
|---|---|---|---|---|
| AppTweak (US median, ~2,800 advertisers) | $1.91 | $4.06 | — | 50–67% by category |
| AppTweak Business | $3.33 | $6.86 | 7.8% | — |
| AppTweak Productivity | $1.74 | $3.58 | 8.3% | — |
| AppTweak Utilities | $1.23 | $2.25 | 10.6% | — |
| SplitMetrics (top-15 categories) | $2.25 | $3.76 | 9.7% | 66.2% |
| Adapty (US all) | $1.58 | $2.51 | 9.0% | 62.7% |
| **Adapty "Document Scanner" niche** | **$2.36** | **$3.74** | — | **63.1%** |
| Adapty "PDF Reader" niche | $3.36 | $4.31 | — | 77.9% |
| MobileAction, ads using Custom Product Pages | $1.46 | $3.07 (down from $4.58) | — | — |

Sources: https://www.apptweak.com/en/aso-blog/apple-ads-benchmarks , https://splitmetrics.com/apple-ads-search-results-benchmarks-2026/ , https://adapty.io/blog/apple-ads-benchmarks-2026/ , https://adapty.io/blog/apple-ads-benchmarks-by-niche/ , https://www.mobileaction.co/report/apple-ads-2026-benchmark-report/ad-variations-using-custom-product-pages/

**Planning numbers used in this plan:** CPT $1.25–$2.40, CPI $2.25–$3.75, TTR 9–11%, CR 60–65%, install-to-paid 5% → cost per payer about $45–$75 on category and discovery terms, lower on brand and exact terms.

### 3.4 Seasonality

- **US tax season (mid-January to April 15)** is the category peak; iScanner ran a "here to save tax season, $26 for life" promotion on 2026-03-31 and ScanGuru ran a "Get Ready for Tax Season" in-app event 2026-03-17 to 04-13. Sources: https://boingboing.net/2026/03/31/iscanners-here-to-save-tax-season-at-only-26-for-life.html , https://appshunter.io/ios/app/scanguru-pdf-scanner-app/id1040149161
- **Back-to-school (August–September):** education downloads +40–60%; productivity peaks in September. Source: https://www.appalize.com/blog/aso-strategies/seasonal-aso-how-to-optimize-your-app-for-holidays-and-events
- **Year-end paperwork (mid-December to early January):** ScanGuru's "Christmas Scans and Signs" event.

### 3.5 What changed in 2025–2026 that affects this campaign

- **Apple Ads multiple search slots** went live globally on 2026-03-17: ads now also appear further down search results, auto-eligible, no per-position bidding, visible on iOS 26.2+. More inventory, somewhat lower average position quality. Sources: https://9to5mac.com/2026/01/22/app-store-search-ads-more-ads-march/ , https://adapty.io/blog/apple-ads-multiple-adslots/
- **Maximize Conversions bidding** (target-CPA auto-bidding for search results) launched 2026-03-16. Source: https://ads.apple.com/app-store/help/campaigns/0095-maximize-conversions
- **Custom Product Pages raised from 35 to 70 per app** (2025-10-29). Source: https://adapty.io/blog/custom-product-pages-app-store/
- **Apple's Search Popularity scores collapsed by 77% on 2025-09-29**, so every ASO tool's "volume" numbers are now unreliable for low-volume terms; use the Search Term Rank report inside Apple Ads Advanced instead. Source: https://aso.dev/blog/apple-ads-popularity-massive-drop/
- **Microsoft Lens retired**: removed from the App Store 2025-11-15, scanning disabled 2025-12-15; Microsoft points users to the Microsoft 365 Copilot app, which cannot save to OneNote/Word. Source: https://techcrunch.com/2025/08/08/rip-microsoft-lens-a-simple-little-app-thats-getting-replaced-by-ai/
- **Epic v. Apple (US storefront):** since 2025-05-01 apps may link to external purchase methods with no entitlement; the Ninth Circuit (2025-12-11) allowed Apple to charge a cost-based commission on link-outs, remanded; Supreme Court review pending into 2027. **Recommendation: keep StoreKit IAP as the only purchase path for this campaign.** Linking out forfeits Promoted IAPs, intro offers, win-back offers and the AdServices-to-StoreKit measurement chain. Sources: https://developer.apple.com/news/?id=9txfddzf , https://law.justia.com/cases/federal/appellate-courts/ca9/25-2935/25-2935-2025-12-11.html
- **Apple Ads Basic is still live** (CPI pricing, search results only, $10K/app/month cap). The thing being retired is the old Campaign Management API on 2027-01-26. Source: https://ads.apple.com/app-store/help/apple-ads-basic/0001-compare-apple-ads-solutions
- **AI features are table stakes:** CamScanner "CS AI", iScanner AI toolbox + on-device Edge Repair (Sep 2025), Adobe Scan AI Assistant with citations (2025), Scanner Pro on-device neural colour mode (Mar 2026). The 2026 differentiator is **on-device** AI versus cloud AI.

---

## 4. The top 5 competitors in depth

### 4.1 CamScanner — PDF Scanner App (INTSIG, id 388627783)

| Field | Value |
|---|---|
| Title / subtitle | "CamScanner - PDF Scanner App" / "Document Scanner PDF Converter" |
| Category, rating | Productivity; 4.8 stars, ~1.9M US ratings |
| Charts | #7–9 top-grossing Productivity (US iPhone, Aug 2026 snapshots) |
| Scale claims | 300M+ users (2025 annual summary), 750M+ downloads across platforms; #1 Productivity in 84 countries |
| Est. iOS last month | 2–3M downloads, $5–7M revenue |
| Free tier | Ads; "Scanned with CamScanner" watermark on every export; OCR preview only; 200 MB–1 GB cloud |
| Paid SKUs seen | $4.99/week; $4.99 and $9.99/month; $49.99/year with $35.99 first-year intro (older variant $39.99 / $29.99 first year); $59.99 and $69.99 yearly variants; no lifetime |
| Trial / paywall | 3-day trial on annual; soft paywall after a 6-step onboarding carousel; account creation prompted after purchase |
| Paid UA | Documented Apple Ads success story: +50% downloads after adopting Custom Product Pages (https://ads.apple.com/app-store/success-stories/camscanner); active TikTok / Instagram / YouTube handles |
| Release cadence | 2–3 releases per month; 2026 pushes: AI search, AI Image Detector, scan-to-translate, "Mega Scan" stitching, redaction |
| Trust history | 2019 Android malware in an ad SDK (Kaspersky); banned in India since June 2020; independent review sites 2.6–3.2/5 despite 4.8 store rating |

**Strengths:** largest brand and budget; constant feature velocity; a finely tuned paywall (weekly impulse SKU, discounted first year, "limited time" urgency); proven Apple Ads + CPP playbook.

**Attackable gaps:** trust (China, malware, India ban, data sharing), watermark + ads + OCR-preview-only free tier, trial auto-renew complaints and cancellation friction, feature bloat. Weekly $4.99 is $259/year effective, a strong price anchor for ads.

**Copy:** soft paywall right after a short value carousel with annual-plus-intro-price pre-selected and weekly as the impulse option; account creation only after purchase; CPPs keyed to intent (ID card, receipts, OCR to Word, sign PDF).

Sources: https://apps.apple.com/us/app/camscanner-pdf-scanner-app/id388627783 , https://screensdesign.com/showcase/camscanner-pdf-scanner-app , https://essexsoftware.com/scaniva/camscanner-free-vs-paid/ , https://adapty.io/paywall-library/camscanner-pdf-scanner-app/ , https://blog.camscanner.com/2025/12/19/camscanner-releases-2025-annual-summary-highlighting-breakthrough-innovation-and-a-global-user-base-exceeding-300-million/ , https://restofworld.org/2024/india-banned-camscanner-government-agencies/ , https://thehackernews.com/2019/08/android-camscanner-malware.html

### 4.2 iScanner — PDF Document Scanner (BPMobile / AIBY, id 1040093707)

| Field | Value |
|---|---|
| Title / subtitle | "iScanner: PDF Document Scanner" / "Scan Photos, Papers with OCR" |
| Category, rating | Business (#76 Business free chart); 4.8 stars, ~1.4M US ratings |
| Scale claims | 145M+ users; "topped US scanning charts in downloads and revenue for 4 years" (press kit) |
| Est. iOS last month | 300–400K downloads, $4M revenue ("How iScanner makes $4 million per month") |
| Free tier | On iOS effectively none: paywall appears as soon as you take the first photo. Android free tier: 5 exports/day, ads, watermark |
| Paid SKUs seen | $3.99 and $4.99/week (bundled with 10 GB / 100 GB cloud); $4.99 and $9.99/month; $19.99–$20.99/year; lifetime only off-store ($39.99 StackSocial, $26 tax-season deal) |
| Trial / paywall | Hard paywall; 3-day trial with the free-trial toggle **off by default**; yearly pre-selected and framed "$0.40/week, save 91%" against the weekly |
| Paid UA | Paywall and onboarding catalogued as reference cases by Adapty, ScreensDesign, Mobbin; Instagram 185K followers; TikTok humour creative around paperwork pain |
| Release cadence | 2–4 iOS releases per month; AI Assistant redesign (Jun 2026), fax sending (Aug 2026), on-device Edge Repair (Sep 2025), AI Math Mode |
| Review themes | 1-star: "can't do anything until you subscribe", trial billing confusion, "did not want to pay $10/m", ads and pop-ups, over-complicated. 5-star: scan quality, OCR in poor light, AI assistant |

**Strengths:** the best-monetised scanner on iOS; hard paywall with trial-toggle-off maximises direct-to-paid; strong "AI" narrative with demo-able features; 10 years of brand equity; brand term is already being squatted by a clone (id 6746195111), so they defend it.

**Attackable gaps:** hard paywall before any value and weekly billing drive the loudest "scam" reviews on Apple's own forums (https://discussions.apple.com/thread/255216813); ads and pop-ups; perceived complexity; cloud upload complaints from paying users; confusing overlapping SKU names.

**Copy:** yearly-anchored paywall with trial toggle defaulting off; short-form humour creative; "AI" headline with concrete demo features in screenshots; frequent small releases.

Sources: https://apps.apple.com/us/app/iscanner-pdf-document-scanner/id1040093707 , https://startupspells.com/p/iscanner-pdf-ocr-scanner-mobile-app-onboarding-genius , https://adapty.io/paywall-library/scanner-pdf/ , https://justuseapp.com/en/app/1040093707/scanner-app-pdf-document-scan/reviews , https://iscanner.com/for-media/ , https://betanews.com/2025/09/24/iscanner-introduces-ai-edge-repair-to-fix-stapled-and-damaged-document-scans/ , https://www.stacksocial.com/sales/iscanner-app-lifetime-subscription

### 4.3 Adobe Scan — PDF & OCR Scanner (Adobe, id 1199564834)

| Field | Value |
|---|---|
| Title | "Adobe Scan: PDF & OCR Scanner" (several title variants indexed, consistent with active CPPs) |
| Category, rating | Business (#34 Business free; #10–11 top-grossing Business); 4.9 stars, ~1.6M US ratings |
| Scale claims | 150M+ downloads, 2.5B documents |
| Est. iOS last month | 700–800K downloads, $2M revenue |
| Free tier | The most generous in the category: unlimited scans, no watermark, no ads, OCR up to 25 pages per file, 2 GB cloud. **Adobe ID sign-in required before first scan; auto-upload to Document Cloud cannot be disabled.** |
| Paid SKUs seen | Scan Premium $9.99/month, $59.99–$69.99/year; "Scan Plus" $4.99/month and $19.99/year (feature split undocumented); PDF Pack $9.99 |
| Trial / paywall | 7-day trial on yearly only; monthly bills immediately; Premium unlocked free for Acrobat / Creative Cloud subscribers |
| Paid UA | No Apple Ads or paid-social evidence found; relies on Acrobat/Reader cross-promotion |
| Release cadence | About every two weeks; AI Assistant with citations (May 2025), generative summary (Aug 2025), auto-straighten, contract key-term extraction |
| Review themes | 1-star: forced Adobe ID, mandatory cloud upload, slow/stuck uploads, sluggish on older iPhones, 415 MB install, double-charged on trial. 5-star: truly free, best printed-text OCR, trusted brand |

**Strengths:** brand trust and the strongest free offer; OCR quality; zero-CAC distribution through Acrobat bundling; clean trial design.

**Attackable gaps:** forced account + cloud (a direct hit for ID, medical and legal documents); performance and size; Word/Excel export, combine and password-protect all behind $9.99/month; weak paid-UA footprint, so "adobe scan" and "ocr scanner" conquest terms should be cheap.

**Copy:** zero-watermark free scanning as the top-of-funnel promise with OCR page cap and export formats as the paywall lever; 7-day trial on annual only; "scan anything" multi-object screenshot sequence; Business-category placement.

Sources: https://apps.apple.com/us/app/adobe-scan-pdf-ocr-scanner/id1199564834 , https://www.adobe.com/devnet-docs/adobescan/ios/en/managingsubscriptions.html , https://www.techradar.com/pro/software-services/adobe-scan-2025-review , https://helpx.adobe.com/acrobat/using/ai-assistant-adobe-scan.html , https://community.adobe.com/t5/adobe-scan-discussions/adobe-scan-files-not-uploading-for-a-month-now-deleted-from-device/td-p/15468719 , https://zapier.com/blog/best-mobile-scanning-ocr-apps/

### 4.4 ScanGuru — PDF Scanner App (GM UniverseApps / Universe Group, id 1040149161)

Chosen as the fifth competitor over Genius Scan, SwiftScan, Tiny Scanner, Scan Shot and TapScanner because it is the largest uncovered app on US iOS by revenue, it is paid-UA-driven, and it bids on exactly the keyword cluster this campaign targets. TapScanner is bigger worldwide but Android-weighted (~#93 US Business grossing). Scan Shot is a close runner-up (~$700–800K/month on only 20–70K downloads).

| Field | Value |
|---|---|
| Title / subtitle | "ScanGuru: PDF Scanner App" / "Document Scanner, Photo to PDF" (title rotated at least five times across "PDF & Photo Scanner", "Document PDF Scanner", "Pro PDF Scanner App") |
| Category, rating | Business (#19 top-grossing Business, #45 top-free Business, US); 4.6 stars, 93K US / 487K+ worldwide ratings; 36M+ lifetime downloads |
| Developer | Universe Group (Genesis ecosystem, Ukraine), Cyprus entity; sister app Cleaner Guru hit #1 US App Store in 2025 |
| Est. iOS last month | 150–300K downloads, $750K–$1M revenue, ~$4.50 per download |
| Free tier | Ads; caps on scans and folders; no OCR, annotation or e-signature |
| Paid SKUs seen | $6.99/week (also $7.99 and $9.99 price tests); $69.99/year; **$59.99 lifetime, priced below yearly**; no monthly |
| Trial / paywall | 7-day trial, hard-ish paywall right after the feature carousel, single weekly plan on the main screen |
| Paid UA | Privacy policy discloses Facebook Custom Audience and Facebook / Instagram / TikTok ads; paywall catalogued by Adapty, ScreensDesign, Paywall Screens; no Apple Ads evidence found |
| In-app events | "Get Ready for Tax Season" (2026-03-17 to 04-13), "Christmas Scans and Signs" (2024-12-18 to 2025-01-09) |
| Review themes | Complaints Board 3.6/5: "misleading free", trapped after trial converts to $6.99/week, hard to cancel, PDF-to-Word mis-formats, handwriting OCR unreliable |

**Strengths:** a Genesis-style paid-UA machine with heavy creative testing; $6.99/week economics that let them pay $3–4 per install; listing agility and seasonal events; mature feature set.

**Attackable gaps:** dominant 1-star theme is "deceptive trial / weekly"; crippled free tier; weak OCR on handwriting, columns and tables; little brand loyalty (users search generically); no visible Apple Ads CPP investment.

**Copy:** keyword-dense title + subtitle covering "PDF Scanner App" and "Document Scanner, Photo to PDF"; seasonal in-app events tied to a feature launch; lifetime SKU priced to convert price-sensitive users; Meta + TikTok short-form "turn your phone into a scanner" demos.

Sources: https://apps.apple.com/us/app/scanguru-pdf-scanner-app/id1040149161 , https://mwm.ai/apps/scanguru-document-pdf-scanner/1040149161 , https://trendapps.dev/app/ios/1040149161/ , https://appshunter.io/ios/app/scanguru-pdf-scanner-app/id1040149161 , https://adapty.io/paywall-library/scanguru/ , https://universeapps.limited/scanguru/privacy.html , https://www.complaintsboard.com/scanguru-b148647 , https://scroll.media/2025/06/27/universe-group-istoriia/

### 4.5 Scanner Pro — OCR Scanning & Fax (Readdle, id 333710667)

| Field | Value |
|---|---|
| Title / subtitle | Rotates: "Scanner Pro: OCR Scanning & Fax", "Scanner Pro - Scan to PDF", "Scanner Pro・Scan PDF Documents"; subtitles "OCR Scan, Fax, & PDF Converter" / "Sign, Convert & Send Documents" |
| Category, rating | Business (#126 Business free); 4.9 stars, ~336K US ratings, 914K worldwide; released 2009 |
| Developer | Readdle (Ukraine, bootstrapped, ~$36M ARR across all apps per GetLatka estimate) |
| Est. iOS last month | ~50K downloads, ~$200K revenue |
| Free tier | Unlimited scans, iCloud sync, **watermark on every export**; no OCR, no auto-upload, no workflows |
| Paid SKUs seen | Scanner Pro Plus **$19.99/year** (cheapest annual among major scanners), $29.99 and $59.99 yearly variants, $6.99–$7.99 monthly, no weekly, no lifetime; add-ons: Fax Pack $0.99, Expense Report $4.99 |
| Trial / paywall | 7-day trial on annual; 50%-off spring sale in 2025; soft paywall |
| Privacy | All OCR, translation and neural enhancement on-device; no Readdle account required |
| Paid UA | None found; editorial/PR-led (Apple award history, sponsor posts); cross-promotion inside Spark / Documents / PDF Expert |
| Review themes | 1-star: watermark re-applied after an update, legacy pay-once buyers "stripped of features", broken restore purchase, crashes after 2026 updates. 5-star: "still the best scanner", OCR quality, privacy |

**Strengths:** brand trust, on-device privacy story, the cheapest annual, deep pro features (fax, expense reports, workflows, measure, translate).

**Attackable gaps:** tiny paid-UA footprint, so "scanner pro", "ocr scanner" and "fax" keywords are winnable; unsettled ASO (three titles in a year); legacy-user backlash; watermark on free exports; no AI assistant, no weekly or lifetime SKU.

**Copy:** a free tier that lets people scan and share before paying; on-device privacy as a headline in screenshots; $19.99 annual anchor with 7-day trial plus seasonal 50% promos; consumable add-ons (fax, expense report) outside the subscription; engineering blog posts about scan quality as PR.

Sources: https://apps.apple.com/us/app/scanner-pro-scan-to-pdf/id333710667 , https://support.readdle.com/scannerpro/billing-subscription/use-scanner-pro-for-free-or-subscribe , https://readdle.com/blog/scanner-pro-8-alex-letter , https://readdle.com/blog/why-scanner-pro-scans-look-better-than-ever , https://app.sensortower.com/ios/us/readdle-inc/app/scanner-pro-pdf-scanner-app/333710667/ , https://verifiedappreviews.com/app/scanner-pro/

### 4.6 Also on the radar

| App | Why it matters |
|---|---|
| Genius Scan (Grizzly Labs) | ~$300K/month, 1.3M ratings at 4.9, 100% offline / on-device; Plus $9.99/yr, Ultra $39.99/yr. The "quality + privacy" reference brand. |
| Scan Shot | ~$700–800K/month on 20–70K downloads: $0.99 7-day trial then $6.99/week. Pure paid-UA play; will be in the same auctions. |
| TapScanner | 300M downloads claimed, Android-heavy; 10 free credits then card; $4.99/week. |
| Tiny Scanner | $500–600K/month on ~20K downloads: almost entirely renewals from a 2013 install base. |
| SwiftScan (Maple Media / Skybound) | $5.99–9.99/month, $34.99–59.99/year, $59.99 lifetime; low volume. |
| iOS Notes / Files, Google Drive | Free built-ins; cannot export OCR text, JPG batches or DOCX, no folders or password PDFs. Position against them on what they cannot do. |

---

## 5. Comparison matrix

| | CamScanner | iScanner | Adobe Scan | ScanGuru | Scanner Pro | **Doc Scanner (proposed)** |
|---|---|---|---|---|---|---|
| Free scans | Yes, watermark + ads | Effectively no | Yes, no watermark | Capped, ads | Yes, watermark | **Unlimited, no watermark, no ads** |
| Account required | For cloud | For cloud | **Yes, always** | No | No | **No** |
| OCR location | Cloud | Mixed (Edge Repair on-device) | Cloud | Cloud | **On-device** | **On-device (Apple Vision)** |
| Weekly SKU | $4.99 | $3.99–4.99 | None | $6.99 | None | $4.99 (secondary) |
| Annual SKU | $49.99 ($35.99 yr 1) | $19.99–20.99 | $59.99–69.99 | $69.99 | $19.99 | **$29.99, 7-day trial** |
| Lifetime | No | Off-store $39.99 | No | $59.99 | No | $49.99 (seasonal) |
| Trial | 3-day | 3-day, toggle off | 7-day (annual) | 7-day | 7-day | 7-day (annual) |
| Paywall | Soft | Hard | Soft | Hard-ish | Soft | **Soft, value-first** |
| AI features | Many (cloud) | Many + on-device | Assistant w/ citations | Translate | On-device translate | On-device summarise / table extract (roadmap) |
| Paid UA intensity | High (Apple Ads + CPP) | High (social + paywall) | Low | High (Meta/TikTok) | Low | Apple Ads first |
| Loudest complaint | Trust, watermark | Hard paywall, billing | Forced account/cloud | Weekly trap | Watermark, legacy | — |

---

## 6. Positioning, offer and paywall for Doc Scanner

### 6.1 Positioning statement

> **Doc Scanner: the honest scanner.** Unlimited scans to clean PDF, free, no watermark, no account, nothing leaves your phone. Pay only when you need OCR text export, Word/Excel export, signatures and folders.

Three proof points, each aimed at a named competitor weakness:

1. **"No watermark. Ever."** (vs CamScanner, Scanner Pro, iScanner free tiers) — the number-one Reddit concern in the category.
2. **"No sign-up. No cloud. On-device OCR."** (vs Adobe Scan's forced Adobe ID, CamScanner's trust history, iScanner's cloud SKUs).
3. **"$29.99 a year, shown up front. No weekly surprise."** (vs ScanGuru $6.99/week and iScanner's trial-toggle complaints). Note: price claims are **not allowed in Apple Ads assets** (icon, name, subtitle, CPP screenshots); the price promise lives in the Promoted IAP display name, the paywall, and Meta/TikTok creative.

### 6.2 SKU ladder (StoreKit, one subscription group)

| SKU | Price | Intro offer | Role |
|---|---|---|---|
| **Annual (default-selected)** | $29.99/year | 7-day free trial | Core offer; sits between Scanner Pro ($19.99) and CamScanner ($49.99); below Adobe and ScanGuru. |
| Weekly | $4.99/week | None | Impulse / one-off paperwork need; matches CamScanner and iScanner; it is where 55–74% of category revenue comes from, so it must exist, but it is never the only visible plan. |
| Monthly | $7.99/month | None | Optional; Productivity revenue skews monthly (77%) per RevenueCat, so test it in month 2. |
| Lifetime (non-consumable) | $49.99 | — | Promote only in tax season and via offer codes / deal sites, following iScanner's StackSocial playbook. Priced below ScanGuru's $59.99. |
| Add-on consumable (later) | Fax pack $0.99–1.99 | — | Copy Scanner Pro's micro-upsell model once fax exists. |

Enrol in the **App Store Small Business Program** (15% commission from day one) if annual proceeds are under $1M. Implement **App Store Server Notifications V2** (V1 is deprecated for new apps).

### 6.3 Paywall rules

- Soft paywall after a 3-screen onboarding (scan → auto-crop → share), shown once, then triggered contextually at OCR export, Word/Excel export, signature, and folder creation.
- Annual pre-selected with the full renewal price ("$29.99/year after 7-day free trial") as the most prominent text, per Guideline 3.1.2 and Apple's subscription page; per-week breakdowns subordinate. This is what gets hard-paywall apps rejected and what earns iScanner its "scam" reviews.
- Trial toggle visible and **on** by default (RevenueCat: trials add +85% LTV in Utilities); add a "we'll remind you 2 days before your trial ends" line and actually send the local notification. This is a differentiator against every competitor above.
- Restore Purchases, Terms and Privacy links on the paywall.
- Configure **Win-back offers** (iOS 18+, Apple surfaces them automatically) and **Promotional offers** for lapsed annual users after month 1 (35% of annual cancels happen then).

---

## 7. The IAP campaign plan

### 7.1 Goals and KPIs

| Funnel step | Benchmark | Target (month 1 test) | Target (scaled) |
|---|---|---|---|
| Tap-through rate (TTR) | 9–11% | ≥ 8% | ≥ 10% |
| Conversion rate tap→install (CR) | 60–66% | ≥ 55% | ≥ 62% |
| Cost per install (category terms) | $2.25–$3.75 | ≤ $3.25 | ≤ $2.75 |
| Cost per install (brand / exact long-tail) | — | ≤ $1.50 | ≤ $1.25 |
| Install → trial start | 6.5–10.9% | ≥ 9% | ≥ 12% |
| Trial → paid (day 14) | 25.6% global | ≥ 30% | ≥ 35% |
| Install → paid (trial + direct) | 4.2–5.4% | ≥ 4.5% | ≥ 6% |
| Cost per paying subscriber | $45–75 | ≤ $70 | ≤ $55 |
| Day-30 ROAS (net proceeds) | — | ≥ 30% | ≥ 40% |
| Projected 12-month ROAS | — | ≥ 100% | ≥ 130% |
| Refund rate | 2–5% | ≤ 5% | ≤ 3% |

Reference LTV: $68.90 12-month LTV for a Utilities trial subscriber (RevenueCat 2026). At $55 cost per payer that is a 125% 12-month ROAS before organic uplift from chart movement.

### 7.2 Pre-launch checklist (1–2 weeks)

**App Store Connect**
- [ ] Final title / subtitle (Section 2); keyword field: `scanner,scan,pdf,document,ocr,receipt,id card,sign,photo to pdf,text,converter,fax,free` (100 chars, no spaces after commas, no words already in title/subtitle).
- [ ] **Promoted In-App Purchases** (up to 20; order matters): 1) Annual "Doc Scanner Pro (1 Year)", 2) Lifetime "Doc Scanner Pro Lifetime", 3) Weekly "Doc Scanner Pro (1 Week)". Display name ≤ 30 chars, description ≤ 45 chars, image 1024×1024 PNG/JPEG, flattened, no rounded corners. Implement StoreKit 2 `PurchaseIntent` (iOS 16.4+) so a purchase started on the App Store completes in-app. Eligible users then see the intro offer on your product page. Source: https://developer.apple.com/app-store/promoting-in-app-purchases/
- [ ] **Introductory offer:** 7-day free trial on Annual.
- [ ] **Custom Product Pages** (six, each with its own screenshot set and promotional text; deep link each to the matching feature on iOS 18+):

| CPP | First screenshot message | Used by ad group(s) |
|---|---|---|
| CPP-1 Scan to PDF (hero) | "Scan anything to a clean PDF in one tap" | Category generic, Brand |
| CPP-2 OCR / text | "Turn paper into editable text, on your phone" | ocr, image to text, text scanner, scan to word |
| CPP-3 Honest scanner | "No watermark. No sign-up. Nothing leaves your phone." | Competitor: camscanner, iscanner, scanguru, scan shot, tap scanner |
| CPP-4 Lens alternative | "Scan to Word, PDF and photos — the simple way" | microsoft lens, office lens, lens scanner, adobe scan |
| CPP-5 Receipts and IDs | "Receipts, ID cards and passports, perfectly cropped" | receipt scanner, id scanner, passport scanner, scan receipts |
| CPP-6 Sign and send | "Sign, fill and share PDFs without printing" | sign pdf, scan and sign, fill form, fax |

- [ ] **In-App Event** tied to a real feature launch (Apple rejects pure price promotions): e.g. "On-device OCR 2.0" as a Major Update, scheduled for mid-January.
- [ ] Localise US English first; add UK, CA, AU storefront copies later (same language, separate Apple Ads campaigns).

**Measurement (Section 7.3)**
- [ ] AdServices attribution token call on first launch, retried 3 times at 5-second intervals, forwarded to RevenueCat or Adapty.
- [ ] App Store Server Notifications V2 → RevenueCat/Adapty → your analytics (trial start, conversion, renewal, refund, grace period).
- [ ] SKAdNetwork 4 / AdAttributionKit conversion schema registered (needed for Meta/TikTok later and as an aggregated cross-check for Apple Ads on iOS 26.2+).
- [ ] Apple Ads Advanced account; link App Store Connect; verify the $100 new-account credit if offered.

### 7.3 Measurement architecture: how an IAP is attributed to a keyword

1. **Deterministic path (Apple Ads only, no ATT prompt needed):** app calls `AAAttribution.attributionToken()` → token (24-hour TTL) is POSTed to `https://api-adservices.apple.com/api/v1/` → returns campaign, ad group, keyword and CPP IDs → stored on the RevenueCat/Adapty customer record → joined to StoreKit 2 transactions and Server Notifications → cohort revenue by keyword for as long as the subscriber lives. This is the only major channel that gives a small advertiser "keyword → trial → paid → renewal" per cohort. Sources: https://developer.apple.com/documentation/adservices , https://www.revenuecat.com/docs/integrations/attribution/apple-search-ads , https://adapty.io/docs/apple-search-ads
2. **Aggregated path (all channels):** SKAN 4 / AdAttributionKit postbacks. Recommended conversion-value schema for a subscription scanner app:
   - Window 1 (days 0–2), fine values: onboarding complete (5), first scan (10), paywall viewed (20), **trial started (45, coarse = medium)**, **direct paid (63, coarse = high)**. Lock the window as soon as a trial starts to speed up postbacks.
   - Window 2 (days 3–7), coarse: low = still trialing, medium = converted to weekly/monthly, high = converted to annual.
   - Window 3 (days 8–35), coarse: high = first renewal with no refund.
   - Fine values are usually withheld at indie volumes (crowd anonymity needs ~20 installs/campaign/day), so weekly vs annual must be separable with coarse tiers.
3. **Reporting cadence:** daily spend / taps / installs from Apple Ads; weekly cohort table by campaign → ad group → keyword → CPP with installs, trials, paid, net proceeds, D7/D30 ROAS from RevenueCat; monthly LTV curve update.

### 7.4 Channel 1: Apple Ads Advanced (months 1–3, 100% of test budget)

**Placement:** Search results only to start (CR 60–66%). Add Search tab in month 2 for brand reach; skip Today tab and product-page placements until install-to-paid is proven (Today tab TTR is 1–3%).

**Bidding:** CPT with max bids 20–30% above Apple's suggested bid for the first ~1,000 taps, then tighten. Daily budget ≥ 5× target CPA. Switch the Category campaign to **Maximize Conversions** with a target CPA once it has ≥ 2 weeks and ≥ 50 installs/week of history.

**Campaign structure (US storefront, iPhone + iPad, all ages):**

| Campaign | Match | Daily budget (test → scale) | Keywords (starter list) | Negatives | CPP |
|---|---|---|---|---|---|
| **DS-US-Brand** | Exact | $10 → $20 | doc scanner, doc scanner app, doc scanner pdf, docscanner, doc scan ocr, doc scanner pdf scan ocr | — | CPP-1 |
| **DS-US-Category-Core** | Exact | $45 → $200 | scanner app, pdf scanner, document scanner, scan to pdf, scanner, scan documents, doc scanner free, pdf scanner app, document scanner app, scan app, scan pdf, photo to pdf, mobile scanner, camera scanner, paper scanner, scan documents to pdf, free scanner app, scanner app free, pdf scan | brand terms, competitor names | CPP-1 |
| **DS-US-Category-OCR** | Exact | $15 → $60 | ocr, ocr scanner, image to text, text scanner, scan to text, scan to word, photo to text, pdf to word, handwriting to text, text recognition | — | CPP-2 |
| **DS-US-Category-Niches** | Exact | $10 → $50 | receipt scanner, scan receipts, id scanner, id card scanner, passport scanner, business card scanner, sign pdf, scan and sign, fill pdf, fax app, send fax, book scanner | — | CPP-5 / CPP-6 |
| **DS-US-Competitor** | Exact | $15 → $80 | camscanner, cam scanner, cam scanner app, iscanner, i scanner, scanner pro, adobe scan, scanguru, scan guru, genius scan, tiny scanner, swiftscan, tap scanner, tapscanner, scan shot, turboscan, scanbot, microsoft lens, office lens, lens scanner | — | CPP-3 (CPP-4 for lens/adobe) |
| **DS-US-Discovery** | Broad + Search Match | $5 → $40 | scanner app, pdf scanner, document scanner, scan to pdf, ocr scanner (broad) | all exact keywords above as exact negatives; plus qr, qr code, barcode, police scanner, radio scanner, photo scanner, negative scanner, film, 3d scanner, virus, malware, wifi, bluetooth, body, nfc, label | CPP-1 |

Total test budget: **$100/day (~$3,000/month)**. Scale budget: **$450/day (~$13,500/month)**.

**Competitor campaign rules:** Apple allows bidding on competitor names; do not use their names in your metadata or CPP assets. Expect CPT on "camscanner" and "iscanner" to be high (both defend their brand; both are also squatted by clones). Expect "adobe scan", "scanner pro", "microsoft lens" and "office lens" to be cheap because those owners barely run Apple Ads. Cap competitor CPT at 1.2× your category CPT and judge on cost per trial, not CPI.

**Weekly optimisation loop:**
1. Move any Discovery search term with ≥ 2 installs into the matching exact campaign; add every irrelevant term as a negative.
2. Pause keywords with ≥ 150 taps and 0 trials; raise bids 10–15% on keywords with cost per trial under target; lower 10–15% where above target.
3. Rotate CPP ad variations: keep the best-TTR variation, replace the worst screenshot set every 2 weeks.
4. Check Search Term Rank report (the only reliable popularity signal since the 2025-09-29 collapse) for new terms.

### 7.5 Channel 2: Meta Advantage+ app campaigns (month 3+, after Apple Ads proves install-to-paid ≥ 5%)

- Objective App promotion, iOS 14.5+ campaign, **App Event Optimization on "trial started"** (needs ≥ 50 events per ad set per week to leave learning). Value Optimization on "subscription paid" needs volume you will not have before month 4–6.
- Enable Aggregated Event Measurement for the App promotion objective (campaign-level reporting without a SKAN schema) and run SKAN/AAK in parallel.
- Creative: 9:16 UGC-style demos under 15 seconds. Hooks that match review-mined pain: "Stop paying $7 a week to scan a receipt", "The scanner app that doesn't watermark your documents", "No account, no cloud: your tax docs stay on your phone", "Microsoft Lens is gone. Here's what to use." Price claims are fine on Meta.
- Budget: start $50/day, three ad sets (broad US 25–54, lookalike of trial starters once ≥ 1,000, interest stack: small business, freelancers, students, tax prep).

### 7.6 Channel 3: TikTok (month 4+, optional)

iOS app promotion with real-time conversion reporting via an MMP (AppsFlyer, Adjust, Branch, Singular, Kochava) or TikTok App Events SDK ≥ 1.5.0; optimise toward trial start; wait an extra ~72 hours for SKAN postbacks before judging. Lean on the humour format iScanner uses (paperwork disaster → scan → done).

### 7.7 Creative plan (all channels)

| Hook | Targets whose weakness | Format |
|---|---|---|
| "No watermark. Ever. Even on the free plan." | CamScanner, Scanner Pro, iScanner | Screenshot 1 on CPP-3; 6-second video |
| "No sign-up. Your documents never leave your phone." | Adobe Scan, CamScanner | Screenshot 2 on CPP-3; privacy badge on CPP-1 |
| "$29.99 a year. Not $6.99 a week." | ScanGuru, iScanner, Scan Shot | Meta/TikTok only (not allowed in Apple Ads assets) |
| "Scan → editable Word text in 3 seconds, offline" | Adobe (paywalled export), ScanGuru (bad OCR) | CPP-2 hero; video |
| "Microsoft Lens is gone. Doc Scanner saves to Word, PDF and Photos." | Orphaned Lens users | CPP-4; Meta interest: Microsoft 365 users |
| "Receipts and IDs cropped perfectly, every time" | Generic; tax season | CPP-5; seasonal |
| "Scan, sign, send — without a printer" | Generic; back-to-school and tax forms | CPP-6 |

Screenshot rules for Apple Ads: no price, offer, rank or award text in icon, name, subtitle or CPP assets; CPP language and device must match campaign targeting or the variation will not serve.

### 7.8 Budget and unit-economics model

Assumptions: CPT $1.80, CR 62%, install-to-trial 10%, trial-to-paid 30%, direct-to-paid 1% of installs, net proceeds after 15% commission, blended first-year net proceeds per payer ≈ $27 (60% weekly at ~6 paid weeks, 40% annual), 12-month LTV benchmark $68.90 for trial subscribers.

| Monthly spend | Taps | Installs | CPI | Trials | Payers | Cost / payer | Month-1 net revenue | 12-month projected ROAS |
|---|---|---|---|---|---|---|---|---|
| $3,000 (test) | 1,667 | 1,033 | $2.90 | 103 | 41 | $73 | ~$1,100 | ~95% |
| $7,500 | 4,167 | 2,583 | $2.90 | 258 | 103 | $73 | ~$2,800 | ~95% |
| $13,500 (scaled, CPT $1.50 via CPP + exact) | 9,000 | 5,580 | $2.42 | 670 (12%) | 290 (~5.2%) | $47 | ~$7,800 | ~150% |

Reading: at benchmark averages the campaign is roughly break-even at 12 months. It becomes clearly profitable only when CPP-driven CPT drops toward $1.50 **and** install-to-paid rises above 6%. Those two levers, not spend, are the month-1 job. Brand and long-tail exact terms will beat these averages; broad category terms will be worse.

### 7.9 Timeline

| Phase | When | What |
|---|---|---|
| 0. Prep | Weeks 1–2 (Oct 2026) | Title/subtitle, SKU ladder, paywall, Promoted IAPs, 6 CPPs, attribution, SKAN schema, Apple Ads account |
| 1. Test | Weeks 3–6 | Apple Ads at $100/day across the six campaigns; weekly optimisation loop; first cohort D14 trial-to-paid read |
| 2. Optimise | Weeks 7–10 | Cut to the top 40 keywords and best 3 CPPs; switch Category-Core to Maximize Conversions; test Monthly SKU and trial length (7 vs 14 days) |
| 3. Scale for tax season | Mid-Jan to Apr 15 2027 | Raise to $300–450/day; schedule In-App Event (feature launch) and Lifetime promotion via offer codes; add Meta AEO at $50–100/day |
| 4. Expand | May–Jun 2027 | UK / CA / AU Apple Ads copies of the winning campaigns; TikTok test; Win-back offers for month-1 annual cancels |
| 5. Back-to-school | Aug–Sep 2027 | Second scale window; student-angle CPP and creative |

### 7.10 Risks and compliance

- **Guideline 3.1.2 rejection** if "free trial" is more prominent than the billed price: keep the renewal price as the largest text on the paywall.
- **Trademark complaints** if competitor names appear in metadata or CPP assets: bid on them, never display them.
- **Low SKAN volume**: under ~20 installs/campaign/day you will receive null conversion values; rely on AdServices for Apple Ads and do not launch Meta until Apple Ads volume is stable.
- **Apple Ads multiple ad slots** may lower average ad position and CR versus 2025 benchmarks; judge on cost per trial.
- **Clone / squat risk**: your "doc scanner" brand term already has four lookalike apps; the Brand campaign exists to defend it cheaply.
- **Epic v. Apple link-out option**: tempting (0% commission in the US today) but it breaks Promoted IAPs, intro offers, win-back and keyword-level attribution; revisit only after the Supreme Court outcome.

---

## 8. What to pull from Sensor Tower (you have it open; these fill the gaps)

For each of CamScanner (388627783), iScanner (1040093707), Adobe Scan (1199564834), ScanGuru (1040149161), Scanner Pro (333710667), plus Scan Shot (1575194801) and Genius Scan (377672876):

1. **App Analysis → Downloads & Revenue**, iOS, **United States**, monthly, last 24 months. Replaces the undated worldwide snippets in Section 3.1 and gives the tax-season curve (look at Jan–Apr 2025 and 2026).
2. **Category Rankings history**, US iPhone, Business and Productivity, Top Grossing and Top Free, last 12 months.
3. **Keyword Rankings (US)**: top ranked keywords per app with traffic score; export the full set and intersect with the keyword lists in Section 7.4.
4. **Search Ads Intelligence**: for the keywords *scanner app, pdf scanner, document scanner, scan to pdf, ocr scanner, cam scanner, scanner* pull Share of Voice and the advertiser list. This answers "who actually bids on these terms", which no public source states.
5. **Ad Intelligence → Creatives**: top Meta / TikTok / Apple Ads creatives for ScanGuru, iScanner, CamScanner and Scan Shot (networks, formats, first seen, share of impressions). Use for the creative plan in 7.7.
6. **In-App Purchases / Pricing history**: confirm current US SKUs and price tests for CamScanner (two conflicting annual prices) and Scan Shot (not found).
7. **Reviews → Review Analysis**, US, last 180 days, filter 1–2 stars, for "subscription", "trial", "watermark", "cancel", "charged".
8. **Usage Intelligence** (if in your plan): DAU/MAU, retention D1/D7/D30 for iScanner and ScanGuru as the hard-paywall benchmark.
9. For **your app (6759896516)**: Keyword Rankings and Search Ads SoV baseline now, so the campaign's organic uplift can be measured later.

---

## 9. Confidence notes

- **Confirmed from listing or vendor text:** titles, developers, categories, star ratings and rating counts, IAP SKU names and prices as listed, trial rules (Adobe 7-day annual only, Scanner Pro $19.99/yr + 7-day, ScanGuru 7-day/$6.99/wk/$69.99/$59.99, iScanner SKU list), Microsoft Lens retirement dates, Apple Ads product facts (placements, multiple slots date, Maximize Conversions date, CPP limit 70, Promoted IAP specs), Epic v. Apple timeline through 2025-12-11.
- **Third-party estimates:** every download and revenue number (Sensor Tower public snippets, mwm.ai, trendapps, ScreensDesign, PaywallScreens) and all chart ranks; most lack a stated month and US-vs-worldwide scope.
- **Conflicting:** CamScanner current annual price ($49.99 with $35.99 intro vs $39.99 with $29.99 intro); CamScanner free cloud (200 MB vs 1 GB); Adobe free OCR cap (25 vs 5 pages); ScanGuru download estimates (150K–500K); Scanner Pro monthly SKU period labels.
- **Not found:** your app's release date, SKUs, prices and rating; keyword-level CPT for scanner terms; which competitors bid on which Apple Ads terms; Meta/TikTok creative specifics; US-only revenue splits; Scan Shot pricing.
- **Inference:** the ~Q4-2025 release estimate for id 6759896516 is from neighbouring App Store IDs, not a source.

## 10. Key sources

Benchmarks: https://www.revenuecat.com/state-of-subscription-apps , https://www.revenuecat.com/state-of-subscription-apps-2026-utilities , https://www.revenuecat.com/state-of-subscription-apps-2025 , https://adapty.io/state-of-in-app-subscriptions/ , https://adapty.io/blog/apple-ads-benchmarks-2026/ , https://adapty.io/blog/apple-ads-benchmarks-by-niche/ , https://adapty.io/blog/apple-ads-install-to-paid-rate-benchmarks/ , https://www.apptweak.com/en/aso-blog/apple-ads-benchmarks , https://splitmetrics.com/apple-ads-search-results-benchmarks-2026/ , https://www.mobileaction.co/report/apple-ads-2026-benchmark-report/ad-variations-using-custom-product-pages/

Apple: https://ads.apple.com/app-store/best-practices/campaign-structure , https://ads.apple.com/app-store/help/campaigns/0095-maximize-conversions , https://ads.apple.com/app-store/help/ads/0077-create-ad-variations , https://developer.apple.com/app-store/promoting-in-app-purchases/ , https://developer.apple.com/app-store/custom-product-pages/ , https://developer.apple.com/app-store/in-app-events/ , https://developer.apple.com/app-store/subscriptions/ , https://developer.apple.com/documentation/adservices , https://developer.apple.com/documentation/adattributionkit , https://developer.apple.com/documentation/appstoreservernotifications , https://developer.apple.com/app-store/review/guidelines/#3.1.2

Market and news: https://sensortower.com/blog/state-of-mobile-2026 , https://9to5mac.com/2026/01/22/app-store-search-ads-more-ads-march/ , https://aso.dev/blog/apple-ads-popularity-massive-drop/ , https://techcrunch.com/2025/08/08/rip-microsoft-lens-a-simple-little-app-thats-getting-replaced-by-ai/ , https://wildandfreetools.com/blog/best-document-scanner-app-reddit-2026/ , https://scanlens.io/best-scanner-apps-iphone , https://www.revenuecat.com/docs/integrations/attribution/apple-search-ads , https://help.branch.io/marketer-hub/docs/meta-aggregated-event-measurement , https://support.google.com/google-ads/answer/10625151 , https://ads.tiktok.com/help/article/about-ios-real-time-conversion-reporting

Competitor-specific sources are listed under each app in Section 4.
