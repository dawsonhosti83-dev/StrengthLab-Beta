# StrengthLab Beta v4 — iPhone / GitHub Pages

Version 4.0 — Training, food, hydration and recovery logging (offline-capable PWA).

## Update your existing site safely

1. **Export your current JSON backup** from Settings in the app. Keep it outside Safari, such as in Files or iCloud Drive.
2. Open the GitHub repository: https://github.com/dawsonhosti83-dev/StrengthLab-Beta
3. Go **inside the folder containing your currently functioning `index.html`**. In the latest screenshot this was `StrengthLab-Beta-v3/strengthlab/` in branch `main`, at:
   https://github.com/dawsonhosti83-dev/StrengthLab-Beta/tree/main/StrengthLab-Beta-v3/strengthlab
4. In that folder choose **Add file → Upload files**. Drag the individual files from this package (`index.html`, `app.js`, `styles.css`, `sw.js`, `manifest.webmanifest`, `icon.svg`, and `README.md`) onto the upload area. Commit the changes. **Do not upload the ZIP file itself or create another nested folder.**
5. Wait for the GitHub Pages deployment in **Actions**. Reopen the *same* site URL on your iPhone. If installed on your Home Screen, close it completely and reopen it. If needed, open the site's address in Safari and refresh.

Your last screenshot showed this folder path, so its matching GitHub Pages address would be:
https://dawsonhosti83-dev.github.io/StrengthLab-Beta/StrengthLab-Beta-v3/strengthlab/

If you have moved the app since then, upload to the **current working folder**, not necessarily this example path. Keeping the same URL preserves the browser's access to previous on-device data. Do not clear Safari website data merely to refresh the app.

## Six changes in Beta v4

1. **Theme works across the app.** Updating hue changes dark backgrounds, panels, borders, navigation, accents and all slider thumbs/tracks. More saturated surfaces make the change visible. The hue is persisted. CSS and JS have new cache-busting version identifiers (`4.0`) and the service worker cache is `strengthlab-v4-0`.
2. **Truly blank first-use training split and exercise library.** All seven days begin empty, with no personal split template. Existing accounts keep their saved split; choose **Clear weekly split** in Settings if you want to start over. Users can create muscle groups, then assign them to days. A generic, optional set of original muscle groups and exercises can be restored manually in Settings without populating the weekly schedule.
3. **Recovery is date-specific.** Each tab uses its own date input ID. A new date starts with blank bedtime, wake time, carbs, readiness, soreness and notes, while returning to a logged date reloads its saved check-in. A per-day **Clear check-in** action is available.
4. **Workout entry resets when changing dates.** Muscle, exercise, load, repetitions, RIR and rest fields return to unentered states. Existing workout entries for each date remain safely stored.
5. **Today weekday buttons now select calendar dates.** The day buttons display actual dates for that calendar week; tapping another day updates food calories, macros, hydration, sets and recovery to reflect that date.
6. **Restore original groups works.** It can restore both the optional original muscle groups *and their exercises*, including entries previously removed. If nothing is missing, it explicitly says they're already present.

## Existing features retained

- Nutrition and hydration logging, favorites / recents, custom foods and serving units.
- QR/barcode scanner when supported, photo and manual input fallback. Requires online food database and camera permission in Safari.
- Custom exercise groups and exercise autocomplete; collapsible exercise folders, PR and previous-session data.
- Workout insights based on available logged data; no claims of medical-grade recovery prediction.
- Times between bedtime and wake are **time in bed**, not measured sleep.
- JSON backup and import.

## Compatibility and privacy

The storage key remains `strengthlab-v1`. Upgrading *at the same origin and path* preserves existing workout, food and recovery records, including older saved splits. This is an offline-first local app, not a cloud account; data is specific to that browser/site. Always keep backups. The barcode library and remote product lookups require an internet connection.

The code was syntax-checked with Node.js and exercised in a phone-width Chromium test harness for fresh install, theme changes, blank split, restore groups, date switching, calorie changes, recovery data retention, workout reset and older-data migration. It has not yet been tested on an actual iPhone for this build.
