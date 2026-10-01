# FZ Server Intelligence V1.2.7 — Fair Minimum Standard Ranking

Authoritative base: V1.2.6 Identity + Role Merge.

## V1.2.7 — Fair Minimum Standard
- Replaces relative best-vs-worst 0–100 normalization with a restaurant minimum-standard model.
- Score **100 = minimum standard met**. 110 ≈ 10% above; 90 ≈ 10% below.
- A superstar server no longer forces another server toward 0 just because the superstar is much stronger.
- Automatic minimum is based on the middle/median result of servers with enough complete data, with conservative factors:
  - Tables/hour minimum = 85% of team median
  - Customers/hour minimum = 85% of team median
  - Sales/hour minimum = 85% of team median
  - Sales/customer minimum = 90% of team median
  - Tip/hour and tip/customer minimum = 80% of team median
  - Maximum normal gap between new tables = 120% of team median gap
  - Normal table opportunity = 80% of team median rotation turns/hour
- Overall score = **45% Work Speed + 45% Sales Result + 10% Tip Result**. Tips intentionally have low weight because customer behavior strongly affects tips.
- Minimum sample before scoring: **3 work hours + 3 tables + 6 customers**.
- Coaching logic:
  - >=120: Excellent
  - >=100: Meets Standard
  - 90–99: Light Coaching, only when table opportunity is normal
  - <90: Coaching Required, only when table opportunity is normal
  - Below standard + opportunity below 85: **Check Rotation First**, not automatic coaching
- UI and bilingual 3-page PDF explain the standard in plain language.
- Existing V1.2.6 identity aliases, role-aware Angela/Caitlin handling, Mia-vs-Mia-Burress separation, stale-roster fix, login/auth flow, PWA, and large UI remain.

- Keeps V1.2.2 login/auth flow unchanged.
- Extra-large typography on phone, tablet, foldable, laptop and desktop.
- Rewrites technical analytics labels into simple manager language.
- Adds a simple score explanation directly in the app and PDF.
- Server detail uses “What We Found” and “What the Manager Can Do”.
- Keeps the 3-page bilingual English/Indonesian PDF with larger, simpler text.
- Fresh PWA cache namespace v127.
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
- A.J. / AJ / Ariana Garner → **Ariana Garner**
- Alaina / Alainna Montalvo variants → **Alainna Montalvo**
- Angela Server / Angela Bar / Angela Gizzard / Angela Grizzad → **Angela Server**
- Caitlin Dillon / Caitlin Bar → **Caitlin Dillon**
- Mia / Mia Gibson → **Mia Gibson**
- Mia Burress remains a separate employee and is never merged with Mia Gibson.

Identity is merged across sources, but Server vs Bartender work remains role-aware. Bartender records do not count toward Server performance scores, sales/hour, tip/hour, or server ranking.
