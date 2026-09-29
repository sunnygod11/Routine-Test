# Routine-Test

ESS routine-test report generator — a single-page, client-side tool that produces a
one-page Thai/English routine-test certificate for inverters connected to the MEA grid
and exports it as a PDF.

- **App:** [`index.html`](index.html) — self-contained static page: no build step, no server,
  no network calls at runtime.
- **Single report:** enter a serial number and pick a model; power rating, firmware version
  and phase count auto-fill from the built-in model database.
- **Batch:** pick **one** model, paste a list of serial numbers separated by commas, spaces,
  semicolons or new lines, then hit *Generate reports*. One serial number downloads a PDF;
  several download as a ZIP.

## Run locally

Open `index.html` in a browser — that is the whole app.

## Deploy on Vercel

1. Import this repo at [vercel.com/new](https://vercel.com/new).
2. Framework Preset: **Other**. Leave Build Command and Output Directory empty.
3. Deploy. The app is `index.html` at the repo root, so the project URL serves it directly —
   no configuration required. [`vercel.json`](vercel.json) only keeps the old
   `/routine_test_report_batch.html` path working.
