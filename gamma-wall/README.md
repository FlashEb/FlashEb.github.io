# Gamma Wall

SPY dollar-gamma heatmap (strike × expiry) from Public.com's live option chain, served at /gamma-wall/.

- `index.html` loads `data/SPY.csv` and re-checks every 5 minutes.
- `.github/workflows/gamma-wall.yml` refreshes the data every 30 minutes on weekdays during US market hours (GitHub can delay scheduled runs by a few minutes).
- Needs repository secrets `PUBLIC_API_SECRET` and `PUBLIC_ACCOUNT_ID` (Settings → Secrets and variables → Actions).
- Run it by hand: Actions → Refresh gamma wall → Run workflow (tick "force" outside market hours).
