# StrengthLab Beta v6 — iPhone workout and nutrition tracker

StrengthLab is a static installable web app for logging custom training splits, individual and repeated working sets, foods, daily macros, fluids, and recovery. Its data is stored **locally in the browser** using the same `strengthlab-v1` storage key as v1–v5, preserving existing user records when the app is updated **at the same URL**. Always export a backup from Settings before replacing files.

## What is new in v6

1. **Reusable workout templates by weekday:** Select a date/day in the Workout tab. Add any exercise from any custom muscle group and the number of working sets. StrengthLab saves that lineup for the selected weekday. Next time the day comes around, it fills in the most recent logged weight, repetitions, RIR and rest, which can be adjusted. Save/update the whole session with one button. Saving a second time updates the same template-linked set rather than duplicating it. Templates do not overwrite historical workouts and can be edited independently of logged sets. You can also import exercises from a previously logged session. Manual set logging remains available in a collapsible area.
2. **Rest N/A** is available for each template working set and for manual working sets; in the data, `null` means rest was not recorded. It is not treated as 0 seconds in fatigue feedback.
3. **Drink choices remain selected:** The fluid log supports water, sparkling water, coffee, tea, milk, juice, soda, protein shakes, sports and electrolyte drinks, and a custom drink name. Quick-add buttons are explicitly labeled as water. Fluid logging tracks volume only; for drinks with calories, enter nutrition separately as food.
4. **Food tab calorie overview** mirrors the Today calorie goal/protein/carb/fat overview and follows the selected date.
5. **Scanner usability:** Camera scanning has permission/HTTPS/readiness messages and several external script fallbacks. An image from Photos and an iPhone “take barcode photo” input are separate; native BarcodeDetector is used for photos where supported, otherwise a third-party `html5-qrcode` scanner is loaded from a CDN. The numeric-barcode entry remains available. Product metadata comes from Open Food Facts and requires internet. **The camera and photo scanner have not been tested on a physical iPhone.** In particular, iOS Safari typically needs the JavaScript fallback library because native BarcodeDetector is not enabled.
6. **Small iPhone layouts:** Inputs, selectors, cards, and workout set editors use fluid columns and are checked at 320, 375 and 430 px widths.

## Uploading to GitHub Pages

1. **Export a JSON backup** in the existing app: Settings → Download JSON backup.
2. Unzip `StrengthLab-Beta-v6-GitHub-Upload.zip` on your computer. It contains all **seven site files directly at the ZIP root**: `index.html`, `app.js`, `styles.css`, `sw.js`, `manifest.webmanifest`, `icon.svg`, `README.md`.
3. Open your GitHub repository (`dawsonhosti83-dev/StrengthLab-Beta`) and navigate to **the exact folder containing your currently working `index.html`**. Your last screenshot showed `StrengthLab-Beta/StrengthLab-Beta/` (repository / nested folder).
4. GitHub → Add file → Upload files. Select **the seven individual unzipped files**, not a parent folder or ZIP. Replace the existing files and commit.
5. After GitHub Pages finishes deploying, fully close and reopen StrengthLab in Safari. A new `v6.0` script/style URL and service-worker cache name refresh assets.

Keep the same URL path to keep access to the locally saved workouts and meals. Changing directories/URLs changes browser storage scope in some setups. If you change site path, export/import a JSON backup.

## Camera permissions

On a real iPhone, open the GitHub Pages HTTPS website in Safari and tap Food → Scan → Start live scanner. Allow the camera when prompted. If blocked, check Safari website camera permissions. For non-camera devices, use **Take a barcode photo**, **Choose existing photo**, or numeric manual UPC/EAN entry. The external barcode library and Open Food Facts lookup require an internet connection. If the app reports a third-party scanner could not load, inspect content-blocking extensions or network access. A readable, well-lit barcode image improves photo decoding.

## Notes

- The app does not sync workouts or meals to GitHub. GitHub Pages only hosts the software.
- Session feedback highlights correlations, not diagnoses or proof that a factor caused performance changes.
- Estimated 1RM is a derived estimate, not an actual tested maximum.
- A food scanned via Open Food Facts can have incomplete nutritional information; verify the package label before relying on entries.
