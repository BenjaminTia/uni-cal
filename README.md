# uni-cal — University calendar (coursework only)

Coursework, classes, exams and school administration, served as an Apple Calendar subscription.
Career, competition, hackathon, networking and extracurricular items live in the separate
**career-cal** feed: https://benjamintia.github.io/career-cal/career.ics

Canonical feed (repo renamed from `university-cal` on 24 Oct 2026):

```
https://benjamintia.github.io/uni-cal/uni.ics
```

## Subscribe (Apple Calendar)
Settings > Calendar > Accounts > Add Account > Other > Add Subscribed Calendar, then paste the
canonical URL above. On a device still subscribed to the old
`https://benjamintia.github.io/university-cal/university.ics` address, edit the subscription to the
new URL - the old Pages path belongs to the pre-rename repo and is not a permanent alias.

## What belongs here
- Classes, lectures, labs, tutorials, day schools, tests, exams, exam periods
- Coursework assessments and their work blocks / DUE markers
- Course administration: group lists, enrolment records, tuition, language-course enrolment
- University infrastructure notices (IT outages, campus power shutdowns)
- Academic advising, FYP scoping, correspondence with course staff
- Coursework progress CHECK banners

Everything else - hackathons, competitions, scholarship/bursary applications, internships,
networking events, campus talks and workshops, professional-body membership - belongs in
`career-cal`. A dated item is added to exactly one of the two feeds.

## Files
- `uni.ics` is the only supported feed. The owner confirmed the new subscriptions work and authorised retirement of all legacy aliases and outdated calendar snapshots on 24 Oct 2026.
- Backups are kept privately outside this public repository. Old files remain in Git history; history has not been rewritten.

## Updating
Edit `uni.ics`, then stage only the changed canonical file and documentation by name:

```
git -c core.autocrlf=false add uni.ics README.md
git commit -m "..." && git push origin main
```

Never use `git add -A`. Feeds must stay pure CRLF, folded at <=75 octets, one VTIMEZONE per TZID,
and must parse cleanly in both `icalendar` and `vobject` before pushing. Verify the live Pages bytes
(HTTP 200, `text/calendar`) after the rebuild.
