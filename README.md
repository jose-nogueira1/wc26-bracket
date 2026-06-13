# World Cup 26 — Bracket Predictor ⚽🏆

An interactive **FIFA World Cup 2026** bracket predictor. Set the final standing of all
12 groups, drag-and-drop to rank the best third-placed teams, then predict every knockout
match — visualised as a real bracket tree — from the Round of 32 all the way to the Final.

> Unofficial fan-made project. Not affiliated with, endorsed by, or sponsored by FIFA.
> Uses an original crest and the host nations (Canada · Mexico · USA), not FIFA's official emblem.

## Features
- **Gated, step-by-step flow** — finish the groups to unlock 3rd-place ranking, then the knockout, then results. Locked steps show a 🔒.
- **Group stage** — drag to set 1st–4th in each of the 12 groups (A–L)
- **Third-place ranking** — drag-and-drop the 12 third-placed teams; top 8 qualify
- **Visual bracket** — a true left-to-right bracket tree with connector lines converging to a centered Final (plus a List view for easy tapping on mobile)
- **Config-driven engine** — official R32 mapping from the FWC26 match schedule, with constraint-based third-place slot assignment (verified across all 495 qualification combinations)
- **Animated podium** — champion, runner-up, third place
- **Bracket-style export** — PNG / PDF with the 12 group standings on each side and the bracket in the middle (unlocks once the whole bracket, including the 3rd-place match, is complete)
- **Bonus:** 🎲 random generator · 🤖 AI simulate (weighted by FIFA ranking) · 🔗 shareable URL
- **Persistence** — predictions are saved in `localStorage`
- **SEO + link preview** — meta tags, Open Graph / Twitter card (`og-image.png`), and a trophy favicon

## Tech
Single self-contained `index.html` — React 18 + Tailwind (CDN), HTML5 drag-and-drop,
html2canvas + jsPDF for export. No build step required.

## Run locally
Open `index.html` in a browser, or serve the folder:
```bash
npx serve .
```

## Deploy
Static site — deploys to Vercel as-is (Framework: Other, no build command, output dir = root).
See `DEPLOY.md` for the full git + Vercel walkthrough.

## Note on the preview image
`og-image.png` is referenced relatively. Some social platforms prefer an absolute URL —
after deploying you can set `og:image` / `twitter:image` to `https://YOUR-DOMAIN/og-image.png`
for the richest link previews.
