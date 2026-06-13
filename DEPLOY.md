# Deploying

This is a static site — just `index.html` plus assets. No build step.

## Option A — push to GitHub, then Vercel auto-deploys

```bash
cd wc26-bracket
git add .
git commit -m "Update bracket predictor"
git push          # if the repo + Vercel git integration are already set up
```

First time only — create and connect the repo:

```bash
git init
git add .
git commit -m "Initial commit"
gh repo create wc26-bracket --public --source=. --remote=origin --push
```

Then at https://vercel.com/new → Import `wc26-bracket` → Deploy.
(Framework: **Other**, Build command: **none**, Output directory: **/**.)

## Option B — deploy straight from the terminal

```bash
cd wc26-bracket
npx vercel --prod
```

## Option C — no terminal

Drag the `wc26-bracket` folder onto https://vercel.com/new.

## After deploying
For the best link previews, edit `index.html` and set the two image tags to your live URL:

```html
<meta property="og:image" content="https://YOUR-DOMAIN/og-image.png" />
<meta name="twitter:image" content="https://YOUR-DOMAIN/og-image.png" />
```
