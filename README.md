# Mini Golf Scores

Live multiplayer mini golf scorekeeper. The host creates a game, shares a link or QR code, and everyone keeps score from their own phone. It's a single static page (`index.html`), with live sync through Firebase Realtime Database.

## Setup (one time)

1. Create a project at https://console.firebase.google.com (Analytics not needed).
2. **Build → Realtime Database → Create database** (any location, start in *locked mode*).
3. In the database's **Rules** tab, paste the contents of `database.rules.json` and publish.
4. **Project settings → Your apps → Web (`</>`)**, register an app, and copy the `firebaseConfig` object into `config.js`:
   ```js
   window.FIREBASE_CONFIG = { apiKey: "...", authDomain: "...", databaseURL: "https://...firebaseio.com", projectId: "...", appId: "..." };
   ```
5. **Repo Settings → Pages → Deploy from a branch → `main` / root**.

The site will be at `https://agent693.github.io/Mini-Golf-Automatic-Score-Tracker/`.
