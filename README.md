# Waveora — GitHub Pages deployment

This version uses Vite and installs `@ffmpeg/ffmpeg` through npm so Vite can bundle the FFmpeg worker with the app. It avoids importing the FFmpeg package directly from `esm.sh`, which caused the cross-origin Worker error.

## Deploy
1. Create a GitHub repository (for example `waveora`) and upload all files in this folder, including `.github/workflows/deploy.yml`.
2. Ensure the default branch is named `main`.
3. In GitHub, open **Settings → Pages** and set **Build and deployment → Source** to **GitHub Actions**.
4. Open the **Actions** tab and wait for **Deploy Waveora to GitHub Pages** to complete.
5. Open the Pages URL shown by GitHub. Use HTTPS, not a local `file://` URL.

No CMD is needed after deployment. The first export downloads the FFmpeg core from a CDN, so the user needs an internet connection. Audio is processed in the browser.

## Test locally (optional)
Install Node.js, then run `npm install` and `npm run dev`.
