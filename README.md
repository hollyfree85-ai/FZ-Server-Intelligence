# FZ Server Intelligence V1.2 — Owner Analytics

Source baselines:
- Quick Board: R3M.8.30 Table Capacity Setup
- Just Tip: ES1.8.5 Host Report Pool Summary

## V1.2 highlights
- Bright futuristic / layered “5D” UI with larger text and simplified Owner workflow.
- Daily, weekly, monthly and custom analytics.
- Server ranking only when Board activity + final Tip/hours data are complete.
- New scoring model: Overall = 40% Pace + 40% Sales Efficiency + 20% Tip Efficiency.
- Pace combines tables/hour, guests/hour and median seating gap.
- Sales efficiency combines sales/hour, sales/guest and sales/table.
- Tip efficiency combines tip/hour and tip/guest.
- Rotation is treated as management context, not as a punishment in the performance score.
- Weakest server analysis includes root causes and management recommendations.
- Rotation fairness compares guest-share distribution with rotation-load distribution.
- 3-page English PDF and 3-page Bahasa Indonesia PDF with layered 5D-style charts.
- Identity Sync keeps aliases together: A.J./AJ/Ariana Garner; Alaina/Alainna; Aida/Aida Gonzales (inactive by default).

## V1.2 roster deletion fix
Roster-only names are shown only when the current Board roster and Tip team agree on the employee for the selected date. Old Tip drafts no longer resurrect deleted employees. Employees with actual Board activity or final Tip reports remain visible for historical accuracy.

## Important metric note
“Pace” means seating throughput (tables/hour, guests/hour, interval between seating events). It does **not** measure how long a server takes to finish table service because Quick Board does not record table-completion timestamps.

## Deploy
Upload these files to the root of the existing GitHub Pages repository and commit:
- index.html
- app.js
- manifest.webmanifest
- sw.js
- README.md

Then refresh the GitHub Pages site with Ctrl+F5 (or clear site cache once) so V1.2 replaces the older service-worker cache.
