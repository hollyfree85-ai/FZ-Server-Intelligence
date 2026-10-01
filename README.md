# FZ Server Intelligence V1.2.10 — Shift Closed Board Status Fix

## V1.2.10 — Shift Closed / 0 Active Server Fix
- A successful Quick Board sync with **0 active servers** is no longer reported as `BOARD ERROR`.
- For the current Daily view, if Board data/archive/team evidence exists and all servers are cut, the status is **BOARD SHIFT CLOSED**.
- Historical seating events continue to load from `analyticsV1` after the live rotation is empty or the shift has been cleared.
- Board connection errors are now separated from analytics/render errors, so a UI calculation issue cannot falsely label the Quick Board connection as broken.
- No scoring, identity, PDF, login, PWA, or V1.2.9 shared-active-window rules were changed.


Authoritative base: **V1.2.8 — Full Aspect Ranking + All Summary**.

## Core scoring change
- Performance is no longer judged from total work hours, tables/hour, customers/hour, sales/hour, tip/hour, or time a table stays occupied.
- Servers are compared inside **same-time active windows**. Example: if A and B are both AM, they are compared while both are active. When one is cut or another server joins, a new comparison window starts.
- Board `cutAt` is used when available. Current Team / shift boundaries are used as fallback so archived activity is not lost.
- **Low-traffic protection:** when there are too few arriving tables for the number of active servers, table/customer share scores are blended toward 100 so nobody is punished because the restaurant is empty.
- Every active/scheduled server receives an Overall Score. No minimum 3 hours / 3 tables / 6 customers rule.
- Missing Sales or Tip data is not scored as zero; available components are automatically re-weighted.

## Score formula
- Work Flow = 60% same-time Table Share + 40% same-time Customer Share.
- Sales Result = 55% Sales per Customer + 45% Sales per Table, when at least two usable sales reports exist.
- Tip Result = 55% Tip per Customer + 45% Tip per Table, with a small Overall weight.
- Overall = 45% Work Flow + 45% Sales Result + 10% Tip Result. Missing components are re-weighted out rather than scored as zero.
- 100 = fair / standard baseline.
- Below-standard Work Flow with low same-time table share becomes **Check Rotation First** before coaching.

## Table timing rule
- **Table occupied duration / turnover duration is never used.** Host may forget to click Ready, so that timing cannot fairly judge a server.
- The app instead counts:
  - total seating events / tables served
  - customers served
  - unique tables used
  - table reuse count
  - how many times each table was filled

## New tab
- Adds **How Score Works / Cara Hitung Nilai** with plain-language explanation of same-time windows, low-traffic protection, scoring weights, missing-data handling, and the no-table-duration rule.

## Rankings + PDF
- Keeps all-server ranking and All Summary. Rankings now emphasize same-time Work Flow, Table Share, Customer Share, Sales per Customer/Table, Tip per Customer/Table, table counts, unique tables and table reuse.
- 3-page bilingual PDF remains:
  - Page 1 Executive Summary
  - Page 2 all-server ranking matrix
  - Page 3 All Summary + coaching/action plan

## Identity / role rules preserved
- A.J. / AJ / Ariana Garner → Ariana Garner
- Angela Server / Angela Bar / Angela Gizzard / Angela Grizzad → Angela Server
- Caitlin Dillon / Caitlin Bar → Caitlin Dillon
- Mia / Mia Gibson → Mia Gibson
- Mia Burress remains separate
- Bartender-role data remains role-aware and does not leak into Server performance.

Source data remains Quick Board R3M.8.30 + Just Tip ES1.8.5.
PWA cache namespace: `fz-server-intelligence-v1210`.
