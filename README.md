# university-cal

University deadlines and events, served as an Apple Calendar subscription.

## Subscribe (Apple Calendar)
Settings > Calendar > Accounts > Add Account > Other > Add Subscribed Calendar
URL: https://benjamintia.github.io/university-cal/university-refresh-20261023.ics

## Files
- `university-refresh-20261023.ics` — fresh URL published on 23 Oct 2026 to bypass a stale Apple subscription cache. Subscribe to this one if the existing calendar is not updating.
- `university.ics` — canonical source file; edit this file first.
- `university2.ics` — legacy mirror. Both legacy feeds are kept identical to the fresh URL until the device is confirmed on the new subscription.

## Updating
Edit `university.ics`, then copy it over `university2.ics` and `university-refresh-20261023.ics`, commit all three `.ics` files by name, and push. GitHub Pages rebuilds in about a minute. Keep all three identical until the old subscriptions are confirmed replaced.
