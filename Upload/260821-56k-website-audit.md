# 56K x Vårdväskan — Website Audit (SEO Audit 2025)

Uploaded: 2026-08-21
Source: Copy of 56K x Vårdväskan - Website Audit (Google Slides, 75 slides)
Source date: 2025-03-11
Author: 56K Digital (agency SEO audit of vardvaskan.se / foretag.vardvaskan.se, delivered to the client). Contacts: Markella Fragkaki (SEO Consultant), Eva Broman (Senior SEO Consultant), Vincenza La Starza (Head of SEO).

Note: many slides are chart-based (visibility index graphs etc.); the underlying numbers are not present in the extracted text — chart takeaways are captured from slide titles.

---

## Agenda

01 Introduction · 02 What is a Site Audit? · 03 Current Performance (incl. Competition & other markets) · 04 Website Audit (Crawlability & Indexation, Fundamentals, Internal Linking, Grow Opportunities) · 05 Next Steps · 06 Other

## 01. Introduction

- 100 million searches per day in Sweden; 20% of searches have never been searched before.
- Organic Search drives 53% of all visitors to B2B & B2C websites (searchengineland.com study) — **ca 30% for Vårdväskan**.
- Four types of search intent with Vårdväskan examples: Informational ("stödstrumpor"), Commercial ("julklapp vårdpersonal", "beez vs birkenstock"), Navigational ("id korthållare vårdväskan"), Transactional ("stödstrumpor bomull").
- Successful SEO integrates: 1 Technical SEO (good technical foundation), 2 Content (matching target audience behaviour), 3 EEAT factors (authority and trust), plus Branding & PR (links from partners & PR).

## 02. What is a Site Audit?

Purpose: identify weaknesses and opportunities affecting organic search; recommendations and priorities form the basis of the SEO strategy. Goal: traffic that drives and grows the business. Audit components: 01 site audit (basics, current performance, user experience); 02 keyword research (search behaviour, competitive analysis); 03 content plan (optimised category pages & site structure, new content, optimised existing content). SEO is an ongoing process: audit & strategy → roadmap → monthly tasks (content optimisation, technical tasks, link building, monitoring) → evaluation (rankings, traffic, conversions, business goals, feedback) → iteration. Scope: over 100 checkpoints in technology, content, structure and user experience.

**Website Health Score: 43% — 55 checks out of 102 did not pass; 16 marked as high priority.** Everything delivered in Sheets as a working document (audit + action plan).

## 03. Current Performance

- Visibility index graphs for vardvaskan.se and foretag.vardvaskan.se (charts; no figures in text).
- Branded vs non-branded traffic split shown for vardvaskan.se (chart).
- **There has been a negative trend for Vårdväskan's brand** (search volume, Keyword Planner).
- **Vårdväskan has the second biggest market share** (share of search).

### Competition & other markets

- Vårdväskan & main competition compared (7days is the smallest competitor, excluded from the graph).
- **Vårdväskan is currently in the middle of the market.**
- **Second biggest within "stödstrumpor"** (Apotea & Apotek Hjärtat are too big and therefore not included in the graph).
- **In the middle of the market within "arbetsskor".**
- **Biggest within "namnskyltar"** while competitors are declining.
- **Second biggest within "vårdkläder".**
- International: Norway (color4care.no vs competition), Denmark (color4care.dk vs competition), Finland (color4care.fi vs competition) — chart slides.

### Top performing URLs (Sweden)

| Keyword | Search volume | Position | URL |
| --- | --- | --- | --- |
| stödstrumpor | 27,100 | 2 | vardvaskan.se/stodstrumpor/ |
| sandaler | 18,100 | 5 | vardvaskan.se/skor/sandaler |
| arbetsskor | 8,100 | 5 | vardvaskan.se/skor/arbetsskor |
| nyckelband | 5,400 | 2 | vardvaskan.se/arbetstillbehor/nyckelband |
| stetoskop | 4,400 | 2 | vardvaskan.se/arbetsredskap/stetoskop |
| otoskop | 2,400 | 1 | vardvaskan.se/arbetsredskap/otoskop-oftalmoskop-och-dermatoskop |
| namnskyltar | 1,300 | 2 | vardvaskan.se/namnskyltar/ |

## 04. Website Audit — Key opportunities

- **Crawlability & Indexation:** currently less than 50% of existing pages are indexed due to crawlability and indexation problems (incorrect robots.txt, missing XML sitemaps, pagination, canonical tags).
- **Internal Linking & Navigation:** thousands of broken links and redirect chains due to incorrect breadcrumbs and old http links. Main navigation and subcategories rely on JavaScript.
- **Hreflang & International Targeting:** the B2B site is currently considered duplicate; canonical tags and hreflang are missing or misconfigured (canonicalizing to the main site).
- **Accessibility & Usability:** the site does not meet WCAG 2.1 AA standards (alt texts, buttons, forms, contrast, "read more" links, page speed). Accessibility score 71%; recommendation over 90%.
- **Subcategories + Product pages:** big opportunity to grow visibility and traffic via subcategory expansion and unique content for product pages and variants.
- **Schema Markup & EEAT:** EEAT factors lacking on key pages (important for YMYL pages); schema markup missing/erroneous; review questionable old backlinks and site security.

### Crawlability & Indexation details

- **B2B site has a canonical to the B2C site:** foretag.vardvaskan.se pages won't rank because Google treats them as duplicates of vardvaskan.se — loss of B2B search traffic, wasted link equity, mixed search intent. Recommendation: consolidate B2B with the main website to increase traffic & decrease crawl budget; if not technically possible, identify unique pages for foretag.vardvaskan.se, only canonicalize exact duplicates, create a dynamic solution for price adjustments, redirect duplicate pages (example pattern from dpj.se).
- **Robots.txt** doesn't contain the correct sitemap.xml and is not optimised (low-hanging fruit): remove incorrect XML sitemap reference, add correct one.
- **Correct sitemap.xml is missing and not added to GSC** (low-hanging fruit): faulty sitemaps confuse Google; submit all URLs, upload sitemaps in Search Console.
- **Product pages are missing hreflang tags** / incorrect setup: reference all versions including the current page and a default URL; follow ISO codes.
- **Many current solutions are JavaScript dependent; the main menu is client-side rendered:** search engines may not crawl key category and product links. Fix: server-side rendering or static HTML for navigation, `<noscript>` fallback, improved internal linking (e.g. HTML sitemap).

### Fundamentals

- **Over a thousand title tags are not optimised** — potentially causing lost clicks and revenue (low-hanging fruit).
- **Address search intent with more specific category names** (low-hanging fruit): e.g. "arbetskläder" (6,400/m, position 41 → /klader/), "arbetskläder herr" (1,300/m, position 55 → homepage), "arbetskläder dam" (1,200/m, position 18 → /klader/arbetsbyxor). Rename e.g. "skor" → "arbetsskor", "kläder" → "arbetskläder".
- **WCAG 2.1 AA not met** — accessibility score 71%, recommendation 90%+.
- **Structured data:** implement schema for Organisation (incl. sameAs), FAQs, Breadcrumbs, Authors; fix current errors; FAQ markup for SERP features and accessibility.

### Internal Linking

- **14% of discovered URLs are redirects or 404s** (low-hanging fruit): fix 404s, avoid redirect chains, routine link checks.
- **Current breadcrumb setup creates a lot of 404 pages** (low-hanging fruit): breadcrumbs missing on several pages; current breadcrumbs link to 404s/301s. Expand breadcrumbs to category and subcategory pages, ensure valid links, use BreadcrumbList structured data.
- **There are categories that cannot be found through the menu** (orphan categories; low-hanging fruit).
- **Improve pagination:** "show more" products loaded via JavaScript cannot be seen/followed by crawlers within rendered HTML. Options: multi-page pagination with self-referencing canonicals (incl. rel=prev/next for other search engines), or a "View All" page with canonicals to it.

### Grow opportunities

- More potential within categories & subcategories: are we showing up for all potential clients? Missing traffic by combining two keywords in one page? Easy for clients to find what they seek? Are we confusing Google?
- **"Men/Women" segment: ~190,000 monthly searches (37 keywords), ~27,000 available clicks/month, current performance ~180 clicks — ca 0.6% of available traffic.** Examples: tunika dam (3,600/m, pos 10, product URL), arbetsbyxor herr (2,900/m, pos 18), arbetsbyxor dam (2,400/m, pos 27), förkläden dam (1,900/m, pos 42), bussarong dam (320/m, pos 4), pikétröja dam (260/m, pos 33), bussarong herr (170/m, pos 11), tunika herr (140/m, pos 17).
- **Unclear intent on category pages makes ranking harder** — prioritize category pages over product pages (broader keywords, longer relevance, better internal linking, higher conversion, stronger backlinks).
- **Meet client needs through content expansion:** subcategories + inspirational articles.
- **Turn faceted navigation into a traffic opportunity based on keyword research:** 01 category + gender; 02 category + materials; 03 category + colors; 04 brands + category; 05 more. Main keywords: arbetsskor dam 2,400; arbetsskor herr 2,400; arbetskläder herr 1,300; arbetskläder dam 880; stödstrumpor herr 720; stödstrumpor dam 480; stödstrumpor nylon 480; stödstrumpor ull 260; birkenstock dam 22,200; birkenstock herr 14,800; hoka dam 4,400; hoka herr 1,900; birkenstock beige 390; hoka svart 320; birkenstock svart 260; birkenstock brun 210.

## 05. Next Steps

**Impact/effort matrix:**

- HIGH impact: robots.txt, title tags, breadcrumbs, duplicate pages, canonical tag issues, XML sitemap, internal links, category page, optimised product variants, accessibility (WCAG), indexation discrepancy, page speed, core web vitals, historic website visibility drop, JavaScript rendering.
- MEDIUM: thin content, unique product text, redirect issues, sources, heading tags, meta description, HTML sitemap, popups (interstitials), image alt texts, accessibility (video), content gaps vs competition, 5XX errors, 404 pages, hreflang issues, helpful unique content, mega menu best practice, article page, product page, brand and campaign pages, structured data errors/opportunities, pagination, crawl budget, brand Wikipedia page, credible author profiles, digital PR, discontinued product management.
- LOW: non-descriptive anchor texts, broken backlinks, related pages, image title tags, image captions, orphan pages, website hierarchy structure, longtail, security headers, GA4 content groups, backlink profile vs competition, unnatural backlinks, image URL file naming.

**Low-hanging fruit — where to start:**

- Crawlability & indexation: remove existing sitemap.xml (api), add new sitemap.xml with all URLs to index, add sitemaps to GSC.
- Linking: fix broken URLs in breadcrumbs, add breadcrumbs to subcategories, fix broken internal links, make all subcategories static URLs, add links to orphan categories.
- Fundamentals: rename key categories ("skor" → "arbetsskor", "kläder" → "arbetskläder"), shorten 1,000+ titles, fix duplicate/missing meta descriptions (product pages), fix structured data errors, add FAQ structured data, unique content for product variations.

**Prioritisation going forward:** LHF & quick wins → B2B → B2C → navigation issues → internal linking → crawlability & indexation → category expansion → accessibility WCAG 2.1 AA.

Deliverables: site audit + recommended action plan in Sheets; working sheet as foundation for category expansion.

## 06. Other

- **Image optimisation:** issues with all aspects of image SEO — alt tags, file size & naming, missing CDN, lazy loading (not low priority but high effort).
- **PageSpeed & Core Web Vitals:** the site does not pass due to LCP, CLS & INP (bigger, more complex project).
- Pop-ups are not responsive in mobile versions.
