# Ripe Legal — Hosted Site

Static HTML for the privacy policy and terms of service. Hosted publicly so
App Store Connect and Google Play Console can link to canonical URLs.

## Files

- `index.html` — landing page linking to both documents
- `privacy.html` — Privacy Policy
- `terms.html` — Terms of Service
- `style.css` — shared styling (light + dark mode)

The content here is the same as `app/legal.tsx` in the main repo. When you
update one, update the other (or eventually swap the in-app screen for a
WebView pointed at these URLs).

## Deploy to GitHub Pages (recommended, ~5 min)

1. Create a new **public** GitHub repo, e.g. `ripe-legal`.
2. Copy the contents of this `legal/` folder into the root of the new repo
   (the `index.html` must be at the repo root, not in a subfolder).
3. Push to `main`.
4. Repo Settings → Pages → **Source: Deploy from a branch** → branch `main`,
   folder `/ (root)` → Save.
5. Wait ~1 minute. Your URLs will be:
   - `https://<username>.github.io/ripe-legal/` (landing)
   - `https://<username>.github.io/ripe-legal/privacy.html`
   - `https://<username>.github.io/ripe-legal/terms.html`

## Where to paste the URLs

- **App Store Connect:** App Information → Privacy Policy URL (required) +
  EULA URL (optional, defaults to Apple's standard).
- **Google Play Console:** App content → Privacy Policy.
- **Inside the app:** optionally update `app/legal.tsx` to render a WebView
  pointed at these URLs instead of the inline text. Not required for store
  submission.
