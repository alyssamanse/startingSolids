# Starting Solids — Deploy to GitHub Pages

This folder is a complete, ready-to-host website. It's **responsive** — it
automatically shows the desktop layout (sidebar navigation) on a computer
and the mobile layout (bottom tabs) on a phone, from the same single URL.

No coding required for the steps below — just uploading files through
GitHub's website.

## What's in this folder
- `index.html` — the page that loads first. It checks your screen width and
  loads either `desktop.bundle.js` or `mobile.bundle.js` accordingly.
- `desktop.bundle.js` — the full sidebar-navigation version (the feeding
  plan, tracker, reports, everything), for screens wider than 820px.
- `mobile.bundle.js` — the phone-optimized version with bottom tab
  navigation, for screens 820px and narrower.
- `manifest.json` — tells iOS this is an installable app, with its icon and
  colors.
- `service-worker.js` — lets the app open even with no signal, once loaded
  once.
- `icon-192.png` / `icon-512.png` — the app icon used on your home screen.

## First-time setup

### Step 1 — Create a GitHub account (skip if you have one)
Go to [github.com](https://github.com) and sign up. It's free.

### Step 2 — Create a new repository
1. Click the **+** in the top right → **New repository**
2. Name it something like `starting-solids`
3. Set it to **Public** (GitHub Pages requires this on the free plan)
4. Don't add a README or .gitignore — leave everything else default
5. Click **Create repository**

### Step 3 — Upload these files
1. On your repository page, click **"uploading an existing file"**
2. Drag in every file from this folder — `index.html`, `desktop.bundle.js`,
   `mobile.bundle.js`, `manifest.json`, `service-worker.js`,
   `icon-192.png`, `icon-512.png` (this README doesn't need to go up)
3. Scroll down, click **Commit changes**

### Step 4 — Turn on GitHub Pages
1. In your repository, click **Settings**
2. In the left sidebar, click **Pages**
3. Under **Source**, choose **Deploy from a branch**
4. Under **Branch**, choose `main` and folder `/ (root)` → **Save**
5. Wait 1–2 minutes, then refresh — you'll get a live URL like
   `https://yourusername.github.io/starting-solids/`

### Step 5 — Try it on both a computer and your phone
- On a computer: open the URL in any browser — you should see the full
  sidebar version.
- On your iPhone: open the URL in **Safari** — you should see the bottom
  tab-bar version.
- To install on your home screen: tap the **Share** icon in Safari →
  **Add to Home Screen** → **Add**.

## Making changes later (the usual workflow)
This is what you'll actually do most of the time, once the site is live:
1. Come back to Claude and ask for whatever change or fix you need.
2. Claude hands you a refreshed copy of this same folder.
3. On your GitHub repository page, upload the changed file(s) the same way
   as Step 3 above — GitHub will ask if you want to replace the old
   versions; say yes.
4. Pages updates automatically within a minute or two.

Your tracked data isn't affected by re-uploading code files — see below.

## A note on your data
Entries you log are saved two ways:
- **Locally on each device**, instantly, as a fast-loading cache.
- **Synced to the cloud** (Cloud Sync, shown on the Data & Backup page) —
  this is what actually keeps your data backed up and shared live between
  your and your husband's devices. It happens automatically within about a
  second of logging something, no button needed.

Re-uploading updated code files never touches either of these — only the
app's code changes, never what you've tracked.

## A note on privacy
The site itself is public (anyone with the link could open it), but that
only means the *app* is visible — not your data. Your tracked entries are
stored in a private cloud database used only by this app (not posted
anywhere public, and not sent to GitHub), plus a local copy on each device
for speed. Don't share the link publicly if you'd rather keep it private
between the two of you.
