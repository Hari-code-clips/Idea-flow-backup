# Rapid Build Hackathon — Viksit UP

Static frontend for the Rapid Build Hackathon event. Two rooms:

1. **Challenges** — 8 briefs across 3 themes (Arth Shakti, Srijan Shakti, Jeevan Shakti), sourced from `viksit_up_challenges.xlsx`.
2. **Prompts** — the Learn → Widen → Diagnose → Ideate → Brief → Build prompt library, with copy-to-clipboard on every card.

## Stack

Pure HTML / CSS / vanilla JS. No build step. No framework. Drop-in deploy.

## Local preview

```bash
cd site
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy to Vercel

From the `site/` folder:

```bash
npx vercel        # first time
npx vercel --prod # production
```

…or drag-and-drop the `site/` folder at [vercel.com/new](https://vercel.com/new). No framework preset required — Vercel will serve it as a static site. `vercel.json` enables clean URLs (`/challenges` rather than `/challenges.html`).

## Structure

```
site/
├── index.html         # landing / track picker
├── challenges.html    # theme-grouped challenge cards
├── prompts.html       # 6-step prompt library
├── styles.css         # full design system
├── vercel.json
└── assets/
    ├── tata-logo.png
    └── tcs-logo.png
```
