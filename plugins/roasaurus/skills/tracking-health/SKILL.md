---
name: tracking-health
description: Diagnose missing or low conversions on ad platforms with ROASaurus (setup status, delivery to Meta, Google Ads, TikTok and others, consent, matched orders). Use when the user says conversions are missing, the ad platform reports fewer sales, or asks whether tracking works.
---

# Tracking health

1. With the `admin:read` scope: `store_setup_status` and `diagnose_store` (optionally for one platform). They list the likely causes, each with the next step and who can take it.
2. Without it: `ad_performance` and `attribution` show whether orders reach each platform; `web_analytics` shows storefront traffic and consent.
3. Steps marked who=merchant need the merchant's own login or clicks (Shopify app embed, ad platform logins, billing): say so, never claim they were done.
4. Settings changes (consent, attribution) only with `admin:write` and only when the user asked for that change.
