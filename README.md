# Air Instrument 🎹✋

A webcam hand-tracking musical instrument. **Right hand** plays chords + draws
calligraphic ink; **left hand** triggers drums. Built with MediaPipe Hands +
Three.js. **Single file, no build step.**

## Try it live

**▶ https://moira-0327.github.io/air-instrument/** — open on any device, allow
the camera, and raise your hands.

<img src="qr.png" alt="QR code to the live demo" width="200" />

_Scan the QR to open the demo on your phone._

## Download the code

**Easiest — ZIP (no tools needed):**
1. Go to https://github.com/Moira-0327/air-instrument
2. Click the green **`< > Code`** button → **Download ZIP**
3. Unzip, then double-click `index.html`.

Direct ZIP link: https://github.com/Moira-0327/air-instrument/archive/refs/heads/main.zip

**Or clone (for editing / commits):**
```bash
git clone https://github.com/Moira-0327/air-instrument.git
cd air-instrument
open index.html      # macOS · on Windows just double-click index.html
```

## Run it (30 seconds)

You have internet? That's all you need.

**Option A — double-click**
1. Download this folder.
2. Double-click `index.html`. It opens in your browser.
3. Allow the camera, click **Start**, raise your hands. 🎶

**Option B — local server** (use this if the camera is blocked on `file://`)
```bash
# any one of these, from inside this folder:
python3 -m http.server 8000
# or
npx serve .
```
Then open http://localhost:8000

> **Camera needs a "secure context."** `localhost` and (in Chrome) `file://`
> both count as secure, so either option above works. If you host it somewhere,
> it must be **https**.

## Modify it

Everything lives in **one file: `index.html`** — HTML, CSS, and all the JS.
Open it in any editor and hit save; refresh the browser. No `npm`, no bundler,
no framework.

Handy places to tinker (search for these in `index.html`):
- Chord voicings / musical scale → search `chord` / `scale`
- Ink trail look (calligraphy) → search `ink`
- Drum triggers → search `drum`
- Hand-tracking sensitivity → search `Hands` / MediaPipe options

## Dependencies

None to install. Loaded from CDN at runtime (needs internet):
- [three.js](https://threejs.org/) `0.182.0`
- [@mediapipe/hands](https://google.github.io/mediapipe/) `0.4`
- [@mediapipe/camera_utils](https://google.github.io/mediapipe/) `0.3`

## Browser support

Chrome / Edge recommended (best WebGL + camera + MediaPipe support). Works on
desktop; mobile is hit-or-miss due to camera + performance.

## Troubleshooting

| Problem | Fix |
|---|---|
| Camera won't turn on | Use **Option B** (localhost server); grant camera permission in the browser prompt. |
| Blank / black screen | Check you have internet (CDN libs). Open DevTools console for errors. |
| No sound | Click/interact once first — browsers block audio until a user gesture. |
| Laggy | Close other tabs; good lighting helps hand tracking; use Chrome. |
