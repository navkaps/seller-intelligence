# Seller Systems Support Intelligence

## What this is
An on-demand support analysis dashboard for Stripe's seller systems team.
Analyzes Slack channels and produces a HTML dashboard + Google Doc report.

## How to run
```bash
./run.sh
```
Then say: **"run the seller systems support report"**

## What the report does
1. Reads the last 14 days from:
   - `#seller-systems-support`
   - `#gtm-seller-systems-cpr`
   - `#gtm-experience-ask` (verify channel name)
2. Compares Week 1 (days 8–14) vs Week 2 (days 1–7)
3. Identifies top issues, trends, anomalies
4. Produces:
   - Updated `index.html` (this dashboard)
   - New dated section appended to the Google Doc
5. Commits and pushes to GitHub

## Output files
- `index.html` — the dashboard (opens in browser)

## Google Doc
https://docs.google.com/document/d/1Q0TNM5St2dotb4rQ-jHA80EhqKKmeKVk-g0ASn_Bp8g

## Channels
- `#seller-systems-support` (C05FDARJBA4)
- `#gtm-seller-systems-cpr` (C09E79ZK3PS)
- `#stratus-support` (C0AEUHR9UC8)
