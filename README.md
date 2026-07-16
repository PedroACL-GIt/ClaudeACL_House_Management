# Homekeeper

A house-management app for iOS — track repairs, recurring maintenance, tools and trades
for every home you look after.

It's built as an **installable PWA** (Progressive Web App): open it in Safari on your iPhone,
then **Share → Add to Home Screen**. It then launches full-screen like a native app, works
**offline**, and keeps your data on the device.

## What's improved over the original

- **Mobile-first, native iOS design** — bottom tab bar, large titles, grouped lists,
  bottom sheets, iOS switches, and full **light / dark mode** (auto or forced).
- **Job history & cost tracking** — "Mark done" logs the date, cost and a note, then
  reschedules the next occurrence automatically.
- **Spending dashboard** — total spend for the year and all-time, broken down by category.
- **Trades & contacts per home** — save your plumber, electrician, gardener etc. with
  tap-to-call phone numbers.
- **Photos on jobs** — attach a photo (auto-downscaled so it stays small on device).
- **Priorities** — flag jobs High / Normal / Low; safety items default to High.
- **Search** across every job, home and room.
- **Backup & restore** — download a JSON file or copy/paste, plus restore.
- **Currency** switch (£ / $ / €).
- Smart defaults: new homes are pre-filled with whole-house safety/maintenance jobs
  (smoke alarms, gutters, filters, extinguisher check); a Garden room pre-fills seasonal jobs.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire app (HTML + CSS + vanilla JS, no build step) |
| `manifest.json` | PWA manifest (name, icons, standalone display) |
| `sw.js` | Service worker for offline caching |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | App icons |

## Running it

Any static host works (GitHub Pages, Netlify, or a local server). Locally:

```bash
python3 -m http.server 8000
# then open http://localhost:8000 on your phone (same network) or desktop
```

A service worker requires HTTPS (or `localhost`) to register, which is what enables
offline use once the app is added to the Home Screen.

## Data & privacy

All data is stored locally on your device (`localStorage`). Nothing is sent anywhere.
Use **More → Backup & restore** to move data between devices.
