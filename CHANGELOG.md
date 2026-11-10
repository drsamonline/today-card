# Changelog

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
