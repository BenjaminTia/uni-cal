# university-cal

University deadlines and events, served as an Apple Calendar subscription.

## Subscribe (Apple Calendar)
Settings > Calendar > Accounts > Add Account > Other > Add Subscribed Calendar
URL: https://benjamintia.github.io/university-cal/university.ics

## Files
- `university.ics` — the original canonical subscription URL. Keep using this one.
- `university2.ics` — legacy mirror, kept byte-identical to the canonical feed.
- `university-refresh-20261023.ics` — diagnostic cache-bypass copy published 23 Oct 2026; not the preferred subscription. Retain until the device issue is identified.

## Updating
Edit `university.ics`, then copy it over `university2.ics` and `university-refresh-20261023.ics`, commit all three `.ics` files by name, and push. GitHub Pages rebuilds in about a minute. Keep all three identical until the device issue is resolved.
