# FZ Server Intelligence V1.2.13 — Bartender Financial Inclusion

Built from V1.2.12 Board-Linked Money Fix.

## Main update
- Pure bartenders such as Dorothy Makovicka and Libby Lane are included when their Tip report has real sales/tip money, even when they have no Quick Board table activity.
- Pure bartenders are shown as **BARTENDER • MONEY ONLY** and are never penalized for tables=0, customers=0, rotation=0, or Work Flow.
- Bartender financial totals are shown in a separate Bartender Financial Summary and in Sales & Tips.
- Pure bartender money does **not** enter Server Work Flow / rotation / coaching rankings.
- Dual-role staff remain role-aware: if Quick Board proves real table service, the Board-linked report can feed Server sales/tips (Sarah Kibler case). Explicit role accounts such as Angela Bar / Caitlin Bar stay linked to the same employee identity but their bar money is kept separate from Server performance scoring.
- Existing Shared Active Windows scoring, slow-traffic protection, SHIFT CLOSED status, render fix, identity merges, PDF, auth and PWA remain.

## Fairness rule
A bartender can have strong sales without serving floor tables. The app shows the bartender's real money data but does not invent a Server speed/rotation score.
