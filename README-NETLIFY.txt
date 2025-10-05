Netlify One‑Click / Simple Deploy
=================================

Option A: Super quick (Drag & Drop)
-----------------------------------
1) Unzip this folder locally so you have:
   - index.html, manifest.webmanifest, sw.js, icon-192.png, icon-512.png, netlify.toml
2) Go to https://app.netlify.com/drop
3) Drag the *entire folder* onto the page. Netlify builds and gives you an HTTPS site.
4) Open the URL. Tap the in‑app “Install App” button to add to your Home screen.

Option B: One‑click “Deploy to Netlify” (via Git)
-------------------------------------------------
1) Create a new public GitHub repo.
2) Upload the contents of this folder to the repo root.
3) Visit: https://app.netlify.com/start/deploy?repository=REPO_URL
   Example: https://app.netlify.com/start/deploy?repository=https://github.com/<you>/<reponame>

Option C: Netlify CLI (one command)
-----------------------------------
1) npm i -g netlify-cli
2) netlify login
3) netlify init  (first time only)
4) netlify deploy --prod --dir=.

Why the site might not show “Install App”
-----------------------------------------
- PWA install prompts require HTTPS. Netlify provides HTTPS automatically.
- Opening over file:// won’t show the install button.
- The “📥 Install App” button appears when the browser fires `beforeinstallprompt`, which only happens over HTTPS.
