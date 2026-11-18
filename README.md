# SupeRR Pressure Rankings

Interactive dashboard for **SupeRR Selector Season 2, Round 1** — ranking T20 batters and bowlers who perform best under pressure.

## What's Inside

- **`index.html`** — Self-contained dashboard with all data, charts, and methodology. Open in any browser.

## Features

- Top 10 batters and bowlers ranked by pressure performance
- Interactive charts (Chart.js): ratings with 90% bootstrap CIs, pressure distribution by over, SR/economy scatter plots
- Full methodology walkthrough (win-probability models, Pressure Index, RAE, shrinkage, composite rating)
- Split-half reliability analysis
- Card and table views with top-30 extended rankings
- Light and dark theme support, responsive layout

## Data

842 T20 matches (IPL 362, T20I 450, other 30), 199,029 deliveries, 2022-2026.

## Method Summary

1. Win-probability model (out-of-fold HistGradientBoosting, chase AUC 0.896)
2. Pressure Index = Leverage Index x Momentum x Stakes
3. Expected outcomes via ML — Runs Above Expected (RAE)
4. Empirical-Bayes shrinkage for fair comparisons
5. Composite: 50% PW-RAE + 25% cWPA + 15% consistency + 10% clutch delta
6. Bootstrap robustness (300 resamples) + 15 sensitivity scenarios
