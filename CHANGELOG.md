# Changelog

## 1.2.0 — 2026-11-14

### Added — a way for the card to leave the tab

Copy, Share (where the browser has it) and Remind. Remind downloads an .ics with
a daily all-day event, so the reminder lives in the calendar you already look at:
no account, no server, no notification permission, nothing running in the
background. Export already existed; it produced a JSON backup, which is not
delivery.

### Fixed — the streak counted in UTC while the cards were filed locally

`streak()` walked days with `toISOString()`, so before 05:30 IST the loop looked
for yesterday's key, found nothing and reported 0. The card key was fixed for
this in 1.1.0; the streak loop was missed. It now uses the same local `key()`.

### Fixed — the history line dropped the task

Earlier cards showed the intention only, so a day saved with a task and no
intention read "(empty card)". Both are listed now.


## 1.1.0 — 2026-11-10

### Fixed — a saved card could not be opened again

The app showed **today and nothing else**. Save a card on Monday, open the app on Tuesday, and the
words were still in storage and unreachable: no history, no list, no way back. That is the whole
complaint, and it is right — a note you cannot read again is not saved.

- **Every saved card is listed** under today's, newest first, with its date and its intention.
  Click one and it opens: date, intention, task, and a button back to today.
- The list updates the moment you save, so what you just wrote is visibly there.

### Fixed — the day key was UTC, the day shown was local

`new Date().toISOString().slice(0,10)` is the **UTC** date. In India (UTC+5:30) a card written at
02:00 was filed under yesterday while the page said today — saved, and then not where you looked.
The key is built from local date parts now, and a card already saved under the old UTC key for the
same day is adopted rather than orphaned.

### Added

- `VERSION` and this changelog. The repository had neither.
