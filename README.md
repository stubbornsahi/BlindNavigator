BlindNavigator — Quick Hosting & Testing Instructions

Contents:
- frontend/: index.html, styles.css, app.js
- backend/: server.js, seed.js, package.json

Frontend-only hosting (fastest, GitHub Pages):
1. Create a GitHub repository (public or private).
2. Upload the files inside the frontend/ folder (index.html, styles.css, app.js) to the repository root or a folder named `docs`.
3. In GitHub -> Settings -> Pages choose Branch: main and folder: / (or /docs) and save.
4. After a minute you'll get a URL like: https://yourusername.github.io/reponame/
5. Open that link in Chrome and click "Start Voice". Use commands like: "Read page", "Open item 1", "Add to cart 1".

Full stack hosting (frontend + Node.js backend on same repo):
Option A — Render.com or Railway.app
1. Push the whole project to GitHub.
2. On Render or Railway, create a new Web Service and connect the GitHub repo.
3. Set the start command to `node backend/server.js` and the root to the repository root.
4. For Render, the service will expose a URL like https://blindnavigator.onrender.com

Option B — Local testing (recommended for demo if backend needed)
1. Install Node.js (v14+)
2. Open terminal:
   cd backend
   npm install
   npm run seed
   npm start
3. Open browser: http://localhost:3000

Notes:
- SpeechRecognition (voice commands) works best in Chrome or Edge browsers.
- For production HTTPS is required for speech recognition; localhost is allowed for testing.
- If you host frontend on GitHub Pages and backend on Render, ensure backend's CORS allows requests from the Pages URL.

If you want, I can:
- Create the GitHub-ready repo structure here for you to upload,
- or create a zip file containing the project (already prepared) for download.
