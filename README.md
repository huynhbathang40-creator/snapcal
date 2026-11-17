# SnapCal

Personal calorie tracker: take a photo of a meal, Gemini estimates calories and macros, and the log is saved on the phone.

- Log meals by photo, by text description (AI), or by typing calories yourself (no AI).
- 100% static (one `index.html`), no server, no database.
- AI: Google Gemini API, called directly from the browser with your own key (free tier).
- Data: stored in the browser's `localStorage` on your device. Use **Settings → Export backup** now and then (the app reminds you every 7 days).
- The API key is NOT in this repo. You paste it in the app's Settings; it stays on your device.

## Setup

1. Get a free key at https://aistudio.google.com/apikey
2. Open the site on your iPhone in Safari → Settings tab → paste the key → **Test key**.
3. Share button → **Add to Home Screen** so it opens like an app.

> Note: the Home Screen app and Safari keep separate storage on iOS. Paste the key and log meals in the same one you plan to use.

## Free tier notes

- Free tier has per-minute and per-day request limits; one person logging meals stays far below them.
- On the free tier Google may use requests to improve its products.
- Default model: `gemini-flash-latest`, with automatic fallback to `gemini-2.5-flash` and `gemini-2.5-flash-lite`.

## Deploy (GitHub Pages)

Static site, no build step. Repo → Settings → Pages → Source: "Deploy from a branch" → Branch `main`, folder `/ (root)` → Save.
The app will be at `https://<username>.github.io/snapcal/`.
