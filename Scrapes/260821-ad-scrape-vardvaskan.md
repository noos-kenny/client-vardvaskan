# Ad Scrape — Vårdväskan (Meta)

> Descriptive scrape of the brand's Meta Ad Library presence. This file records what the brand is doing (facts, verbatim quotes, dates) as a foundation for later creative and strategic audits. Evaluation and recommendations belong in Audits/, not here.

## 1. Scrape metadata

- **Data sources:** Motion MCP (Creative Analytics) only. Motion has no workspace/ad-account connection for Vårdväskan, so its own creative insights (`get_creative_insights`, with real performance metrics) were not available — the brand is only accessible as an **Inspo brand** (`get_inspo_creatives`), i.e. Ad-Library-mirrored data with no spend/impressions/hook-rate figures. This scrape is therefore **volume/creative-content only, no performance data**, even though the brand being scraped is the client itself.
- **Meta Ad Library browser fallback/complement:** not run this pass — the Claude in Chrome browser extension was not connected in this session. This means Page-level totals ("~X results" from the Library UI itself), EU transparency/demographic data, and "multiple versions"/"X ads use this creative and text" duplication signals were **not captured**. See §10.
- **Brand / Page name:** Vårdväskan (Motion brand match, `brandId` 66f87c1aaa0d5e9098fac6a6). Industry per Motion: Medical / Healthcare Professional Bags.
- **Page ID:** 101120089975936 — confirmed identical to the `view_all_page_id` in the source URL supplied by the user, and to the `platformId` on Motion's brand record.
- **Source URL supplied by user:** `https://www.facebook.com/ads/library/?active_status=all&ad_type=all&country=SE&is_targeted_country=false&media_type=all&search_type=page&sort_data[direction]=desc&sort_data[mode]=total_impressions&view_all_page_id=101120089975936`
- **Motion follower counts (as of pull):** Facebook 150,947 · Instagram 24,161 (@vardvaskan) · combined 175,108.
- **Motion library totals (as of 2026-08-20T17:18 per Motion metadata):** 2,525 creatives all-time · 118 currently active (50 image, 64 video, 4 carousel, 0 unknown per Motion's own bucketing).
- **Scrape date/time:** 2026-08-21, ~08:20–08:30 UTC.
- **Method and sample:**
  - Pull 1 — `get_inspo_creatives(status=ACTIVE, sort=NEWEST, limit=150)` → returned all **118 active creatives** (complete active set; 54 tagged `image`, 64 tagged `video` in the per-asset format field — see format-mix note in §3 on the image/carousel discrepancy).
  - Pull 2 — `get_inspo_creatives(status=ACTIVE_AND_INACTIVE, sort=NEWEST, limit=300)` → newest 300 creatives regardless of status (97 active + 203 inactive in this window), spanning launch dates 2026-05-13 to 2026-08-17. Used for inactive/historical themes (§9); not the full inactive history (2,525 − 118 ≈ 2,407 inactive creatives exist, of which only 203 were sampled here).
  - `withGlossary: true` was requested on both pulls; Motion returned an empty glossary array for every creative, so taxonomy tags are **not available** for this brand.
  - Video analysis — `get_creative_transcript` run on 10 videos (5 longest-running active + 5 newest active); `get_creative_summary` run on 3 of those as a follow-up when transcript audio was absent or non-verbal. See §4b.
- **Regional sister views:** not checked — no browser pass this run (§10).

## 2. Volume & activity

- **Total creatives (all-time, per Motion):** 2,525.
- **Active creatives:** 118 (per both Motion's brand metadata and the direct active pull — the two numbers agree).
- **Oldest still-active ad:** started **2026-05-13**, ~98 days running as of this scrape. Five ads (3 video, 2 image/video variants) all launched within the same 2026-05-13 to 2026-05-15 window and are all still active — a distinct launch wave rather than a single ad. All five sit around "bästsäljare" (bestseller) and product-hero messaging (see below).
- **Launch clustering in the sampled newest-300 window (2026-05-13 → 2026-08-17):** visible waves around mid-May (bestseller/hero push, 5+ ads), early August (Back-to-Work campaign, 7+ ads across the wave), and a steady trickle of nametag ("Namnskyltar") and compression-sock ("Stödstrumpor") ads throughout.
- **Long-runners (almost certainly proven performers, not confirmed by spend data):**
  - "Kitta dig från topp till tå" (video, started 2026-05-13/14, ~97–98 days active) — bestseller "kit yourself head to toe" framing.
  - "Vårdens favoriter 🌟" (image, started 2026-05-13, 98 days active) — bestseller compression-sock framing.
  - "Upptäck favoriten Beez Remedy" (video, started 2026-05-13, 97 days active) — private-label shoe hero.
  - "Slipp värken på passet" (video, started 2026-05-15, 96 days active) — compression-sock pain-point framing.
  - "Din egen stil - även på jobbet" (video, started 2026-05-13, 96 days active) — personal-style/self-expression framing, UGC-styled.

## 3. Format mix

- **Motion's own bucketing (active set):** 50 image, 64 video, 4 carousel, 0 unknown = 118.
- **Per-asset format field on the same 118 creatives:** 54 tagged `image`, 64 tagged `video`, 0 tagged `carousel` — the 4 carousel ads are most likely represented in the per-asset feed as individual `image` cards rather than as a single carousel unit, which would reconcile the two counts (50 + 4 ≈ 54). Not independently verified without a browser pass on the Library UI.
- Video is roughly on par with static (64 vs 50–54) among currently active ads — this brand runs video at real volume, not as an occasional format.
- **Production level:** mixed. Some clearly polished/product-shot content (hero shoe and sock shots, bundle/kit flat-lays); some UGC-styled talking-to-camera pieces (e.g. "Din egen stil", the nurse-testimonial pen video); some silent, text/graphic-overlay driven pieces (see §4b — several videos have no speech at all).
- **CTA distribution across the 118 active ads:** "Shop now"/"Shop Now" 67 (44+23, case varies), "Learn More"/"Learn more" 46 (28+18, case varies), "Subscribe" 3, "Buy now" 2. Shop-now and Learn-more are roughly balanced overall, i.e. a mix of direct-response and softer/traffic-style CTAs.
- Destination types include a number of Meta Canvas/Instant Experience links (`fb.com/canvas_doc/...`) alongside direct site links — see §7.
- "Multiple versions"/duplication-across-ad-sets signals: not available from Motion's Inspo feed; would require the Ad Library browser view (§10).

## 4. Hooks & copy (verbatim)

All quotes below are exact primary-copy text as returned by Motion (which mirrors the Ad Library), including emoji. Status = active unless marked inactive; period = launch date → scrape date (i.e. days active) where known.

1. "Shoppa skor och sandaler - nu med upp till 40% rabatt! Uppdatera skogarderoben för jobb och fritid." — image/video, active, appears on 8 active creatives, newest launched 2026-08-17.
2. "Nya favoriter är här! Uppdatera din arbetslook med våra senaste plagg och accessoarer." — active, 8 creatives.
3. "Kickstarta hösten med grymma deals från vår Back to Work kampanj - upp till 40% rabatt!" — active, 7 creatives, part of the early-August Back to Work wave.
4. "Sätt en färgglad touch på arbetsklädseln med stödstrumpor i premiumkvalitet. Upp till 30% rabatt!" — active, 5 creatives.
5. "Ta med din personliga stil till jobbet och - be YOU at work! 🌸" — active, 5 creatives.
6. "Endast fantastin sätter gränser - designa din egen unika namnskylt! Just nu - 20% rabatt!" — active, 5 creatives (2 image, 3 video), oldest launched 2026-08-04, still running. **Note: "fantastin" — see flag in §10.**
7. "Upptäck färdiga kit som matchar och kittar dig från topp till tå – redo för arbetsdagen." — active, 5 creatives.
8. "Sommarvibbar på jobbet! Matcha strumpor och tillbehör i somriga mönster. 🍉🍦" — active, 5 creatives.
9. "\"Som att gå på moln\" - se varför tusentals vårdhjältar väljer Remedy sneakers." — video, active, 97 days running (since 2026-05-13). Private-label (Beez Remedy) social-proof framing.
10. "Tusentals vårdhjältar kan inte ha fel... Våra stödstrumpor räddar benen (och humöret) varje dag! 🌸" — image, active, 98 days running.
11. "Är du den enda som har trötta ben och ont i fötterna? 🦶Jämna ut oddsen med våra stödstrumpor!" — video, active, 96 days running. Direct pain-point question hook.
12. "Vård-Sveriges favoriter! Kitta dig från topp till tå med våra bästsäljare." — video, active, 97–98 days running (two creative variants).
13. "Förenkla klinikens inköp. Skapa företagskonto och få 10% på första ordern." — active, 3 creatives. B2B/company-account offer.
14. "Prenumerera på vårt nyhetsbrev och få 15% rabatt på ditt första köp hos Vårdväskan." — active, 3 creatives (2 of which point to a broken landing page — see §10).
15. "Vi står upp för er som står upp för andra - varje dag! 🩺" — active, 2 creatives. Brand-values framing.
16. "Oslagbar kvalitet, prestanda och funktionalitet - upp till 20% rabatt på alla Littmann stetoskop!" — active, 2 creatives. Distributed-brand (3M Littmann) push.
17. "Dina kollegors hemliga vapen. 🤫 Rätt tryck på vaden ger energi till sista timmen av passet!" — active, 2 creatives.
18. "Arshig visar hur du kan ta med din personliga stil till jobbet – be YOU at work! 🌸" — video, active, 1 creative — named-creator UGC variant of theme #5.
19. "Outfits i vården 🌸 hur ser din style ut? \n#vårdväskan #ootd" — active, 1 creative. UGC/community-style, own hashtag.
20. "Vem sa att stödstrumpor bara är för äldre, är obekväma eller fula? Inte vi! 🌸" — active, 1 creative. Objection-handling hook.

**Recurring copy elements:**
- "Vårdhjältar" ("healthcare heroes") is a repeated identity/address term across several social-proof lines (#9, #10, and inactive-set equivalents in §9).
- 🌸 is the single most repeated emoji, used consistently on lifestyle/self-expression and compression-sock copy; 🦶🩺🍉🍦🍋 appear as category-specific accents (feet/pain, medical, seasonal fruit theme).
- Rhetorical-question hooks recur on the pain-point angle ("Är du den enda som...", "Trötta ben & fötter?", inactive-set: "Vem sa att...").
- Offers are consistently framed as "upp till X% rabatt" (up to X% off) rather than flat percentages, even where the underlying discount is fixed.

**Tonality:** Swedish, informal "du" address throughout, no "ni"/formal register even on the B2B company-account copy. Voice reads as a friendly colleague/peer speaking to healthcare staff ("vårdhjältar", "dina kollegor") rather than a corporate retailer voice. Emoji use is frequent but categorized/thematic, not scattered.

**Performance per copy-variant:** not available — this requires `get_creative_insights` on the brand's own connected ad account, which does not exist in this Motion workspace. No spend/hook-rate/CTR figures exist for any of the copy above; frequency counts above are creative-count only, not performance.

## 4b. Video analysis

**Selection:** 10 of the 64 active videos were analysed — the 5 longest-running active videos (all ~96–98 days, launched 2026-05-13 to 2026-05-15) and the 5 newest active videos (launched 2026-08-04 to 2026-08-15), via `get_creative_transcript`. `get_creative_summary` was additionally run on 3 of these (1 long-runner, 2 from the newest set) to recover a hook where the transcript alone was uninformative.

**Spoken hooks, verbatim:**
- Only **one** of the 10 videos sampled had a substantive spoken hook. "Hitta stilen hos Vårdväskan" (launched 2026-08-12, active): *"Alla som jobbar inom vården vet att alla har minst en sak som de bara måste ha i sin arbetsuniform."* (0:00–0:06, per Motion's AI hook detection) — opens a first-person testimonial from what reads as a nurse/care-worker about a multi-colour pen from Vårdväskan used to colour-code patient report notes. Full transcript (Swedish, Motion's own translation in brackets): *"Alla som jobbar inom vården vet att alla har minst en sak som de bara måste ha i sin arbetsuniform. När jag tog examen så beställde jag en bläckpenna med flera olika färger från vårdväskan och den har jag använt varje dag sedan dess. [...] det som inte är rödmarkerat i mina rapportblad, det finns inte."*
- "Din egen stil - även på jobbet" (2026-05-13, active): transcript is spoken but non-lexical — *"Monday, Tuesday, Wednesday, Thursday, Friday."* is the only text Motion's transcription returned; likely a stylised/rhythmic voice-over rather than a substantive hook line.
- All other 8 sampled videos returned either no speech at all (transcription engine reported "no audio track found in file" / silence) or a failed/placeholder transcript (e.g. "Thank you.", "Bye.", a single ".").
- For "Back to Work - Upp till 40% rabatt!" (2026-08-04, active), `get_creative_summary` recovered the hook from on-screen text rather than speech: *"POV: Det är Back to work-kampanj hos Vårdväskan ✨"* — a two-person UGC-style clip of people leaving a building carrying shopping bags/boxes, per Motion's AI summary.

**Structure:** the sampled videos split into two clear patterns: (1) silent/music-only, text-overlay-driven ads where the hook is entirely visual (product shot + headline text, e.g. the "POV: Back to work" clip), and (2) a smaller set of spoken UGC-testimonial pieces (the pen-testimonial video) that open with a relatable claim about the profession before introducing the product. No talking-head "expert" or voiceover-narrator format was found in this sample — where speech exists, it is first-person/testimonial in style, not a brand narrator.

**Patterns across the videos:** the dominant pattern in this 10-video sample is that **audio is not load-bearing** — 8 of 10 had no usable speech, meaning these ads are built to work with sound off, consistent with feed/Reels viewing habits. The one substantive spoken hook opens with a broad in-group claim ("alla som jobbar inom vården vet...") before narrowing to the specific product — a relatable-claim → product structure.

**Limitations:** only 10 of 64 active videos were sampled (no performance data exists to prioritise by, so selection was by recency + tenure only, not by proven effectiveness). Silent/music-only videos may still carry a visual hook (on-screen text in the first 1–3 seconds) that this pass did not capture, since it relied on spoken transcript plus a limited number of AI summaries — image-based hook text was not OCR'd or reviewed frame-by-frame for the remaining videos.

## 5. Messaging themes

1. **Bestseller/authority framing** — "Vård-Sveriges favoriter!", "Vårdens favoriter 🌟", "Upptäck Vårdväskan". Positions the brand/product as the default choice within its category.
2. **Pain-point → product (compression socks / feet)** — "Är du den enda som har trötta ben och ont i fötterna?", "Trötta ben & fötter?", "Dina ben är ditt viktigaste arbetsredskap." Direct address of physical strain from shift work.
3. **Social proof via "vårdhjältar"** — "Tusentals vårdhjältar kan inte ha fel...", "Älskad av vårdpersonal". Peer-validation framing specific to the healthcare-worker identity.
4. **Identity / self-expression at work** — "Ta med din personliga stil till jobbet - be YOU at work! 🌸", "Lite mindre vitt. Mycket mer du. 🎨" (inactive set, §9), "Outfits i vården 🌸 hur ser din style ut?". Positions workwear as a personal-expression category, not just uniform compliance.
5. **Seasonal/thematic collections** — "Sommarvibbar på jobbet!" (fruit/summer patterns), "Nyhet! Frukttema", plus inactive-set themes (Pride, exam season) — recurring rotation of themed print collections on socks/accessories.
6. **Offers & urgency** — percentage-off framing across nearly every active category (see §6), always "upp till X%".
7. **B2B / company account** — "Förenkla klinikens inköp. Skapa företagskonto och få 10% på första ordern.", plus the free sample-box (Provlådan) copy in the inactive set. Distinct funnel from the B2C consumer offers.
8. **Distributed-brand spotlights** — Littmann (3M) stethoscopes, Beez Remedy sneakers (private label) each get dedicated single-product creative, distinct from the general assortment ads.
9. **Kit/bundle "head to toe" framing** — "Kitta dig från topp till tå", "Matchande kit från topp till tå", "Medical kit från topp till tå" — recurring cross-sell framing bundling socks + shoes + accessories into one purchase decision.

**Brand split:** the large majority of active creative promotes the Vårdväskan private-label range (Beez) and general assortment; distributed/carried brands (Littmann, and implicitly HOKA/Birkenstock etc. per the product catalogue) appear in a visibly smaller number of dedicated creatives (Littmann: 2 active) rather than driving the bulk of active volume.

## 6. Offers & pricing

- **Discount range observed on active ads:** 10% (first B2B order) up to 60% ("Arbetstillbehör upp till 60%"), with 20%, 30%, and 40% all represented as distinct active campaigns simultaneously (nametags −20%, stödstrumpor/arbetsredskap up to −30%, skor/sandaler and Back to Work up to −40%).
- **Newsletter/first-purchase incentive:** 15% off first purchase for email sign-up ("Prenumerera på vårt nyhetsbrev och få 15% rabatt på ditt första köp").
- **B2B incentive:** 10% off first order for creating a company account (företagskonto).
- **Free-trial/sampling offer (B2B):** "Provlådan" — free-shipping, free-returns sample box, no purchase obligation (per copy in the inactive set, §9; consistent with the B2B services description already in Info/client-info.md).
- **Multiple discount tiers run in parallel** on different categories at the same time (e.g. −20% nametags, −30% compression socks/tools, −40% shoes/Back to Work, −60% accessories, all active simultaneously as of this scrape) — this reads as category-led discount tiering rather than one storewide rate.
- **Historical (inactive set) offers** not currently running include "3 för 2" bundle deals (compression socks, work accessories) and a "Sommarrea! Upp till -70%" summer sale — a deeper discount than anything currently active. See §9.

## 7. Landing pages & funnel

- **Direct site destinations observed:** category pages (`/stodstrumpor/`, `/arbetstillbehor/`, `/skor/`), campaign pages under `/kampanjer/` (e.g. `skor-och-sandaler-deals`, `stodstrumpor-deals`, `namnskyltar-deals`, `arbetsredskap-deals`), a bestsellers page (`/bastsaljare`), theme-shop pages (`/temashoppar/medical-tema`), a bundle page (`/arbetstillbehor/bundles`), individual PDPs (e.g. a South West Sandy work-shoe product page), and the B2B account-creation page (`foretag.vardvaskan.se/skapa-foretagskonto`).
- **Meta Canvas / Instant Experience destinations:** several of the long-running hero ads (bestseller kit, stödstrumpor social-proof, "personal style" video) point to `fb.com/canvas_doc/...` in-app experiences rather than the website directly — these act as an on-platform intermediate step before (presumably) linking out to the site.
- **Destinations were read from Motion's stored `landingPageUrl` field only — not click-verified in a live browser.** Actual current behaviour of each link is unconfirmed.
- **Broken/placeholder destination found on two active ads:** `http://undefined` — both are the "15% rabatt på ditt första köp" newsletter-signup creative (one image variant, 6a484750708e10d24258a0f3 and 6a484750708e10d24258a0f1). This looks like a tracking/UTM template that failed to populate rather than a real URL. Flagged in §10.
- **Funnel signals:** the newsletter and företagskonto offers read as top-of-funnel acquisition (new customer/new company sign-up); category and campaign-page destinations read as mid-funnel category browsing; individual PDP links (named shoe products) read as narrower retargeting-style pushes. No explicit retargeting copy ("your item is waiting") was observed in the sampled copy.

## 8. Audience signals

- **EU transparency/DSA demographic data:** not captured — requires the Ad Library browser view, which was not available this run (§10).
- **Language:** all sampled copy is Swedish, consistent with a Sweden-only Meta presence under the Vårdväskan brand name (Color4Care, the NO/DK/FI/DE brand, was not checked — see §10, out of scope for this URL/page).
- **Regional sister Pages:** not checked this pass.
- **Indirect signals in creative:** copy consistently addresses the viewer as a healthcare worker directly ("dina kollegor", "vårdhjältar", "alla som jobbar inom vården") — audience is squarely staff/practitioners, not end patients or general consumers. No strong gendered framing observed in the copy itself; the one UGC testimonial video features a female-presenting speaker, and named-creator credit ("Arshig visar...") appears on one style-focused video.

## 9. Inactive-ad history

Based on the 203 inactive creatives captured in the newest-300 sample (launch dates 2026-05-13 to 2026-08-03 — this is a recent slice, not the brand's full inactive history of ~2,400 creatives):

- **"3 för 2" bundle campaigns** — "Stödstrumpor - 3 för 2" (14 creatives) and "Arbetstillbehör 3 för 2" (13 creatives) were a substantial recent push that is not currently active.
- **Deeper seasonal discount:** "Sommarrea! Upp till -70%" (6 creatives) — a steeper discount than any currently-active offer (max currently active is 60%).
- **"Beez Pulse – komfort i varje steg"** (15 creatives) — a private-label product launch (Beez Pulse) that was pushed hard and is now fully inactive; worth checking whether it's been superseded by newer Beez products (Remedy, Hero, Slip On are the private-label shoe names on file in Info/client-info.md; "Pulse" is not currently listed there).
- **"Journalgrodorkollektionen"** (5 creatives) — a themed collection launch ("journalgrodor" ≈ a novelty/frog-themed nurse item) not currently running.
- **"Pride-kit från topp till tå"** (4 creatives) — matches the "Happy Pride" theme shop already on file in Info/client-info.md; ran and is now inactive, i.e. a seasonal/calendar-linked drop rather than a standing collection.
- **"Dags för examen!"** (4 creatives) — graduation/exam-season campaign, timed to nursing-school graduation, now inactive.
- **"Sandal season - upp till 30% rabatt"** and **"Skor + Sandaler - upp till -50%/-20%"** variants — multiple discount tiers on the same shoe/sandal category were tested at different points across the sampled window, echoing the same category-tiering pattern seen in the active set (§6).
- 33 of the 203 sampled inactive creatives have no headline value at all — likely catalogue/DPA-style or Canvas-only creatives without a standard single-headline field; not individually itemised in this pass.

## 10. Observations, flags & gaps

**Flags — things the client should know now:**
- **Spelling error in currently active copy:** "Endast **fantastin** sätter gränser" (should almost certainly read "fantasin", i.e. "imagination") appears on 5 currently active nametag creatives (2 image, 3 video; oldest still running since 2026-08-04, newest since 2026-08-11). Library/creative IDs: 6a7bde76bd1fb961665f2f59, 6a779da9327036a84f8f9496, 6a779da9327036a84f8f9498, 6a728b57bef76e1aa062df92, 6a728b57bef76e1aa062df9a.
- **Broken landing page on 2 currently active ads:** landing page resolves to `http://undefined` on the "15% rabatt på ditt första köp" (newsletter signup) image creatives. Library/creative IDs: 6a484750708e10d24258a0f3, 6a484750708e10d24258a0f1. This looks like an unpopulated URL template (missing UTM/dynamic parameter) rather than a real destination — worth a direct click-check, since it wasn't browser-verified in this pass.

**Patterns worth following in the next scrape:**
- Whether the parallel category-discount tiering (20/30/40/60% simultaneously across categories) is a standing structure or shifts wave to wave.
- Whether "Beez Pulse" reappears (it went fully inactive despite a 15-creative push) or is being retired from the private-label range.
- Whether the Back to Work wave (7+ creatives, launched early August, still active) continues into a broader "back to school/work" seasonal push.

**Limitations of this scrape:**
- **No performance data anywhere in this file.** Motion has no connected ad account for Vårdväskan; every figure here is a creative/content count, never spend, impressions, hook rate, CTR, or ROAS. Frequency counts ("appears on N creatives") describe how often near-identical copy was launched, not how well any version performed.
- **No Ad Library browser pass.** Total-library "~X results" figures, EU transparency/demographic breakdowns, regional sister-Page views, and "multiple versions"/duplication-across-ad-sets signals were not captured — the Claude in Chrome extension was not connected this session.
- Only 203 of the roughly ~2,400 inactive creatives were sampled (the newest-300 pull, most of which were active); most of the brand's inactive history is unreviewed.
- Only 10 of 64 active videos were transcript/summary-analysed; visual (on-screen text) hooks on the other 54 were not reviewed.
- Glossary/taxonomy tags were requested but returned empty for every creative — Motion does not have creative taxonomy data for this brand.
- Color4Care (the NO/DK/FI/DE brand) was not checked — this scrape covers only the Vårdväskan Meta Page supplied by the user.

**Suggested next steps:**
- A browser-based Ad Library complement pass (once Claude in Chrome is connected) to get total-volume figures, EU demographic breakdown on the long-running hero ads, and click-verification of the broken `http://undefined` landing page.
- Re-scrape in 4–8 weeks to build a time series, and to see whether the fantastin typo and the broken newsletter landing page have been fixed.

*Source: Motion Creative Analytics (Meta Ad Library mirror), public data. Scraped 2026-08-21. All quotes verbatim from ad copy/transcripts.*
