---
name: wasted-spend
description: Find campaigns, ad sets and ads that spend without profitable sales in ROASaurus and propose pauses or budget cuts for approval. Use when the user asks about wasted ad spend, ads without sales, or what to pause.
---

# Wasted spend

1. Period: the last 14 days unless the user gives one. Use at least 7 days so a slow week does not decide.
2. `ad_performance` and `campaign_profit` for the period: keep entities with spend above zero and no attributed orders, or profit after ad spend below zero.
3. Check `attribution` with a longer click window before calling something wasted: view-through and late conversions can change the picture (`view_through`).
4. Show the list: entity, platform, spend, orders, profit after ads, and why it qualifies.
5. Only for the entities the user confirms: `propose_action` with kind `pause` (or `budget` with a lower value), a short reason and the evidence. With the `actions:apply` scope, use `apply_action` only when the user asked to apply right away.
6. Report each proposal's status as the tool returns it.
