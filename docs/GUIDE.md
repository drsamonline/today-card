# Today Card — user guide

**Version 1.1.0 · PolyForm Noncommercial 1.0.0**

One card for the day: the date, one intention, one task, and a streak of the days you filled it in.

## What it does

- Shows today's date.
- Lets you write **one intention** and **one task** for the day.
- Keeps a **streak** of consecutive days you filled it in.
- Remembers everything on your device.
- **Earlier cards** — a history list, so a past day can be read back rather than overwritten.
- **Export** writes a CSV of every day.

## The one thing to know

The day key is **local**, not UTC. A card filled at 11 pm belongs to that day, not to tomorrow
because a server somewhere had already rolled over. Cards written before this behaviour existed are
adopted rather than orphaned.

## Why one intention and one task

Because a card with ten lines is a to-do list, and a to-do list is a thing you fail at rather than a
thing you read. One of each is small enough to finish and specific enough to remember.

## Your data

It lives on the device. Export the CSV if you want it elsewhere — and do that before clearing site
data, because the browser is the whole database.

## Licence

PolyForm Noncommercial 1.0.0. See [LICENSE](../LICENSE).
