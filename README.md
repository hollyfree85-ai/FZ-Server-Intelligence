# FZ Server Intelligence V1.2.15 — Unified Identity Money + Bartender Fairness

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


## V1.2.15 — Unified identity money + bartender fairness
- Angela Server / Angela Bar / Angela Gizzard / Angela Grizzad are one canonical employee identity.
- When Quick Board records real Bar-table seating for a dual-role employee, Bar-role sales/tips are included with Server-role money in that person's performance numerator. The UI still shows the Server-vs-Bar breakdown for audit.
- This fixes the unfair case where Board tables/customers were already merged under one identity but Bar money was excluded from the score.
- In formations with 9 or more active servers, bartender Work Flow is compared against the Bar-table pool, while floor servers are compared against the floor-table pool. Bar 1–Bar 12 still count as real tables.
- In smaller formations, bartenders continue to be compared with the same-time team because they can serve both Bar and floor.
- Pure money-only bartender records remain excluded from table/rotation scoring only when Quick Board has no seating activity.
