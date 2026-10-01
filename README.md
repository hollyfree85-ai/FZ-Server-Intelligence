# FZ Server Intelligence V1.2.16 — Unified Identity Money + Bartender Fairness

Built directly from V1.2.14 Bar Tables Count + Bartender Table Activity.

## Main update
- Pure bartenders such as Dorothy Makovicka and Libby Lane are included when their Tip report has real sales/tip money, even when they have no Quick Board table activity.
- Pure bartenders are shown as **BARTENDER • MONEY ONLY** and are never penalized for tables=0, customers=0, rotation=0, or Work Flow.
- Bartender financial totals are shown in a separate Bartender Financial Summary and in Sales & Tips.
- Pure bartender money does **not** enter Server Work Flow / rotation / coaching rankings.
- Dual-role staff remain role-aware. If Quick Board proves real table service, Board-linked money can feed the performance score. If the same employee also has a separate explicit Bar account and Quick Board records Bar-table seating on that date, that Bar money is also linked into the same employee performance numerator, while the Server-vs-Bar breakdown remains visible for audit.
- Existing Shared Active Windows scoring, slow-traffic protection, SHIFT CLOSED status, render fix, identity merges, PDF, auth and PWA remain.

## Fairness rule
A bartender can have strong sales without serving floor tables. The app shows the bartender's real money data but does not invent a Server speed/rotation score.


## V1.2.14 — Bar tables are real tables
- Bar 1 through Bar 12 seating events from Quick Board count as Tables Served and Customers Served.
- Bar seating contributes to same-time Work Flow, table/customer share, unique/reused table counts, and table history.
- A bartender with Bar-table seating is not treated as MONEY ONLY; they have real table activity.
- Bartender money remains role-aware and is not double-counted.
- Table occupied/Ready duration is still never used for scoring.


## V1.2.16 — Unified identity money + bartender fairness
- Angela Server / Angela Bar / Angela Gizzard / Angela Grizzad are one canonical employee identity.
- When Quick Board records real Bar-table seating for a dual-role employee, Bar-role sales/tips are included with Server-role money in that person's performance numerator. The UI still shows the Server-vs-Bar breakdown for audit.
- This fixes the unfair case where Board tables/customers were already merged under one identity but Bar money was excluded from the score.
- In formations with 9 or more active servers, bartender Work Flow is compared against the Bar-table pool, while floor servers are compared against the floor-table pool. Bar 1–Bar 12 still count as real tables.
- In smaller formations, bartenders continue to be compared with the same-time team because they can serve both Bar and floor.
- Pure money-only bartender records remain excluded from table/rotation scoring only when Quick Board has no seating activity.


## V1.2.16 — Full identity money merge + skip-neutral fairness
- Angela Server / Angela Bar / Angela Gizzard / Angela Grizzad (plus role variants) are one canonical employee. All linked sales, tips, and payout are combined for performance whenever the canonical employee has real Quick Board seating activity.
- Caitlin Dillon / Caitlin Bar (plus Caitlin Dion / Caitlin Bartender variants) are one canonical employee with the same full-money merge rule.
- Server-vs-Bar buckets remain visible for audit; Server detail also shows a Money by Linked Account table.
- Manual SKIP and BAR auto-skip are never performance penalties. Live skip cells reduce expected table opportunity instead of reducing the employee score.
- Historical PM bartender auto-skip is inferred from the known rule: every 2 real Bar tables creates 1 auto-skip, so that mechanic is neutralized even when old per-server skip cells are unavailable.
- CHECK ROTATION FIRST is renamed CHECK TABLE DISTRIBUTION. Manager guidance focuses on section/table distribution, not skip count.
- Bar 1–Bar 12 remain real tables.
