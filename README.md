# World Cup 26 — Bracket Predictor ⚽🏆

An interactive **FIFA World Cup 2026** bracket builder. Pick the final standing of all
12 groups, drag-and-drop to rank the best third-placed teams, then predict every knockout
match from the Round of 32 all the way to the Final.

> Unofficial fan-made project. Not affiliated with, endorsed by, or sponsored by FIFA.

## Features
- **Group stage** — drag to set 1st–4th in each of the 12 groups (A–L)
- **Third-place ranking** — drag-and-drop the 12 third-placed teams; top 8 qualify
- **Config-driven bracket engine** — official R32 mapping from the FWC26 match schedule,
  with constraint-based third-place slot assignment (verified across all 495 qualification combinations)
- **Full knockout flow** — Round of 32 → Round of 16 → QF → SF → Third-Place Match → Final
- **Animated podium** — champion, runner-up, third place
- **Bonus:** 🎲 random generator · 🤖 AI simulate (weighted by FIFA ranking) · 🔗 shareable URL · 🖼️ PNG / 📄 PDF export
- **Persistence** — your predictions are saved in `localStorage`

## Tech
Single self-contained `index.html` — React 18 + Tailwind (CDN), HTML5 drag-and-drop,
html2canvas + jsPDF for export. No build step required.

## Run locally
Just open `index.html` in a browser, or serve the folder:
```bash
npx serve .
```

## Deploy
Static site — deploys to Vercel as-is (no build command, output dir = root).
