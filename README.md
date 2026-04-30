# TacSim — MOUT Training PWA

National Guard Military Operations in Urban Terrain (MOUT) training reference app. Built as a progressive web app — works offline, installs to home screen.

## What's Inside

| Section | Content |
|---|---|
| Solo Clear | 7-step individual room clearing technique |
| Team Entry | 4-man stack roles, go signal, breach flow, sectors of fire |
| Edge Cases | Barricaded doors, contact before entry, civilians, stairwells, T-intersections |
| Drone Ops | ISR integration, overwatch protocol, comms format, limitations |
| AI Quiz | Infinite randomized MOUT doctrine questions with AI-generated feedback |

## Deploy to Cloudflare Pages (5 minutes)

1. Fork or clone this repo
2. Go to [pages.cloudflare.com](https://pages.cloudflare.com)
3. Create Application → Connect to Git → Select this repo
4. Build settings: **Framework = None**, build command = blank, output = blank
5. Save and Deploy → live at `your-project.pages.dev`

Every push to `main` auto-redeploys. Free tier covers millions of requests/month. HTTPS is automatic (required for PWA install).

## File Structure

```
tacsim/
├── index.html      ← Full app (all JS/CSS inline, single file)
├── sw.js           ← Service worker for offline support
├── manifest.json   ← PWA manifest
├── icon-192.png    ← PWA icon (create: 192×192px)
├── icon-512.png    ← PWA icon (create: 512×512px)
└── README.md
```

## Icons

Create two PNG files with your logo:
- `icon-192.png` — 192×192 pixels
- `icon-512.png` — 512×512 pixels

Use any image editor or search "PWA icon generator" online.

## Ads

Current ad slots use fictional placeholder content. To monetize:

- **Google AdSense** — Sign up at adsense.google.com, replace ad div HTML with AdSense units
- **Direct sponsors** — Contact tactical gear brands directly, replace placeholder HTML with sponsor copy
- **Carbon Ads** — Apply at carbonads.com for a single clean unit

Ad slots are clearly labeled "AD" per FTC disclosure requirements.

## Content Notes

All training content is based on public domain US Army doctrine:
- FM 3-06 Urban Operations
- SH 21-76 Ranger Handbook (CQB sections)

US government publications are not subject to copyright. No trademarked names are used in training content.

## AI Features

The app uses the Anthropic Claude API for:
- Per-card "Ask AI" instructor notes
- Quiz question generation (19 doctrine topic areas, infinite unique questions)

The API key is handled by your deployment environment. For Cloudflare Pages, you can proxy the API call through a Cloudflare Worker to keep your key server-side.

## License

Training content derived from public domain US Army doctrine. App code: MIT.
