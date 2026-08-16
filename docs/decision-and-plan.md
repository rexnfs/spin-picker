# Spin Picker — Platform Decision & Build Plan

## The decision: build a PWA now, wrap for the App Store later (if ever)

You need this in class **soon**, and a native App Store app can't deliver that:
- Apple review takes days to ~2 weeks for a first submission, and can bounce back.
- Requires a paid Apple Developer account ($99/yr).
- A single-purpose "spinner" utility risks rejection under Apple's "minimum
  functionality" guideline — these simple tools get flagged.

A **Progressive Web App (PWA)** avoids all of that and is the right first move:
- **Usable today** — no review, no store, no account.
- **Feels like a real app** — "Add to Home Screen" gives it a home-screen icon,
  full-screen (no browser bars), and offline use.
- **Data stays on your phone** — the roster lives in local storage; no accounts,
  no privacy concerns with student names.
- **One codebase** can later be wrapped with Capacitor and submitted to the App
  Store if you ever want to, with almost no rewrite.

### Recommendation
Ship the PWA. Revisit a native App Store build only if you specifically want store
distribution — the PWA covers everything you described for classroom use.

## Proposed tech stack (kept deliberately small)
- Plain HTML/CSS/JS or a light Vite setup — no heavy framework needed.
- `localStorage` for wheels + rosters (works offline, private to the device).
- A web app manifest + service worker for install + offline.
- Hosting: a free static host (e.g. Netlify/Vercel/GitHub Pages) so you get a URL
  you open once on your iPhone and "Add to Home Screen."

## Build phases (after mockup approval)
1. **Approve the look** using the mockup, then lock palette/layout tweaks.
2. **App shell** — menu of wheels, wheel screen, editor screen.
3. **Persistence** — save/load wheels to localStorage; seed with your real roster.
4. **Spin + celebration polish** — deceleration feel, confetti/fireworks alternation.
5. **PWA install** — manifest, icons, service worker, offline.
6. **Deploy** — push to a static host, send you the URL to install on your iPhone.
7. **(Optional later)** Capacitor wrap + App Store submission.

## Open questions for later
- Real roster names (import your class list).
- "No repeats until everyone's been picked" mode? (common classroom ask)
- Sound effects on/off?
