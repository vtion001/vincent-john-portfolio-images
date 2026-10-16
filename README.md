# vincent-john-portfolio-images

Public image host for [vtion001/vincent-john-portfolio](https://github.com/vtion001/vincent-john-portfolio).
Keeping the captures in this sibling repository prevents v0.app syncs from replacing binary assets and lets jsDelivr serve them without adding weight to the portfolio deployment.

## Image convention

Every portfolio image is an optimized **1600×1000 PNG** at DPR 1. Web entries are real browser captures; mobile entries are local screenshots presented in a consistent device frame. A failed web capture is an error and is never replaced with an illustration.

Use:

```text
https://cdn.jsdelivr.net/gh/vtion001/vincent-john-portfolio-images@main/images/<slug>.png
```

## Image map

| Portfolio entry | File | Capture source |
|---|---|---|
| Alto Property | `images/alto-property.png` | Live homepage hero |
| Bricklane Property Group | `images/bricklane.png` | Local Vue homepage (`:5173`) with API `:8080` on an isolated temporary SQLite database |
| iStrat Website | `images/istrat.png` | Live homepage hero |
| BOB | `images/bob.png` | Seeded local supervisor dashboard (`:8082/supervisor`) |
| MCA Tracker | `images/mca-tracker.png` | Isolated local Compose demo (`:8088/deals`) |
| MFG Calculator | `images/mfg-calculator.png` | Seeded local estimator (`:5173/estimator`, API `:8090`) |
| Kip | `images/kip.png` | Local Android screenshot in an Android frame |
| Pookoo | `images/pookoo.png` | Local iOS screenshot in an iPhone frame |
| SiteSignal PM | `images/sitesignal.png` | Local iOS screenshot in an iPhone frame |
| Alto Mission Control | `images/alto-mission-control.png` | Local frontend with reviewed, sanitized fixture responses |

## Refresh

From the portfolio repository, inspect the plan first:

```bash
node scripts/capture-screenshots.js --dry-run
```

Generate missing images directly into this repository:

```bash
npm run screenshots
```

Regenerate all ten:

```bash
npm run screenshots:force
```

The pipeline also supports `--only=kip,pookoo`, `--source=mobile`, and an explicit `--output-dir=/absolute/or/relative/path`. It launches installed Google Chrome by default; set `PORTFOLIO_CAPTURE_CHANNEL=bundled` to use Playwright's bundled Chromium instead.

Review every generated image for legibility and sensitive data before committing or publishing it. Mission Control is fail-closed behind fixed safe fixtures; do not weaken that interception for a capture.
