# StrengthLab Beta v7 — iPhone / GitHub Pages

A personal, local-first exercise, food, hydration, and recovery logging web app.

## New in v7

- **Editable repetition ranges:** Set a default min/max in Settings or Training Intelligence (1–50 reps). In Training Intelligence, select any saved custom muscle group to set its own optional override, or return to the default. Session feedback checks those ranges.
- **Custom muscle group progress:** Training Intelligence lets you filter to every custom group (including groups present in historical records), review direct sets in the selected 7-day window versus the preceding 7 days, select a logged exercise, and view estimated best strength and last-session trends for that exercise. It never blends unrelated exercises into one strength score.
- **Custom foods use Serving Size:** Enter an amount and a mass or volume unit, optional descriptive name (e.g. “1 scoop”), then enter calories, carbs, protein and fat **for that serving**, not per 100 units. Unit conversions remain available when logging. Previously saved foods still use their existing nutritional values correctly.
- **Blank goals on fresh installs:** Calorie, protein, carbohydrate and fluid goals (and body weight) start empty. Empty goals show "Not set" instead of 0% or an invented target; they can be cleared later in Settings. Existing saved goals remain unchanged.
- **Food log resets:** After saving a food to the diary, the selected food, portion, meal choice, and search fields reset. It does **not** delete the saved food or diary history. The food remains available for quick re-selection.
- Retains the v6 workout template, camera/photo scanning, fluid types, theme picker, date-aware food totals and Recovery tab.

## Update on GitHub Pages

1. **Important:** From your existing running app go to **Settings → Download JSON backup**, and save it outside Safari.
2. Extract this ZIP. It contains the seven app files **at the root** of the archive, not an enclosing `strengthlab` folder.
3. In your GitHub repository, find the **existing `index.html` that is currently serving the live app**. Upload and replace the files **in that same directory**; do not create a `StrengthLab-Beta-v7` or `strengthlab-v7` folder.
4. Commit changes and check the GitHub Actions deployment; refresh your Safari web app. If Safari keeps showing the old version, close and reopen it (and refresh in Safari). The service-worker cache version and assets are bumped to v7.
5. Your training and food data uses the same browser local-storage key (`strengthlab-v1`) as previous releases, provided the **origin and URL path stay unchanged**.

### Notes

- This is an installable web app, not an App Store application. Hosting on GitHub Pages uses HTTPS. The app has not been tested on a physical iPhone.
- Nutrition and hydration records are stored on that browser only. Export backups regularly; moving to a different GitHub Pages URL/path may make past locally saved data inaccessible from the new address.
- Camera scanning depends on Safari permission, device support, a scanner script from an external CDN, and an internet connection for product lookup. Manually entering a barcode remains an alternative.
- Estimated 1RM and training feedback are descriptive performance signals, not direct measures of muscle growth or diagnoses of fatigue. Individual effort, range of motion and technique can alter these estimates.
