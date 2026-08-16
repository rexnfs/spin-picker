# Spin Picker 🎡

A fun, game-show-style random picker. Push a big button and a wheel spins down to a
random result, then celebrates with confetti or fireworks. Built first for calling on
students in an LDS seminary class, but each "wheel" is just a named list of options, so
it works for anything (who prays today, class treats, review questions, etc.).

## Status
**Live** as an installable PWA → https://rexnfs.github.io/spin-picker/
(Add to Home Screen on iPhone for a full-screen, offline app.)

The production app is `index.html` + `manifest.webmanifest` + `sw.js` + `icons/`,
served by GitHub Pages from the `main` branch. The original concept mockup is kept
in [`mockups/`](mockups/); see [`docs/decision-and-plan.md`](docs/decision-and-plan.md)
for the platform decision.

## Core features
- Multiple picker wheels, managed from a menu.
- Create / rename / delete a wheel, choose an icon.
- Add and remove options (students or anything). Saved on-device (localStorage).
- Big Spin button → Big-Wheel drum decelerates and lands on a random option.
- Short lists repeat around the drum so the wheel always looks full-sized.
- Large, legible result popup + alternating confetti / fireworks.
- Per-wheel **No Repeats** toggle: won't pick the same option twice until all
  have been chosen, then it resets (with a manual Reset available too).
- Installable + works offline (PWA).

## Deploy / update
Edit files, then:
```
git add -A && git commit -m "..." && git push
```
GitHub Pages rebuilds automatically (~1 min). Bump the `CACHE` version in `sw.js`
when changing cached assets so installed devices pick up the update.

## Folder layout
```
spin-picker/
├─ README.md
├─ docs/                 # decisions, plans, notes
│  └─ decision-and-plan.md
├─ mockups/              # clickable concept prototypes (no build step)
│  └─ spin-picker-mockup.html
└─ (app/ — added once the mockup is approved)
```
