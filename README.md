# FZ Server Intelligence V1.2.2 — Auth Repair + Responsive PWA

Hotfix over V1.2.

## Fixes
- More robust Owner login initialization using the same session-persistence pattern as Just Tip.
- Login accepts Owner username or full email.
- Visible error if authentication succeeds but Owner profile verification fails.
- Fresh PWA cache namespace (`v121`) and cache-busted app/service-worker URLs to prevent mixed old/new builds.
- Reset App Cache button on login screen for emergency recovery.
- Install App support with 192px/512px icons and standalone manifest.
- Responsive layout improvements for phones, tablets/iPad, foldables and desktop.
- Existing V1.2 analytics, identity sync, roster fix and bilingual 3-page PDF remain intact.

## Deploy
Upload all files in this package to the root of the existing GitHub Pages repository and replace the older files. After deployment, open the site once and use **RESET APP CACHE** if an older cached build is still controlling the page.


## V1.2.2 hotfix
- Restores the exact V1 Firebase Auth initialization pattern (`getAuth` + session persistence) that was previously confirmed working.
- Keeps V1.2 analytics, 3-page bilingual PDF, PWA installability, and responsive layout.
- Significantly enlarges login, buttons, KPI values, server names, analysis text, ranking tables, and mobile/tablet typography.
- Uses fresh cache namespace v122 to prevent mixed old/new assets.
- Fixes the V1.2.x JavaScript parser regression that prevented the main module from loading at all.
