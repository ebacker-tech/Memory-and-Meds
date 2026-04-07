# Memory & Meds Tracker

A shared cognitive health and medication tracking Progressive Web App (PWA) for small care teams and families. Built as a single HTML file — no server, no database, no install required.

---

## Features

- **Shared group access** — everyone uses the same password to see the same data in real time
- **Memory event logging** — log cognitive events with severity (1–10), event type, triggers, and notes
- **Monthly calendar** — color-coded by severity so patterns are easy to spot
- **Medication tracking** — shared medication list, mark-as-taken, and missed-med alerts
- **Alerts** — banner appears for all group members when a severe event (8+) is logged or a medication is missed
- **Manual sync** — tap the Sync button to pull the latest data from your group
- **CSV export/import** — back up and restore your data anytime
- **Dark mode** — automatic, follows system preference
- **iPhone home screen ready** — add to home screen for a full-screen app experience

---

## Setup (GitHub Pages)

### Step 1 — Create a GitHub repository

1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click the **+** icon → **New repository**
3. Name it something like `memory-meds-tracker`
4. Set visibility to **Public** (required for free GitHub Pages)
5. Click **Create repository**

### Step 2 — Upload the file

1. Inside your new repository, click **Add file** → **Upload files**
2. Drag and drop `index.html` onto the upload area
3. Scroll down and click **Commit changes**

### Step 3 — Enable GitHub Pages

1. Go to your repository's **Settings** tab
2. Click **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Set the branch to **main** and the folder to **/ (root)**
5. Click **Save**

### Step 4 — Get your URL

After about 1–2 minutes, your app will be live at:

```
https://YOUR-GITHUB-USERNAME.github.io/memory-meds-tracker/
```

Share this URL with your care team. Everyone who opens it will be able to join your group using the shared password.

---

## How to update the app

When a new version of `index.html` is available:

1. Go to your repository on GitHub
2. Click **Add file** → **Upload files**
3. Upload the new `index.html` — it will overwrite the old one
4. Click **Commit changes**

The update goes live in about 1 minute. Your data is stored separately and will not be affected by updates.

---

## How shared data works

Data is stored in Claude's shared artifact storage, keyed by a hash of your group password. This means:

- **Anyone with the password** can join the group and see all data
- **Data is not tied to a device** — it works on any phone, tablet, or computer
- **The password is the only access control** — choose something your care team will remember but others won't guess
- **The sync button** pulls the latest data from the group — use it after other members have added entries

> **Important:** If you forget the group password, there is no recovery option. Write it down somewhere safe.

---

## Adding to iPhone home screen

1. Open the app URL in **Safari** on iPhone
2. Tap the **Share** button (box with arrow pointing up)
3. Scroll down and tap **Add to Home Screen**
4. Tap **Add**

The app will appear on your home screen with the brain icon and run full-screen like a native app.

---

## Customising medications

The default medications are placeholders. To update them:

1. Sign in to the app
2. Go to the **Meds** tab
3. Use the **×** button to remove any medications you don't need
4. Use the **Add** form at the bottom to add your actual medications and times

Changes are saved immediately and shared with the whole group.

---

## Data privacy

- All data is stored in Claude's artifact storage under an anonymous key derived from your password
- No names, emails, or personal identifiers are stored outside the app itself
- Anthropic may retain storage data subject to their standard data policies
- For sensitive medical data, do not use real names or identifying information in notes

---

## File structure

```
index.html    ← the entire app (one file)
README.md     ← this file (optional, for your reference)
```

No dependencies to install. No build step. Just the one HTML file.
