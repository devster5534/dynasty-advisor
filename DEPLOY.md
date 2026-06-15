# How to Deploy Dynasty Advisor

Single-file static app — no build step, no backend. Takes about 5 minutes.

---

## Step 1 — Push to GitHub

1. Go to [github.com](https://github.com) and create a new repository
   - Name it: `dynasty-advisor`
   - Set it to **Public**
   - Do NOT add a README

2. Open Terminal and run:

```bash
cd "/Users/ddepoint/AI Vault/Projects/Dynasty Advisor/app"
git init
git add index.html
git commit -m "Launch: Dynasty Advisor"
git branch -M main
git remote add origin https://github.com/devster5534/dynasty-advisor.git
git push -u origin main
```

---

## Step 2 — Enable GitHub Pages

1. Go to your repo: `github.com/devster5534/dynasty-advisor`
2. Click **Settings** → **Pages**
3. Under "Branch", select `main` → **Save**
4. Your live URL: `https://devster5534.github.io/dynasty-advisor`
5. Takes about 60 seconds to go live

---

## Step 3 — Test it

Open the URL and confirm:
- App loads and starts fetching data for Devster5534 automatically
- If you have multiple dynasty leagues, a league selector appears
- Roster loads with position cards and dynasty values
- Trade proposals appear (may be empty if your roster is already balanced)
- "Refresh Data" button clears cache and reloads

---

## Making Updates Later

```bash
cd "/Users/ddepoint/AI Vault/Projects/Dynasty Advisor/app"
git add index.html
git commit -m "Update: [describe change]"
git push
```

GitHub Pages rebuilds automatically in ~60 seconds.

---

## Troubleshooting

**"No leagues found"** — The app uses the 2025 NFL season. If your dynasty league is set up under a different year, open `index.html`, find `const SEASON = '2025'` and change it.

**No dynasty values loading** — FantasyCalc may be temporarily down. The app will show roster structure without values and retry on next load. Click "Refresh Data" to try again.

**Wrong team / can't find my roster** — Your Sleeper display name in the league may differ from your username. Click the username chip in the header and re-enter your display name as it appears in Sleeper.
