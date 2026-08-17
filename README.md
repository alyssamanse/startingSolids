# Starting Solids — Deploy to GitHub Pages

This folder is a complete, ready-to-host website. Once it's live at its own
URL, "Add to Home Screen" on your iPhone will work properly, and your tracked
data will actually persist between visits (this is the fix for the storage
issue from Claude — it only happens because this will have a stable,
permanent web address instead of living inside a generated file).

No coding required for the steps below — just uploading files through
GitHub's website.

## What's in this folder
- `index.html` — the page iOS/GitHub Pages loads
- `app.bundle.js` — the entire app (React + your 12-week plan, tracker,
  reports, everything), bundled into one file
- `manifest.json` — tells iOS this is an installable app, with its icon and
  colors
- `service-worker.js` — lets the app open even with no signal, once loaded
  once
- `icon-192.png` / `icon-512.png` — the app icon used on your home screen

## Step 1 — Create a GitHub account (skip if you have one)
Go to [github.com](https://github.com) and sign up. It's free.

## Step 2 — Create a new repository
1. Click the **+** in the top right → **New repository**
2. Name it something like `starting-solids` (the name becomes part of your
   URL, so keep it simple)
3. Set it to **Public** (GitHub Pages requires this on the free plan)
4. Don't add a README or .gitignore — leave everything else default
5. Click **Create repository**

## Step 3 — Upload these files
1. On your new (empty) repository page, click **"uploading an existing
   file"** (a link right on the page)
2. Drag in every file from this folder — `index.html`, `app.bundle.js`,
   `manifest.json`, `service-worker.js`, `icon-192.png`, `icon-512.png`
   (the README doesn't need to go up, that one's just for you)
3. Scroll down, click **Commit changes**

## Step 4 — Turn on GitHub Pages
1. In your repository, click **Settings** (top menu)
2. In the left sidebar, click **Pages**
3. Under "Build and deployment" → **Source**, choose **Deploy from a
   branch**
4. Under **Branch**, choose `main` and folder `/ (root)` → **Save**
5. Wait 1–2 minutes. Refresh the Pages settings page — you'll see a green
   banner with your live URL, something like:
   `https://yourusername.github.io/starting-solids/`

## Step 5 — Add it to your iPhone home screen
1. Open that URL in **Safari** on your iPhone (must be Safari, not Chrome —
   this only works in Safari on iOS)
2. Tap the **Share** icon (square with an arrow, bottom of the screen)
3. Scroll down and tap **Add to Home Screen**
4. Tap **Add**

You now have an app icon on your home screen. Tapping it opens full-screen,
no browser bar — it behaves like a real installed app.

## Bringing over your existing data
If you already tracked foods in the Claude version, do this once, right
after your GitHub Pages site is live:
1. Open the **old** Claude version → **Data & Backup** → Copy to Clipboard
   (or Download .json)
2. Open the **new** GitHub Pages version → **More → Data & Backup** →
   paste that into the Import box → **Import & Replace**

From that point on, everything you log in the GitHub Pages version will
actually stick around between visits — that's the whole point of moving it
here.

## Making changes later
If you ever want text or behavior changed, come back to Claude, ask for the
update, and it'll hand you a refreshed `app.bundle.js` (and any other
changed files) — just re-upload the new version(s) to the same GitHub
repository (Settings aren't affected, just drag the new file in and commit
again) and GitHub Pages updates automatically within a minute or two.

## A note on privacy
Once this is on GitHub Pages, the site itself is public (anyone with the
link could open it), but **your tracked data is not** — it's stored only in
your iPhone's browser storage, never sent to GitHub or anywhere else. Just
don't share the link somewhere public if you'd rather keep it private
between the two of you.
