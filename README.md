# Spin Picker 🎡

A fun, game-show-style random picker. Push a big button and a wheel spins down to a
random result, then celebrates with confetti or fireworks. Built first for calling on
students in an LDS seminary class, but each "wheel" is just a named list of options, so
it works for anything (who prays today, class treats, review questions, etc.).

## Status
Pre-build. Concept mockup is in [`mockups/spin-picker-mockup.html`](mockups/spin-picker-mockup.html).
See [`docs/decision-and-plan.md`](docs/decision-and-plan.md) for the platform decision and build plan.

## Core features
- Multiple picker wheels, managed from a menu.
- Create / rename a wheel, choose an icon.
- Add and remove options (students or anything).
- Big Spin button → wheel decelerates and lands on a random option.
- Large, legible result popup + alternating confetti / fireworks.

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
