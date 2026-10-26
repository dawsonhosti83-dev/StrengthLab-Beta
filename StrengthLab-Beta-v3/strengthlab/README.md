# StrengthLab Beta v3 — GitHub Pages (iPhone)

## Update the existing live app

Repo: https://github.com/dawsonhosti83-dev/StrengthLab-Beta
Live website: https://dawsonhosti83-dev.github.io/StrengthLab-Beta/strengthlab/

**Before uploading:** open your current StrengthLab on your iPhone and choose **Settings → Download JSON backup**. Keep that file safely outside Safari.

Keep the website path the same. Your current repository places the app in the `strengthlab/` folder. Replace its existing files with the files **inside the `strengthlab/` folder of this ZIP**, including the NEW `app.js` and `styles.css`, and updated `index.html`, `sw.js`, `manifest.webmanifest`, `icon.svg`. You can update using Git or GitHub's web UI. Do not upload a ZIP file as-is, or nest another `strengthlab/` inside the current folder. Pages source remains `main` / `(root)`.

Wait for GitHub Pages → Actions deployment to complete, then reopen the same live URL. Safari's installed PWA can cache updates: close the app and relaunch it; if needed visit the URL in Safari and refresh. Do **not** clear site data to force an update until you have exported your backup.

## v3 features

- **Today** tab restored, along with daily calories/macros, split, fluids, sleep and quick links.
- Discreet notifications for additions, removals and preference updates.
- Food list with favorites and recent-food priority; remove saved foods individually (hides bundled example foods), keeping logged diary entries.
- Fully hue-adjustable color palette: backgrounds, borders, buttons, cards, slider track/thumb, active navigation.
- Add/remove muscle groups, customize the seven-day split with checkboxes.
- Expand each muscle group to add/remove exercises and see last session and estimated e1RM PR.
- Exercise input suggestions: matching names first, alphabetical tie-break, tap or keyboard-select.
- **Recovery** tab: a single daily sleep/wake check-in calculates the overnight interval; pre-workout carbs and subjective readiness / soreness are saved once per day.
- Food portions in mass and liquid units, fluid presets and configurable fluid goal.
- Scanner using html5-qrcode (online CDN) with live camera, image file and manual UPC/EAN alternatives. Food data comes from Open Food Facts; verify product labels.
- Insights compare the best logged set of the same exercise on different session dates. Do not interpret the estimated 1RM as a true tested max.
- JSON backup/import. Maintains the v1/v2 localStorage key `strengthlab-v1` on the same origin and URL to retain prior sessions and foods.

## Privacy / known limits

The app does not sync with a server; all food, workout, sleep and fluid records remain in browser localStorage. The app can load offline after installation, but barcode library loading and food product lookup require the internet. iOS Safari camera requires HTTPS, permission and a supported device. Sleep/wake difference is *time in bed*, not measured sleep. Volume is load × reps and is not a direct proxy for muscle growth. Unit volume and unit mass conversions are not interchangeable without density.
