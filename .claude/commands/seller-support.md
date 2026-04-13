Run the full Seller Systems Support Intelligence report.

Steps:
1. Read the last 14 days of messages from #seller-systems-support (C05FDARJBA4), #gtm-seller-systems-cpr (C09E79ZK3PS), and #stratus-support (C0AEUHR9UC8). Split into Week 1 (days 8-14 ago) and Week 2 (days 1-7 ago). For every top-level message with replies, fetch the full thread.
2. Try running the combined SFDC + Slack Hubble query first (see SKILL.md for SQL). If it fails due to permissions, fall back to Slack-only via MCP.
3. Analyze all messages and SFDC cases: categorize issues, count frequency per category per week, identify trends, surface anomalies, flag escalations. Read full threads before assigning root cause or resolution status.
4. Compare week over week: what increased, decreased, is new, persisted.
5. Produce a BLUF (3-5 sentences: what's critical, what to do now, key metric). Include SFDC WoW trend if available.
6. Produce Stratus Deep Dive and Approvals Deep Dive sections.
7. Before writing new INLINE_DATA: read the current index.html and extract the existing total W2 ticket count — set that as `meta.prev_w2_total` in the new data (powers the diff badge). If none exists, set to null.
8. Update /Users/navin/seller-intelligence/index.html with fresh INLINE_DATA — new run date, updated KPI tiles, WoW chart data, issue table, watchlist, BLUF, SFDC section, Stratus Deep Dive, Approvals Deep Dive, Critical Quotes.
9. Update Harbor prototype hbrprt_UJQeDbTQFJQgm1: call get_harbor_prototype_draft, replace only the JSON after `const D=` with the new INLINE_DATA, call update_harbor_prototype.
10. Open http://localhost:8080/ (start `python3 -m http.server 8080 &` if not running). Do NOT commit, push, or publish to pages.stripe.me.
