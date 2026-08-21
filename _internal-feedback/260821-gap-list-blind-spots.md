# Internal feedback — gaps the gap-list missed (pre-kickoff review)

Source: Anna Eriksson (NOOS, Paid Search), in chat, 2026-08-21.
Context: reviewed a "what are we missing?" summary generated from this knowledge tree ahead of the client kickoff meeting the following week. The summary was assembled by reading `client-data-overview.md` plus all knowledge files. Anna listed five things she expected to be flagged that were not.

This is feedback on the **system** — the field structure and how the gap summary is produced — not on the client.

---

## 1. Sales statistics as a data source is not a field anywhere

Anna asked: *"Försäljningsstatistik? Finns den i Power-BI? Går det att dela / kan vi få inlogg dit?"*

The tree records revenue totals (102 MSEK 2025, 114 MSEK target 2026) and scattered funnel ratios from the 56K audit, but there is **no field for the client's own sales reporting system or access to it**. `Access & tools` lists ad platforms, GA4, Mailchimp, Hubspot, Clerk.io, Smartly — no BI/reporting layer. Power BI is not mentioned anywhere in the tree, so the gap summary could not surface it.

Consequence: the summary asked for AOV, LTV and margin per category as abstract numbers, when the actionable question is *where does that data live and can we get a login*. Category-level sales data is the input to the priors gate and to any HERO-product work.

Suggested system change: `Info/client-info.md` → `Access & tools` should explicitly cover BI/reporting and data-warehouse access (Power BI, Looker, Shopify/ERP reporting), or `Strategy/measurement.md` should carry a "sales data source & access" field. Right now nothing prompts for it.

## 2. Persona provenance is not captured — only persona content

Anna asked: *"När gjordes deras personas? Hur togs de fram?"*

`Strategy/creative-strategy.md` → `Audience / Personas` holds "Fräcka Felicia" and "Rutinerade Rita" in detail, sourced to the client's B2C strategy 2026. It records **what** the personas say, never **when they were made or on what evidence**. So the field reads `[x]` collected and the gap summary treated it as solved.

This matters because it is the difference between a persona built on CRM/purchase data and one built in a workshop. The tree already separates assumed barriers (`creative-strategy.md`) from verified customer language (`customer-voice.md`) — persona provenance deserves the same treatment. A workshop persona from 2023 reused in a 2026 strategy deck is a different input than a data-derived one.

Suggested system change: personas should carry method + date (how derived, what data, when, by whom). Either as a sub-line in the field's instruction text or as a general rule that persona entries state provenance.

## 3. Targets are captured as a single year, with no pacing and no next year

Anna asked: *"Försäljningsmål och hur de taktar 2026. Mål för 2027?"*

`Goals & targets` in `marketing-strategy.md` holds the 2026 revenue target and notes that marketing-specific numbers are missing. It does **not** prompt for:

- **Pacing / actuals to date** — are they tracking to 114 MSEK eight months in? A target is meaningless without the run rate against it. This is arguably the single most important commercial fact for a kickoff, and no field asks for it.
- **The horizon beyond the current year** — 2027 targets, which determine whether we are building for a quarter or for a growth curve.

Suggested system change: `Goals & targets` should ask for current pacing against stated targets and the multi-year horizon, not just the stated numbers. The field's own instruction text already says to flag gaps between stated targets and historical performance — pacing data is what makes that check possible, and it is not requested.

## 4. Budget document — spend per channel/platform

Anna asked: *"Budgetdokument? Så man kan se spend fördelad per kanal/plattform."*

`Channel spend distribution` exists as a field and is correctly marked `[ ]` missing, so this one was surfaced — but as an abstract "no spend split figures in collected material". Anna's framing is better: **ask for the artifact** (the client's media budget document), not the numbers. Asking for a document gets you the split, the periodisation and the market breakdown in one go, and it is a concrete thing to request in a meeting.

Suggested system change: pattern-level. Where a field's content normally lives in a client document (media budget, year wheel, sales report), the gap summary should ask for the document rather than the data points. Cheaper for the client to hand over and less lossy.

## 5. Brandstory: "not yet converted" overstates what exists

Anna: *"Brandstory var bara en bild."*

`Upload/260821-brandstory-keynote-note.md` says the Brandstory FINAL 2026 Keynote (.key, 23.6 MB) could not be converted and is "pending conversion", and `Info/brand.md` repeats that a Brandstory exists but is not yet converted. Per Anna, the file is essentially just an image — so converting it will not yield a brand story document. The tree currently implies a substantive asset is one export away.

Consequence: both a false lead (a future run chases a conversion that yields nothing) and a masked gap (there is no written brand story — that is a real hole, not a tooling problem).

Suggested system change: when ingestion fails on a file, the note should distinguish *could not read it* from *read it and there was little in it*. As written, an unconvertible file is always logged as pending content. Where the format blocks reading entirely, the note should say the content is unknown rather than implying it is pending.

---

## Pattern across all five

Four of the five gaps were invisible to the summary because **the tree has no field for them** — sales data access, persona provenance, target pacing, next-year horizon. The gap summary can only report against the field structure it reads, so a missing field reads as "nothing missing". A field marked `[x]` is the most dangerous state in the tree: it stops anyone asking the follow-up question.

Two things follow for the system:

1. The gap summary should not be purely field-driven. It needs a pass that asks what a kickoff actually needs and compares that against the tree, rather than only listing `[ ]` and `[~]` fields.
2. `[x]` should not close a subject. Several `[x]` fields here (Personas, Products, Name) are collected but shallow — collected content and confidence in that content are different axes, and the overview only tracks the first.

Both point to the same underlying limit: the overview tracks presence, not sufficiency.
