# StrengthLab Beta v5 — exercise library freedom

**What's changed:** No built-in exercise presets are provided on first launch or through the optional muscle group setup. Users can create any muscle groups and exercise names. Autocomplete uses only names saved by the user, and logging a new exercise adds it to their saved list.

**For existing users:** Existing saved exercise names, muscle groups, logs, PRs, nutrition, recovery, and splits are preserved. If earlier versions populated exercises you don't want, visit **Settings → Exercise library → Clear all saved exercise suggestions**. This clears all saved names, including custom ones, but preserves historical workouts and PR records. Re-add any exercises you want. The separate **Add common muscle groups (empty)** option adds only group names; no exercises.

## Updating the GitHub Pages app

1. Back up first: **Settings → Download JSON backup** in your current app.
2. Extract this ZIP on your computer. It contains the seven app files **directly at the root**, not in an additional folder.
3. In your GitHub repository, open the folder where your **currently working `index.html`** is located. Your latest screenshot showed `StrengthLab-Beta/StrengthLab-Beta/` (repo/folder).
4. Choose **Add file → Upload files** and upload the seven extracted files, replacing the old names. **Do not upload the ZIP or an enclosing folder.** Commit the changes.
5. Wait for GitHub Pages deployment, then refresh your app. The JS/CSS asset version and service-worker cache are updated to `5.0` to pick up this release.

**Data note:** This app stores data in your browser at the site URL, not in GitHub. Keep the same URL path to preserve local storage. Export a backup before any folder/URL move or Safari data clearing.
