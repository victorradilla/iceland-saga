# Iceland 12-Night Saga — Private Edition

Personal Ring Road trip guide. FI 686 departs 22 May 22:00, FI 689 returns 04 Jun 16:45.

## What's in this folder

- `index.html` — the responsive guide with a PIN gate
- `.nojekyll` — tells GitHub Pages to serve the file as-is

## Access

The page is gated with a **4-digit PIN: `0522`** (your departure date).

- Enter once on each device; unlock persists 90 days.
- The PIN check happens in your browser — there's no server. Only the SHA-256 hash sits in the source, not the PIN itself.

## Change the PIN

Open `index.html`, search for `EXPECTED_HASH = `, and replace the long hex string with the SHA-256 of your new code. On a Mac:

```bash
echo -n "1234" | shasum -a 256
```

## Deploy to GitHub Pages

1. Create a public repo at **github.com/new** (e.g. `iceland-trip`).
2. Click **uploading an existing file** on the empty repo page → drag in `index.html`, `.nojekyll`, and this README.
3. Commit → **Settings → Pages → Source: Deploy from a branch → `main` / `(root)` → Save**.
4. ~30 seconds later, open `https://<your-username>.github.io/iceland-trip/` on your phone.

## Update later

Edit `index.html` directly in GitHub's web UI (pencil icon → save) — Pages rebuilds in under a minute.
