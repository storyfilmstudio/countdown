# COUNTDOWN STUDIO

A browser-based countdown video creator built with HTML, CSS and vanilla JavaScript.

## What is included

- Live canvas preview with play, pause, restart and timeline scrubbing
- 10 visual styles: Luxury Gold, Royal Blue, Neon Pink, Cinematic Red, Silver Chrome, Purple Glow, Emerald Green, Digital LED, Minimal Clean and Glass Effect
- Independent background colour presets, including pure chroma green (`#00FF00`)
- Countdown formats: `MM:SS` and `HH:MM:SS`
- Real-time and compressed/custom-duration modes
- Typography, scale, frame, glow and placement controls
- Synthesized audio options, volume control and sound tests
- 16:9, 9:16 and 1:1 output sizes, plus 30/60 FPS choices
- Browser video recording with download and filename controls
- Source ZIP export built into the app without a third-party ZIP library
- English and Sinhala setup guides

## Project structure

```text
countdown-studio/
├── index.html
├── favicon.svg
├── README.md
├── README_SI.txt
├── css/
│   └── style.css
└── js/
    └── app.js
```

## Run locally

The project does not need a build step or Node.js.

Recommended: serve the folder over localhost so browser media APIs work consistently.

1. Extract the ZIP.
2. Open a terminal inside the `countdown-studio` folder.
3. Run one of these local static servers:

   **Python**
   ```bash
   python -m http.server 8080
   ```

   **Node.js (if installed)**
   ```bash
   npx serve .
   ```

4. Open `http://localhost:8080` (or the URL printed by `serve`).

Opening `index.html` directly may show the interface, but browser recording or audio APIs can behave differently under `file://`.

## Publish on GitHub Pages

1. Create a GitHub repository.
2. Upload the **contents** of the `countdown-studio` folder, preserving the `css` and `js` folders.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select your branch (usually `main`) and folder `/ (root)`, then save.
6. Open the Pages URL after GitHub finishes publishing.

The app uses relative asset paths (`./css/style.css`, `./js/app.js`), so it also works when the repository is published under a project subpath.

## Export notes

- Video rendering happens locally in the browser; the project does not upload your countdown or video to a backend.
- The browser must support `HTMLCanvasElement.captureStream()` and `MediaRecorder`.
- The application selects an available recording format. Some browsers can record MP4; others will produce WebM. The actual extension is shown after export.
- 60 FPS and Full HD/vertical Full HD rendering can be demanding on phones. For older or lower-memory devices, try 1280×720 at 30 FPS.
- Long real-time countdowns take approximately the same time to record as the requested video duration. Compressed mode creates a shorter file.
- Audio export uses the Web Audio API. The browser may require a user interaction before audio playback is allowed.

## Troubleshooting

- **Unstyled page:** check that `css/style.css` exists and that the folder structure above was preserved.
- **Buttons do nothing:** check that `js/app.js` exists and open the browser developer console for errors.
- **Video export unavailable:** use a current version of Chrome, Edge or Firefox over `http://localhost` or HTTPS.
- **No audio in the result:** make sure sound is enabled, the sound option is not Silent, and the browser permits audio playback.
- **GitHub Pages shows a blank or unstyled page:** make sure the asset paths were not changed to root paths beginning with `/`, and that the files are committed in the correct folders.

## Privacy

Countdown composition and rendering run in the browser. External font files may be requested from Google Fonts when internet access is available; system fallback fonts are used otherwise.
