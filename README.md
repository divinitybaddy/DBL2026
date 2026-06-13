# 🏸 TournamentHub

A mobile-friendly, live-scoring tournament manager that works entirely in the browser.  
**No server. No database. No install.** Just a single HTML file hosted on GitHub Pages.

---

## 🚀 Deploy to GitHub Pages (5 minutes)

### Step 1 — Create the repository

1. Go to [github.com/new](https://github.com/new)
2. Repository name: `tournament-hub` (or any name you like)
3. Set visibility to **Public**
4. Click **Create repository**

### Step 2 — Upload the file

**Option A — via the GitHub web UI (easiest):**
1. In your new repo, click **Add file → Upload files**
2. Drag and drop `index.html` from this folder
3. Commit message: `Initial deploy`
4. Click **Commit changes**

**Option B — via Git (if you have Git installed):**
```bash
git init
git add index.html
git commit -m "Initial deploy"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/tournament-hub.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. In your repo, go to **Settings → Pages**
2. Under **Source**, select **Deploy from a branch**
3. Branch: `main` / folder: `/ (root)`
4. Click **Save**

After ~60 seconds your site will be live at:
```
https://YOUR_USERNAME.github.io/tournament-hub/
```

---

## 🔴 Enable Live Sync (JSONBin — free)

Without sync, scores only save locally. With JSONBin, admin edits push live to all viewers instantly.

### Step 1 — Get your JSONBin API key
1. Go to [jsonbin.io](https://jsonbin.io) → Sign up (free)
2. Dashboard → **API Keys**
3. Copy your **Master Key** (starts with `$2a$` or `$2b$`)

### Step 2 — Connect in the app
1. Open your tournament as **Admin**
2. Tap the ☁ sync icon in the top-right header
3. Paste your Master Key → tap **Connect & Save**
4. A bin is auto-created — a **Share Link** appears

### Step 3 — Share with viewers
1. Copy the share link from the sync panel  
   It looks like: `https://you.github.io/tournament-hub/?bin=64abc…&tid=t_xyz`
2. Send it to participants via WhatsApp, email, QR code — anything
3. Viewers click the link → scores load instantly, refresh every 6 seconds

> ⚠️ **Important:** In your JSONBin dashboard, make sure the bin is set to **Public** so viewers can read without a key.

---

## 📱 How to use

### Admin
| Action | How |
|---|---|
| Create tournament | Landing page → **New Tournament** |
| Add teams | Setup tab → add groups & teams |
| Enter scores | Scores tab → pick two teams → fill in sets |
| Save automatically | Every change auto-saves locally + syncs to JSONBin |
| Change password | Key icon in header |
| Export results | Export tab → download CSV |

### Viewer (participants)
| Action | How |
|---|---|
| Open live scores | Click the share link the admin sent you |
| No login needed | Tap "View Live Scores" — done |
| Auto-refresh | Scores update every 6 seconds |
| Export results | Export tab → download CSV |

---

## 🗂 Tabs

| Tab | Who sees it | Description |
|---|---|---|
| **Setup** | Admin only | Configure tournament, teams, players |
| **Schedule** | Everyone | All fixtures with dates, venues, status |
| **Scores** | Everyone | Game-by-game scorecards (admin can edit) |
| **Standings** | Everyone | Points table per group |
| **Knockout** | Everyone | Semi-finals, final, 3rd place bracket |
| **Export** | Everyone | Download CSV files |

---

## 🔄 Updating the app

When a new version of `index.html` is available:
1. In your GitHub repo, click on `index.html`
2. Click the pencil ✏️ edit icon → then the **⋮** menu → **Delete file** — OR
3. Simply upload the new `index.html` and commit — GitHub will replace the old one
4. GitHub Pages redeploys automatically within ~60 seconds

---

## 🛠 Tech notes

- **Single file** — everything (HTML + CSS + JS) in one `index.html`
- **Zero dependencies** — no npm, no build step, no framework
- **Storage** — `localStorage` for local persistence, JSONBin for cross-device sync
- **Fonts** — system-ui (iOS/macOS native font, no download needed)
- **Icons** — Tabler Icons (loaded from CDN)
- **Mobile** — fixed bottom tab bar on phones, horizontal tab bar on tablets/desktop
- **Safe areas** — respects iOS notch / home indicator via `env(safe-area-inset-*)`
