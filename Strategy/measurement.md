# Measurement — Vårdväskan

How the client measures performance, and how much confidence the numbers deserve. Creative recommendations are worthless if the client cannot tell whether they worked.

## KPI stack & reporting cadence
Which metrics are actually followed, at what level, how often, and by whom.

Partially collected: per the NOOS retainer draft (as of 2026-05), reporting will be monthly meetings + weekly/bi-weekly performance reports + a performance dashboard. 56K's 2024 analysis worked against a 14% platform COS threshold on Google Ads (implying COS/ROAS steering at the time) and proposed moving optimization toward GM1/GM2 profit. Client-confirmed KPI stack: *Not yet collected*.

## Attribution model
Platform-reported, MMM, incrementality testing, blended, or a mix. Attribution window.

Partially collected (56K audit of the setup, as of 2024-12): GA4 with ecommerce parameters across several markets, ready for data-driven attribution; Cookiebot consent manager; server-side cookies extending cookie lifetime; Consent Mode V2 Advanced (cookieless pings, ~65% modelled recovery); Enhanced Conversions live; Conversion Cart Data (product-level) live. No MMM or structured incrementality in place at that time (56K pitched MMM as a next step). Attribution window: *Not yet collected*.

## Measurement maturity
Is measurement connected to the backend (Shopify, CRM, ERP)? Server-side tracking? Known data quality problems? Who owns the setup.

Per 56K (agency audit, as of 2024-12): overall great measurement setup, with gaps — **user-id not working** in GA4 (blocks new-vs-returning measurement and journey stitching); **sensitive user data sent in page URLs (e.g. emails in reset links) — GDPR risk** to remediate. Server-side cookies in place. ERP/backend connection for GM1/GM2 steering proposed by 56K but adoption unconfirmed. CRM side (per client, 2026): Mailchimp engagement/purchase signals used for segmentation; advanced analysis (RFM, churn risk, customer value) limited by Mailchimp functionality. Setup ownership: *Not yet collected*.

## Definition of a creative win
The concrete threshold that makes an ad a winner in this account — hook rate, thumbstop, CTR, CPA or ROAS level. If no definition exists, note that: it is a blocker for hypothesis-driven work.

*Not yet collected* — no definition exists in the collected material. The client has explicitly asked for insight-based hypothesis testing with structured learnings (per meeting recap, 2026), so defining a win threshold is a known open item.

## Test infrastructure
A/B testing capability, incrementality panels, brand lift studies, holdouts. What has actually been run, not what is theoretically available.

*Not yet collected* as confirmed-run tests. 56K proposed (2024-12) Meta brand lift and conversion lift studies and regular creative A/B testing; whether any were run is unknown.
