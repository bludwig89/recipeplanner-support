# Recipe Planner — Support Site

This is the public support page for the Recipe Planner iOS app. It doubles as the
**Support URL** and **Privacy Policy URL** required by App Store Connect.

The site has two tabs:
- **Support** — app description, support contact (benludwig6382@gmail.com), and an FAQ (restore purchases, import recipes, camera scan, serving multiplier, sync, sharing, importing from other apps).
- **Privacy** — full privacy information: what the developer can/can't see, how CloudKit storage works, no-tracking statement, and data recovery. Deep-linkable at `.../#privacy`.

Files (keep both in the repo root):
- `index.html` — the page (no build step, no dependencies)
- `AppIcon.svg` — the app icon shown in the header (referenced by `index.html`)

## Deploy to GitHub Pages (~5 min)

1. Create a **public** repo on GitHub named `recipeplanner-support`.
2. Upload `index.html` (and this README) to the repo root, or push it:
   ```bash
   cd recipeplanner-support
   git init
   git add index.html AppIcon.svg README.md
   git commit -m "Recipe Planner support page"
   git branch -M main
   git remote add origin https://github.com/<yourusername>/recipeplanner-support.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Set branch to **main** and folder to **/ (root)**, then **Save**.
6. Wait ~1 minute. Your page goes live at:
   ```
   https://<yourusername>.github.io/recipeplanner-support/
   ```

## Use in App Store Connect

Paste the live URL into both fields:
- **Support URL** — required
- **Privacy Policy URL** — required (same page is fine; the privacy section is included)

The **Marketing URL** is optional — leave blank for v1.0.

## Updating

Edit `index.html` and push again. GitHub Pages redeploys automatically within a minute.
Remember to bump the "Last updated" date in the Privacy Policy section when the privacy
terms change.
