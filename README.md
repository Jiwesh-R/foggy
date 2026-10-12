# fog. — a living mirror

A single-file browser experience: fog your webcam mirror by breathing, write on the glass with a pinch gesture, and wipe it clean with a fist.

## Publish on GitHub Pages

1. Create a **public** GitHub repository called `fog` (or use your own repository name).
2. Upload `index.html` and `.nojekyll` from this folder to the **root** of its `main` branch. (You can also upload this README.)
3. In the repository, go to **Settings → Pages → Build and deployment**.
4. Set **Source: Deploy from a branch**, **Branch: main**, and **Folder: / (root)**, then **Save**.
5. Visit `https://YOUR-USERNAME.github.io/fog/`, replacing both the username and `fog` with your actual names.
6. On the start screen, press **step into the mirror**, then allow camera and microphone permissions.

GitHub Pages provides HTTPS, which browsers require for webcam access. MediaPipe's pinned JavaScript and models are fetched from jsDelivr, so internet access is needed to load those assets; the camera and microphone data stay in the browser and are not uploaded by this site.

No backend, compilation, npm, service worker, or build process.

## Controls

- Breathe or hold Space to add fog.
- Pinch your thumb and index finger and move to write through the fog.
- Make a fist and swipe to wipe away a broad area.
- Bottom-left **brush** slider adjusts stroke radius.
- **C** resets the fog; **S** or the shutter saves a PNG; **Esc** returns to start.

## Local development

Run `python -m http.server 8000` in the repository directory, then visit `http://localhost:8000/`. Opening the HTML from `file://` does not grant camera access.
