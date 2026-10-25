# Today Card

[![live](https://img.shields.io/badge/live-online-22c55e)](https://drsamonline.github.io/today-card/)
[![license](https://img.shields.io/badge/license-PolyForm Noncommercial-blue)](LICENSE)
[![download](https://img.shields.io/github/v/release/drsamonline/today-card


**One card for the day.** Your date, one intention, one task, and a streak.
Offline, no accounts, no telemetry.

Built with **web-kit** and **Forge**.

## What it does

- Shows today's date.
- Lets you write **one intention** and **one task** for the day.
- Keeps a **streak** of consecutive days you filled it in.
- Remembers everything on your device; **Export** writes a CSV of every day.

## Run it

Open `docs/index.html` in a browser. That's the whole app — it works from
`file://`, offline.

## Build the EXE and APK

On every push, GitHub Actions builds a portable Windows EXE and a signed Android
APK (via the shared `app-builder` kit) and attaches them to the `app-latest`
release. See `.github/workflows/build-apps.yml`.

## Structure

```
docs/index.html      the app
docs/web-kit.js      the shared runtime (from drsamonline/web-kit)
```

## Licence

MIT. (c) 2026 Dr Sohil Momin.
