# Master Planner

A single-file, self-contained planning/scheduling app. All task data lives inline in `index.html`; per-user progress (checkboxes) is stored in the browser's `localStorage`, with an optional JSON export/import for manual backups.

## Live progress sync (optional)

To let everyone viewing the hosted page see the same live progress (instead of each viewer having their own separate local checkboxes), configure a free [Firebase Realtime Database](https://firebase.google.com/) and fill in `FIREBASE_CONFIG` near the top of the `<script>` block in `index.html` (search for `CLOUD SYNC`):

```js
var FIREBASE_CONFIG = {
  apiKey: "...",
  databaseURL: "https://YOUR-PROJECT-default-rtdb.firebaseio.com",
  projectId: "..."
};
```

Leave it blank to keep the app fully local (default, unchanged behavior).

## Editing later

It's a single HTML file — open it, edit, commit, push. GitHub Pages redeploys automatically a minute or two after you push to `main`.

## Hosting

Deployed via GitHub Pages, serving `index.html` from the repo root on the `main` branch.
