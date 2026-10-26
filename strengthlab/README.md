# StrengthLab Beta v2 — GitHub Pages

## Update your existing GitHub Pages app

Your current repository is `dawsonhosti83-dev/StrengthLab-Beta`. Your previous upload placed all app files inside the `strengthlab/` subfolder. **Keep the same location** when updating to preserve the existing website URL and browser localStorage data.

1. **Back up your current data first:** in the old app open Settings > Export JSON backup.
2. Download and unzip `StrengthLab-Beta-v2.zip`.
3. In your GitHub repository, replace `strengthlab/index.html`, `strengthlab/sw.js`, `strengthlab/manifest.webmanifest`, and `strengthlab/icon.svg` with the corresponding files from the extracted `strengthlab` folder. The GitHub web editor can edit each file individually, or use Git to commit the files.
4. Ensure GitHub Pages publishes the `main` branch from `/ (root)`.
5. Open `https://dawsonhosti83-dev.github.io/StrengthLab-Beta/strengthlab/` in Safari. Refresh after GitHub Pages finishes deploying; if the old app persists, close and reopen it or clear this site's cached data **only after exporting a backup**.

## What's new
- Collapsible muscle groups with example exercises, estimated e1RM PRs, and last logged set.
- Editable seven-day split in Settings. Existing workouts remain saved.
- Food favorites and recently logged food priority.
- Food serving sizes: g, oz, kg, lb; liquid mL, L, fl oz, cups, tablespoons, teaspoons; and custom serving sizes. Volumetric units are offered for liquid foods only (no unsupported density conversions).
- Fluid log in Food and Today.
- Accent hue slider in Settings.
- Camera scanning fallback for iOS Safari via html5-qrcode CDN; requires HTTPS, camera permission, and internet. Manual barcode entry remains available.

## Notes
- Existing local data uses the same `strengthlab-v1` localStorage key, to preserve it when updating the **same URL**. Always export a backup first.
- Product nutrition uses Open Food Facts. Verify labels and serving sizes. Some products may have incomplete data.
- The scanner fallback loads from `unpkg.com` when used; if blocked or offline, enter the barcode manually.
- e1RM estimates are not verified PRs and can be inaccurate for isolation lifts.
- No accounts or cloud synchronization; browser data is local to the device.
