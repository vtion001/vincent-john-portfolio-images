# vincent-john-portfolio-images

Public image host for [vtion001/vincent-john-portfolio](https://github.com/vtion001/vincent-john-portfolio).

Lives in its own repo so:

- The portfolio's v0.app auto-sync can't clobber the bytes
- jsDelivr serves the files from a global CDN for free
- The portfolio itself stays slim — no large binary churn in PR diffs

## Usage

Reference each image from the portfolio via jsDelivr, pinned to `@main` (auto-updates) or a tag (immutable):

```
https://cdn.jsdelivr.net/gh/vtion001/vincent-john-portfolio-images@main/images/<slug>.png
```

## Image map

| Portfolio entry | File | Source |
|---|---|---|
| iStrat Website | `images/istrat.png` | live capture — istrat-website-revamp.vercel.app |
| Alto Property | `images/alto-property.png` | live capture — altoproperty.com.au |
| Sales CRM | `images/sales-crm.png` | live capture — sales-crm-brown.vercel.app |
| Skin Essentials | `images/skin-essentials.png` | live capture — v0-skin-essentials-website.vercel.app |
| Bricklane Property Group | `images/bricklane.png` | local-clone dashboard capture (or generated illustration if dev env fails) |
| Alto Chatwoot | `images/alto-chatwoot.png` | local-clone dashboard capture (or generated illustration) |
| Joshua OpenClaw | `images/joshua-openclaw.png` | generated illustration (voice-driven agent, no UI) |
| BOB AGS | `images/bob-ags.png` | local-clone dashboard capture (or generated illustration) |
| AGS Email Tool | `images/ags-email-tool.png` | generated illustration (internal tool, no public UI) |

All images are 1280×720 PNG, dark brand background (`#0f0f0f`) with lime accent (`#ccff00`).

## Refresh

Run `npm run screenshots:force` in the portfolio repo, then copy the regenerated PNGs here and push to `main`. jsDelivr's `@main` URLs auto-update; allow a few minutes for CDN propagation, or use a tag URL for immediate invalidation.
