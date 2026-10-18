MY SUDOKU — ANDROID HOME-SCREEN APP
===================================

WHAT THIS PACKAGE DOES
- Adds a PWA manifest and app icon.
- Adds a service worker to cache the app for offline use.
- Keeps the existing Sudoku game code.
- Does not require a Play Store account or paid software.

EASIEST FREE INSTALL ROUTE: GITHUB PAGES
Important privacy note: a GitHub Pages website is publicly reachable on the internet, even if you don't share its link. The current game has no account or server-side score sync, but anyone who finds the URL can play it. Do not put personal/sensitive information in the game. If you need the app itself to be inaccessible to everyone else, use a local-only app wrapper or a private hosting solution instead.

1. On a computer, sign in or create a free account at https://github.com/
2. Create a new repository. Example name: my-sudoku. For GitHub Free, make the repository PUBLIC if you plan to use GitHub Pages.
3. Upload the contents of this ZIP (not the ZIP file itself) to the repository's root:
   index.html
   manifest.json
   service-worker.js
   icons/sudoku-192.png
   icons/sudoku-512.png
4. In the repository, open Settings -> Pages.
5. Under Build and deployment, choose "Deploy from a branch", select branch "main" and folder "/ (root)", then Save.
6. Wait for deployment. GitHub will show a site address similar to:
   https://YOUR-USERNAME.github.io/my-sudoku/
7. Open that HTTPS address on your Android phone in Chrome while online. Wait a few seconds so the app and files are cached.
8. In Chrome, tap the three-dot menu and choose "Install app" or "Add to Home screen" (wording varies), then confirm.
9. Open the new Sudoku icon once while online. Then test airplane mode and open the installed app.

OFFLINE NOTES
- The app shell is cached by the service worker after the first online visit.
- Keep the game open briefly after first loading so caching can finish.
- Saved progress uses browser local storage, so it is tied to that browser/site on that device.
- Clearing Chrome/site data may erase saved progress.
- Updates to the hosted game may take a refresh or app restart to appear.

IF INSTALL DOES NOT APPEAR
- Confirm the address starts with https://
- Confirm manifest.json and service-worker.js are in the repository root.
- Open the site in Chrome, not a file manager preview.
- Refresh once, wait a few seconds, then check the three-dot menu again.

REFERENCE
MDN: https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Guides/Making_PWAs_installable
GitHub Pages HTTPS: https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https
