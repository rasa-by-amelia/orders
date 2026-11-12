# RASA Phone Orders dashboard

A single static page (`index.html`) for the RASA by Amelia team: phone orders taken by
the AI phone agent, each checked against Square, and every call with its transcript.

The page holds no data. It asks for a password and loads everything from the
`orders-dashboard` function in the private `rasa-phone-agent` project, which only
answers with the right password (set as `DASHBOARD_PASSWORD` in Supabase).

## RASA Insights (`insights/`)

A second page at `/orders/insights/` for the owners: sales, customers, and Google and Meta
ads, with daily insights. It also holds no data: it loads everything from the
`insights-dashboard` function, which needs its own password (`INSIGHTS_PASSWORD`), separate
from the staff password above.

## RASA Food cost (`insights/cogs/`)

The owners' food cost (COGS) page at `/orders/insights/cogs/`: supplier receipts (photo or
PDF, read by Claude, checked and confirmed by an owner), ingredients and their prices. Same
password as Insights. It holds no data: everything comes from the `cogs` function, and
receipt photos stay in a private Supabase Storage bucket (the page gets 10-minute links).
