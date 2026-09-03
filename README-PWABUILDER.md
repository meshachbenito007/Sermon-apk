# NJC Sermons — PWABuilder-ready

This project has been prepared as a Progressive Web App (PWA) for PWABuilder.

## Added
- `manifest.json` with app metadata, icons, colors, scope and standalone display.
- `sw.js` service worker with an app-shell cache and offline fallback.
- PWA meta tags and manifest links in `index.html` and `admin.html`.
- 192px, 512px and 1024px PNG app icons in `icons/`.

## Publish first
PWABuilder analyzes a live HTTPS URL. Upload this folder to an HTTPS host (for example your existing web host) and make sure `manifest.json` and `sw.js` are reachable at the same origin.

## Then
1. Open https://www.pwabuilder.com/
2. Enter your public HTTPS website URL.
3. Run the PWA scan.
4. Choose **Android** / Google Play packaging.
5. Download the generated Android package/project and follow its signing/build instructions.

## Important
The Supabase client is loaded from jsDelivr, so sermon/event data still requires network access. The service worker caches the application shell for offline startup; it does not make Supabase data permanently available offline.
