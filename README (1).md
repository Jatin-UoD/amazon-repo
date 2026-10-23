# HomePilot — One Home. One App. Total Control.

Smart-home app demo (mobile-first, no backend, no API keys). Works offline in the browser.

## Files
- `index.html` — the HomePilot app
- `ring.html` — Ring Demo Device (simulator that shows a pairing code and sends motion/doorbell events)

## Ring demo sync (no API)
1. Open `ring.html` in one tab and copy the code (e.g. `RING-AB12-CD34`).
2. Open `index.html` → More → Ring Security → paste the code → Sync Ring.
Need a fresh code? Use "Get new code from Ring device" in HomePilot (or "Generate new code" in `ring.html`); the old pairing is removed.
3. In `ring.html` press "Send motion event". HomePilot records it, notifies, and runs the enabled "Motion Light" automation.

Both pages must be open in the same browser on the same site (they talk through localStorage).
This is a **simulated** Ring device. It is not a real Amazon Ring connection; real Ring needs partner access, OAuth and a webhook server.

## Deploy on Vercel
Push to GitHub → Vercel → Add New Project → Framework "Other" → Deploy.
