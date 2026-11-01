# RASA Phone Orders dashboard

A single static page (`index.html`) for the RASA by Amelia team: phone orders taken by
the AI phone agent, each checked against Square, and every call with its transcript.

The page holds no data. It asks for a password and loads everything from the
`orders-dashboard` function in the private `rasa-phone-agent` project, which only
answers with the right password (set as `DASHBOARD_PASSWORD` in Supabase).
