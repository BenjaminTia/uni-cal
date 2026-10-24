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
All four files carry the SAME uni-only content (byte-identical). Legacy names exist so a device
subscribed to an older address still receives the correct, uni-only scope rather than the
pre-split combined feed.
- `uni.ics` - canonical subscription URL (use this one).
- `university.ics` - legacy name, kept identical to `uni.ics`.
- `university2.ics` - legacy cache-bypass mirror, kept identical.
- `university-refresh-20261023.ics` - diagnostic cache-bypass copy (23 Oct 2026), kept identical.

## Updating
Edit `uni.ics`, copy it over the three legacy names, then stage exactly those files by name:

```
cp uni.ics university.ics; cp uni.ics university2.ics; cp uni.ics university-refresh-20261023.ics
git -c core.autocrlf=false add uni.ics university.ics university2.ics university-refresh-20261023.ics README.md
git commit -m "..." && git push origin main
```

Never use `git add -A`. Feeds must stay pure CRLF, folded at <=75 octets, one VTIMEZONE per TZID,
and must parse cleanly in both `icalendar` and `vobject` before pushing. Verify the live Pages bytes
(HTTP 200, `text/calendar`) after the rebuild.
