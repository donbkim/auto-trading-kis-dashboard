# Auto Trading KIS Dashboard

Mobile-first public dashboard for the isolated `index_trend` paper strategy. This repository contains no brokerage credentials, account data, Google Sheet ID, or ingest secret.

## Pages setup

1. Push this directory to the `main` branch.
2. In repository Settings → Pages, choose **GitHub Actions** as the source.
3. The checked-in `config.js` contains the public Apps Script `/exec` URL. Update it only when a new deployment URL is created. The URL is public and contains no write credential.
4. The included workflow publishes the root directory whenever `main` changes.

The page reads `doGet?view=dashboard&callback=...` by JSONP so it can consume the Apps Script endpoint from GitHub Pages without exposing a write secret. Do not put `INDEX_TREND_DASHBOARD_INGEST_SECRET` in this repository.
