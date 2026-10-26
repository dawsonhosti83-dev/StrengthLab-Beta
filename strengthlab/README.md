# StrengthLab iPhone PWA

An installable, mobile-first workout and food tracker.

## Run
Host the entire folder on an HTTPS static host (GitHub Pages, Netlify, Cloudflare Pages, etc.). For local testing, from the folder run `python3 -m http.server 8000` and open http://localhost:8000. A local file (`file://`) will not support service workers or camera permissions.

## Install on iPhone
Open the HTTPS URL in Safari, tap Share > Add to Home Screen. Open the saved app icon.

## Features
- Five-day training split with working-set logging, load, reps, RIR, rest, sleep, soreness, readiness, and pre-workout carbs.
- Food diary with gram/ounce serving controls, macros, custom foods, and Open Food Facts barcode lookup.
- Live camera scanning where BarcodeDetector is available; otherwise enter UPC/EAN codes manually. QR contents may not represent product codes.
- Estimated 1RM comparisons and conservative session feedback.
- Local storage plus JSON export/import.

## Limitations
- No user accounts or cross-device sync. Browser storage can be cleared; export backups.
- Camera detection support differs across iOS/browser versions; manual lookup is the fallback.
- Open Food Facts is crowdsourced; always verify nutrition against labels.
- Analysis is descriptive and does not measure central fatigue, recovery state, or predict hypertrophy.
- App icons are SVG; some iOS configurations may prefer PNG icons.
