# FZ Server Intelligence V1.2.8 — Full Aspect Ranking + All Summary

Authoritative base: **V1.2.7 — Fair Minimum Standard Ranking**.

## V1.2.8 — Full Aspect Ranking + All Summary
- Keeps the fair restaurant minimum-standard model from V1.2.7. Score 100 still means the restaurant minimum is met; rankings do not revert to best-vs-worst normalization.
- Adds full ranking for every eligible server across 15 aspects:
  1. Overall Result
  2. Work Speed
  3. Tables per Work Hour
  4. Customers per Work Hour
  5. Average Time Between New Tables (lower is better)
  6. Sales Result
  7. Sales per Work Hour
  8. Sales per Customer
  9. Sales per Table
  10. Tip Result
  11. Tip per Work Hour
  12. Tip per Customer
  13. Tables Served
  14. Customers Served
  15. Rotation / Table Opportunity
- Every ranking shows all eligible servers, not only Top 3.
- Adds an automatic **All Summary** after the rankings. It explains that the Best Overall server may not be the fastest, identifies the leaders in speed/sales/customer handling, and summarizes each scored server's strongest ranking positions.
- Adds Coaching & Action after the All Summary. Only below-standard results with normal table opportunity become coaching; low opportunity stays **Check Rotation First**.
- Ranking volume/opportunity (tables served, customers served, rotation) is context only and does not automatically increase/decrease performance coaching.
- Average Time Between New Tables uses the average seating-event gap per day/shift; #1 means the shortest average gap.

## 3-page bilingual PDF
- Page 1: plain-language Executive Summary built from all rankings.
- Page 2: ranking position matrix for all eligible servers across all 15 aspects, grouped into Overall/Speed, Sales, Tips, and Volume/Opportunity.
- Page 3: All Summary, each server's best ranking positions, coaching reasons, rotation context, and specific manager actions.
- English and Bahasa Indonesia remain selectable.

## Preserved from V1.2.7 / V1.2.6
- Fair minimum standard: 100 = restaurant minimum met.
- Overall = 45% Work Speed + 45% Sales Result + 10% Tip Result.
- Minimum sample: 3 work hours + 3 tables + 6 customers.
- Below-standard + low opportunity = Check Rotation First, not automatic coaching.
- Identity aliases remain locked:
  - A.J. / AJ / Ariana Garner → Ariana Garner
  - Angela Server / Angela Bar / Angela Gizzard / Angela Grizzad → Angela Server
  - Caitlin Dillon / Caitlin Bar → Caitlin Dillon
  - Mia / Mia Gibson → Mia Gibson
  - Mia Burress remains separate
- Role-aware server/bartender handling remains.
- Current Team / stale-roster fix remains.
- Large bright responsive PWA UI, working Owner auth, and bilingual PDF remain.
- Source data remains Quick Board R3M.8.30 + Just Tip ES1.8.5.

PWA cache namespace: `fz-server-intelligence-v128`.
