# FZ Server Intelligence V1.2.6 — Simple Language + Extra-Large UI

- Keeps V1.2.2 login/auth flow unchanged.
- Extra-large typography on phone, tablet, foldable, laptop and desktop.
- Rewrites technical analytics labels into simple manager language.
- Adds a simple score explanation directly in the app and PDF.
- Server detail uses “What We Found” and “What the Manager Can Do”.
- Keeps the 3-page bilingual English/Indonesian PDF with larger, simpler text.
- Fresh PWA cache namespace v126.
- Source data remains Quick Board R3M.8.30 + Just Tip ES1.8.5.


## V1.2.6 — Executive Summary PDF
- PDF remains exactly 3 pages.
- Page 1 is now a true Owner Executive Summary written in simple English or Indonesian.
- It explains what happened, who stood out, who needs coaching, why, whether table distribution was fair, data completeness, and what the manager should do next.
- Pages 2–3 retain detailed comparison, 5D charts, rotation/table-distribution analysis, coaching reasons, and action plan.
- Auth/login and underlying analytics calculations are unchanged from the previous working build.


## V1.2.6 — Current Team Truth / Stale Roster Fix
- No-activity ROSTER rows now use **Board Today’s Team** as the only Board roster source.
- Old names still present in `rotationBoardV31` can no longer resurrect a deleted employee.
- Tip `todayTeamRemoved` is honored, so retained drafts/receipts do not make removed employees appear as current roster.
- Real historical work is preserved: any server with actual Board seating activity or a real final Tip report still appears for that date even after being removed from Today’s Team.
- Example expected behavior: Angela Server can remain when currently scheduled; Angela Grizzad/Grizzard, Libby Lane, or Dorothy Makovicka disappear when absent from both current teams and have no activity/report for the selected day.


## V1.2.6 — Employee Identity Merge

Locked identity mappings used across Board + Tip:
- Angela Server / Angela Bar / Angela Gizzard / Angela Grizzad → **Angela Server**
- Caitlin Dillon / Caitlin Bar → **Caitlin Dillon**
- Mia / Mia Gibson → **Mia Gibson**
- Mia Burress remains a separate employee and is never merged with Mia Gibson.

Identity is merged across sources, but Server vs Bartender work remains role-aware. Bartender records do not count toward Server performance scores, sales/hour, tip/hour, or server ranking.
