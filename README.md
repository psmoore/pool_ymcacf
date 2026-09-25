# YMCA of Central Florida aquatics — Pool Relay embed preview

A mockup of a central aquatics section for [ymcacf.org](https://ymcacf.org/): one live
[Pool Relay](https://www.poolrelay.com) calendar covering all fourteen Y pools, plus a page per program.
The real site spreads this across fourteen location pages, fourteen class-schedule widgets, a lesson
finder that searches one program at a time, and swim team pages whose practice times sit behind an
interest form.

Not an official YMCA of Central Florida page. It says so in a ribbon across the top.

Built with `python3 build.py` (the chrome lives there; edit it, not the HTML) and served by GitHub Pages.

## The pages

| Page | Calendar | Scoped to |
|---|---|---|
| `index.html` — Find a swim time | [`zhzk448T…`](https://www.poolrelay.com/v/zhzk448Thgeod0PjWntw82) | every pool, one day, one row per pool; **Teams** menu picks a program |
| `lap-swim.html` | [`oIqQALO9…`](https://www.poolrelay.com/v/oIqQALO9J4LAqlhYZCvYpv) | lap swim, pools that have it |
| `swim-lessons.html` | [`CjkIGvPP…`](https://www.poolrelay.com/v/CjkIGvPPrv5ZqlNdFNzG8C) | group lessons at 11 Ys; **Practice Groups** menu picks a level |
| `swim-team.html` | [`T2pTbHBy…`](https://www.poolrelay.com/v/T2pTbHBy00qUJanIgYhGmi) | the two swim team schedules that are published (Winter Park, Dr. P. Phillips) |
| `water-fitness.html` | [`MQnVkkXr…`](https://www.poolrelay.com/v/MQnVkkXruVn39uYNJiyHYE) | water fitness at 12 Ys |
| `open-swim.html` | [`tFHqGU9M…`](https://www.poolrelay.com/v/tFHqGU9MMALSmd1fjzDvcm) | Downtown rec swim, splash pads, feature pools |
| `locations.html` | [`e3kuZyCt…`](https://www.poolrelay.com/v/e3kuZyCtwPu86rA2JFVHqa) | one Y, the whole week; **Facilities** menu, opens on Winter Park |

## Sources (read 2026-09-24)

- **Pool hours**: each location page's hours list (`ymcacf.org/locations/<slug>/`).
- **Classes**: each location's Family Center Schedule, a Technogym mywellness class timetable
  (`services.mywellness.com/Core/Facility/<id>/SearchCalendarEvents`). Only pool rooms and water classes kept.
- **Swim lessons**: the program finder behind the lesson pages
  (`ymcacf.my.salesforce-sites.com/services/apexrest/YmcaEvents?tag=…`), tags Swim Starters, Preschool
  Stage 1–4, School Stage 1–6 and Teen Adult Swim Lessons: 424 sessions, Oct 17 – Dec 15.
- **Swim teams**: the Developmental and USA Swim Team pages (locations and prices; no times).

The locations page lists 18 sites: 14 family centers with pools, Parrish Health & Fitness (no pool) and
three early-learning centers.

## What is ours

- **Lap Lanes and Program Area.** No Y says which lanes lap swim keeps while lessons and classes run, so
  each main pool is split in two: pool hours show as lap swim in *Lap Lanes*, lessons and classes in
  *Program Area*. Downtown's indoor pool also has an *Open Swim Area* for its recreational swim.
- **Pool hours as lap swim** at twelve Ys. Roper and Winter Park publish lap swim on their class
  schedules, and those times are used instead (open-ended; Roper's feed ends Oct 30 – Nov 4).
- **Lessons grouped by time slot.** Levels that start at the same time at the same Y are one calendar
  block (203 blocks for 424 sessions), tagged with every level in it, so the level menu still filters.
  Each block lists open spots per level as of Sept 24.
- **Osceola**: Friday lap swim "3:00 am – 5:45pm" entered as 3pm. Sunday Stage 5 (listed as ending
  Nov 18) and Sunday Teen/Adult (listed as ending Nov 1) both entered as four Sundays from Oct 18; the
  Stage 5 session is merged with Stages 4 and 6 at the same time.
- **Frank DeLuca** Thursday/Friday Water Fitness is listed in Studio A; entered in the pool.

## Open questions (also on the hub page)

| | |
|---|---|
| **Conflict** | Winter Park: open lap swim until 7pm and swim team 4–7pm Tue–Thu in the same Lap Pool. Left flagged. |
| **Conflict** | Dr. P. Phillips Developmental Swim Team is listed Mon/Tue/Thu 7:30–8:30 **am**. Left flagged. |
| **Conflict** | Roper pool hours vs. its class schedule's lap swim (Tue/Thu mornings, 4–5pm). |
| **Conflict** | Leonard & Marjorie Williams Tuesday Teen/Adult lessons 7:00–7:30pm; pool listed open until 7pm. |
| **Gap** | Swim team times for 9 of 11 Developmental locations and all 5 USA Swimming locations. |
| **Gap** | Osceola and Wayne Densch class schedules are empty. |
