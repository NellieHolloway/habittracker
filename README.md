# The Almanac

A quiet ledger of daily practices — a single-page habit tracker that installs as a desktop app.

![The Almanac](icon-192.png)

## What it does

- **Track habits** with flexible schedules: every day, specific weekdays (e.g. Mon/Wed/Fri), or N times per week
- **Set goals** with optional end conditions: for N days, or until a specific date — habits auto-archive when complete
- **See your patterns** in an annual heatmap, weekday-by-weekday completion chart, 12-week trend, and per-habit detail views with 18-week history
- **Browse the archive** to revisit completed or paused habits — restore any of them back to active
- **Keep your data** — everything lives in `localStorage` on your device; export/import as JSON anytime
- **Works offline** once installed

## Install as a desktop app

The fastest path, no command line needed:

1. **Download this repo** as a ZIP (green "Code" button → "Download ZIP") and unzip it
2. **Create a new repo on GitHub** — call it anything (`almanac`, `my-habits`, etc.)
3. **Upload the files**: on the new empty repo's page, click "uploading an existing file" and drag every file from the unzipped folder into the browser. Commit.
4. **Enable GitHub Pages**: Settings → Pages → Source: "Deploy from a branch" → Branch: `main`, folder: `/ (root)` → Save
5. **Wait ~30 seconds**, then visit `https://YOUR-USERNAME.github.io/REPO-NAME/`
6. **Install it**: in Chrome, Edge, or Brave, look for the install icon in the address bar (a small monitor with a down-arrow) and click it. The Almanac opens in its own window from then on. You'll also see a gold "Install" button in the app's toolbar.

On macOS Safari, use *File → Add to Dock*. On iOS, use the share menu → *Add to Home Screen*.

The installed app behaves like any native app: own window, dock icon, no browser chrome, works offline.

## How updates work

Push changes to the repo → GitHub Pages republishes within a minute → the service worker fetches the new version on next launch. You'll see the new version after one reload.

If you ever want to force-refresh, the installed app has a menu (three dots in some browsers, right-click in others) with a "Reload" option, or you can uninstall and reinstall.

## Local use

Just open `index.html` in any modern browser. The install/offline features need HTTPS hosting, but the app itself works fine from `file://` — you just won't get the install prompt or the service worker.

## Keyboard shortcuts

| Key | Action |
|---|---|
| `N` | New habit |
| `1`–`9` | Toggle habit by position |
| `←` / `→` | Previous / next day |
| `Esc` | Close modal |

## Backup

Use the **Export** button regularly. Your data lives in `localStorage`, which is per-browser and per-device — if you clear browser data or switch machines, the export is your only way to recover. The exported JSON can be imported on any device.

## File overview

```
index.html       The whole app — HTML + CSS + JS in one file
manifest.json    PWA manifest (name, icons, display mode)
sw.js            Service worker — caches assets for offline use
icon-192.png     App icon (small)
icon-512.png     App icon (large, for splash screens)
favicon.png      Browser tab icon
```

## Tested in

Chrome, Edge, Brave (full PWA install + offline). Firefox (works, but install support varies by version). Safari (works; "Add to Dock" available on recent macOS).
