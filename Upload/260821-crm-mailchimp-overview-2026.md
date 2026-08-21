# Vårdväskan's CRM Work in Mailchimp — Current State 2026

Uploaded: 2026-08-21
Source: Vårdväskans CRM-arbete i Mailchimp – nuläge 2026.docx (Drive folder "CRM : Mailchimp overview"; file last modified 2026-08-13)
Source date: 2026 (data window cited: August 2025 – July 2026)
Author: Vårdväskan / CRM team (client-side current-state description). Original in Swedish; translated to English.

---

Vårdväskan's CRM work in Mailchimp is built on one shared audience and one shared customer view, from which the right recipients are segmented by market, vertical, engagement and behaviour. The goal for 2026 is to move from broad reach to higher actual relevance and engagement — the right communication to the right customer, rather than a classic "spray and pray" model.

## One audience — several markets and target groups

The audience **Vårdväskan AB contains 427,514 contacts**. Of these, **425,507 are opted in for email marketing** and **221,385 for SMS marketing**. Email and SMS are two contact channels within the same customer base — the figures should not be added together.

We operate in **SE, NO, FI, DK and DE**. The customer base is not split into separate audiences per country; market and vertical are combined through customer data in Mailchimp. A Swedish B2C customer is defined, for example, as SE = TRUE + B2C = TRUE.

| Market | B2C | B2B |
| :-: | :-: | :-: |
| SE | 277,577 | 8,112 |
| NO | 102,709 | 3,843 |
| FI | 58,053 | 2,187 |
| DK | 12,667 | 451 |
| DE | 1,844 | – |

Segment sizes show the size of each target group and should not be summed to the audience total.

On the Swedish market we can additionally segment by profession. Profession data currently exists on **70,642 contacts**, but is not yet registered on the whole Swedish base. Identified professional groups: Undersköterska (assistant nurse) 28,182 · Sjuksköterska (nurse) 10,927 · Vårdbiträde (care assistant) 5,366 · Läkare (physician) 1,933 · Tandläkare (dentist) 1,045 · Medicinsk sekreterare (medical secretary) 917 · Barnmorska (midwife) 629 · Fysioterapeut (physiotherapist) 447 · Hudterapeut (skin therapist) 201 · Annat (other) 20,995.

## Engagement governs who we activate

For ongoing campaigns we primarily use our **90/180 segment**. A customer qualifies through at least one of three signals: open within 90 days, click within 90 days, or purchase within 180 days. Both email engagement and actual purchase thus determine which customers we consider relevant to activate.

We also have broader **180/365 segments** with the same principle, used sparingly and mainly when a larger activation motivates broader reach.

Qualifying for the main segment does not automatically mean the customer receives the send. Before a campaign is sent, a set of central exclusions is applied:

- **Recent Purchasers** — protects customers who recently bought from renewed campaign pressure.
- **New Leads** — keeps new leads out of regular campaign sends during the first period.
- **Low intent Openers (MPP)** — filters out contacts whose opens are mainly driven by Apple MPP and who lack clicks or other stronger intent signals.
- **Low intent Openers** — filters out contacts who open mail but lack sufficiently strong other engagement.
- **Unengaged Buyers** — catches previous buyers whose current email engagement is too weak.
- **Frequency** — ensures the customer is not over-communicated and that automated journeys take precedence over campaigns.

## 17 active e-commerce flows

Mailchimp currently contains **17 active e-commerce flows** covering the central parts of the customer journey: Welcome Series, Browse Abandonment, Abandoned Cart, Winback, Loyalty / Campaign Offers, Product Recommendation, Cross-sell and New Arrivals.

Cross-sell and New Arrivals are broken down at category and product level, so communication can be adapted to what the customer previously showed interest in or bought.

Flows are prioritized over regular campaigns. We work with a **frequency cap of maximum four emails per week** and a **24-hour cooldown** after activation. In Winback, Abandoned Cart and Browse Abandonment, harder locking is used: the customer is paused from competing flows and campaigns during the active journey.

**Send schedule:** B2C campaigns are normally sent Wednesday and Sunday at 09:00; B2B Wednesday at 09:00. Flows activate Monday–Tuesday and Thursday–Saturday between 09:00–12:00, separating automated communication from the regular campaign days.

## Lead capture, SMS and personalization

New leads are captured directly on the site. For **B2C**: Sign-up and Exit Intent, together with ready popup templates for sales and Flash Sales that can be activated quickly. For **B2B**: Sign-up, Företagskonto (company account) and Provlådan (the sample box).

**SMS** is today used mainly tactically at Flash Sales, sale launches and end of sale. The next step is to build the channel into automated journeys as well, above all Welcome, Abandoned Cart and Winback.

**Clerk.io** is integrated with Mailchimp as part of the existing e-commerce and personalization setup.

## Focus ahead: better precision, not higher volume

Within B2C SE alone, approximately **22.3 million emails were sent between August 2025 and July 2026**. The scale already exists. The 2026 focus is therefore not to maximize the number of sends, but to get better at identifying actual engagement, intent and the right moment to communicate.

The next development step is above all more advanced customer analysis, e.g. **RFM models, churn risk and customer-value-based segmentation**. That would add precision on top of today's behaviour- and engagement-based model, but the possibilities are currently partly limited by Mailchimp's analysis and segmentation functionality.
