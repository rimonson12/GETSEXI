# Train Log setup

## 1. Put the app online (GitHub Pages, same as Golf Log)
1. Create a new public repo, for example `train-log`.
2. Upload `index.html`, `sw.js`, `manifest.json`, `icon-180.png`, `icon-512.png`.
3. Settings > Pages > Deploy from branch > `main` / root. The app lives at `https://<your-username>.github.io/train-log/`.

## 2. Connect a Google Sheet
1. Create a new Google Sheet (for example "Train Log").
2. Extensions > Apps Script. Replace everything in `Code.gs` with this `Code.gs`. Save.
3. Choose `setupSheet` in the function menu and click Run. Approve the permissions. This builds the tabs.
4. Deploy > New deployment > type Web app. Execute as: Me. Who has access: Anyone. Deploy and copy the `/exec` URL.
5. In the app: Settings > paste the URL > Save and test.

Tabs: **Sets** (one row per set), **Workouts** (one row per session), **Exercise Summary**, **Top Sets** (top weight per exercise per day, good for charts), **Weekly**, and **Weekly by Program** (gym phases and Mobility counted separately).

## 3. Install on your iPhone
Open the GitHub Pages link in Safari > Share > Add to Home Screen. Open it once while online; after that it works offline.

## Updating later
Upload the new `index.html` (and `sw.js` if it changed) to the repo, then open the app and reload twice.
If you change `Code.gs`, use Deploy > Manage deployments > edit > New version so the URL stays the same.

## Loading a new program
Plan > Import workouts > choose a CSV with the same columns as the 6-month plan. Workouts with the same name are replaced; your history is kept.
