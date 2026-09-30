# FZ Server Intelligence V1 — Owner Analytics

Source baselines:
- FZ Quick Board R3M.8.30 — Owner Table Capacity Setup
- Fred Zhang Just Tip ES1.8.5 — Host Report Pool Summary

## Purpose
Third, read-only Owner analytics app. Combines Quick Board seating/rotation data with Just Tip financial/hour data.

## Main features
- Owner-only authentication using the existing Just Tip Firebase Auth + users profile role check.
- Daily / weekly / monthly / custom date range.
- AM / PM / All filter.
- Board metrics: tables, guests, section, table, seating timestamp, rotation slots, pace, table utilization.
- Tip metrics: hours, sales, paid tip, cash tip, total tip income, busser tip out, bar tip out, bar tip received, final paid out.
- Rankings: Overall Performance Index, sales, guests, tables, sales/hour, guests/hour, tables/hour, sales/guest, tip/hour.
- Detailed per-server seating history.
- Employee Identity Sync aliases, including defaults:
  - A.J. = Ariana Garner
  - Alaina Montalvo / Alainna Montalvo = Alainna Montalvo
  - Aida / Aida Gonzales = Aida Gonzales (inactive by default)
- Employee can be inactive without deleting historical analytics.
- PDF export in English or Bahasa Indonesia.
- PWA install support.
- Board auto refresh every 30 seconds; Tip data uses Firestore realtime listener.

## Overall Performance Index
Period-relative percentile index:
- 30% Sales / Hour
- 22% Guests / Hour
- 18% Tables / Hour
- 15% Sales / Guest
- 15% Tip Income / Hour

This is a management comparison index, not a disciplinary score.

## Pace definition
"Speed/Pace" means seating throughput (tables/hour, guests/hour, median time between seating events). It is NOT table-service duration because Quick Board does not record checkout/completion timestamps.

## Deployment
Upload the contents of the ZIP to a GitHub Pages repository root and enable Pages.

## Safety
This app does not write to Quick Board or hourlyReports. Alias settings are stored locally in the browser for V1 and do not rewrite either source app.
