# Prep Register — JEE

A lightweight, single-file web app for tracking JEE prep: an error log (chapter-wise, marked A/B/C), spaced revision sessions, mock test scores, a daily checklist, announcements/notices, and quick links to other study apps.

No backend, no build step — just HTML, CSS, and vanilla JavaScript. All data is stored locally in your browser via `localStorage`, so your data stays on your device.

## Features

- **Error Log** — Log every question you get wrong or find tricky, tagged by subject and chapter, marked A (wrong), B (tricky), or C (easy). Filter by subject and drill into any chapter to see every logged question.
- **Revision** — Track revision sessions grouped by subject and chapter, tagged by type (HW, Error Log, PYQ, Reference, Other), with attempted/correct counts and accuracy per chapter.
- **Tests** — Log mock test scores, subject-wise splits, and key mistakes to fix.
- **Checklist** — A daily task list with priorities and fixed/flexible time slots.
- **Notices** — Pin important announcements/reminders to the top of the app.
- **Apps** — Quick-launch shortcuts to other study tools/resources you use.
- **Streak tracker** — Keeps a running streak of days you've logged activity.

## Getting started

Since this is a static single-page app, you have a few options:

### Option 1: Open directly
Just open `index.html` in your browser. Everything works locally.

### Option 2: Serve locally
```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

### Option 3: GitHub Pages
1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Set the source branch to `main` and folder to `/ (root)`.
4. Your app will be live at `https://<your-username>.github.io/<repo-name>/`.

## Add to Home Screen (mobile)

The app is a full installable PWA:
- **Android/Chrome**: open the site → menu (⋮) → **Install app**. It installs with its own icon, opens without browser chrome, and works offline (thanks to `sw.js` caching the app shell).
- **iOS/Safari**: open the site → Share → **Add to Home Screen**.

## Repo structure

Every file lives at the root of the repo — no subfolders needed:

```
index.html            — the app itself
manifest.json         — PWA metadata (name, icons, theme color) so it's installable
sw.js                 — service worker; caches the app shell for offline use
icon-192.png          — app icon (192px)
icon-512.png          — app icon (512px)
apple-touch-icon.png  — icon used by iOS "Add to Home Screen"
```

## Data & privacy

All data (questions, tests, revisions, tasks, announcements) is stored **only** in your browser's `localStorage` — nothing is sent to a server. Clearing your browser data or switching devices/browsers will reset the app. There is currently no export/import or cloud sync.

## Tech stack

- Plain HTML/CSS/JavaScript (no frameworks, no build tools)
- Google Fonts (Bitter, IBM Plex Mono, Inter)
- Browser `localStorage` for persistence

## License

MIT — see [LICENSE](LICENSE).
