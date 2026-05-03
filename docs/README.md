# Agile Board PWA

Industrial-aesthetic agile board for task and noise management.
Installable as a Progressive Web App (PWA).

## Files

```
agile-board/
├── index.html      ← Main application
├── manifest.json   ← PWA manifest
├── sw.js           ← Service worker (offline caching)
├── icon-192.svg    ← App icon (192×192)
├── icon-512.svg    ← App icon (512×512)
└── README.md       ← This file
```

## Deployment

**The app must be served over HTTPS for PWA features to work.**

### Option A — GitHub Pages (free)
1. Create a new GitHub repo
2. Upload all files to the repo root
3. Go to Settings → Pages → Deploy from branch (main / root)
4. Visit `https://<username>.github.io/<repo-name>`

### Option B — Netlify (drag & drop)
1. Go to https://app.netlify.com/drop
2. Drag the entire `agile-board/` folder onto the page
3. Your app is live instantly with HTTPS

### Option C — Any static host
Upload all files to the same directory on any static web server with HTTPS.

### Option D — Local (no install prompt, but works offline after first load)
```bash
npx serve .
# or
python3 -m http.server 8080
```
Note: Install prompt requires HTTPS, so it won't appear on localhost.

## PWA Features
- **Installable** — "Install App" button appears on supported browsers
- **Offline** — Full functionality without internet after first load
- **Responsive** — Works on mobile and desktop
- **Data persistence** — All cards saved to localStorage

## Data
All data is stored in `localStorage` under the key `agileBoardPWA`.
Use the **[ EXPORT ]** button to back up your board as JSON.
Use the **[ IMPORT ]** button to restore from a backup.
