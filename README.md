# PixelProTech Auto Clip Editor — PWA Package

Upload a long video, auto-pick the most active moments, crop to vertical/square, export short clips, and post them. Runs fully in the browser; the video never leaves your device.

Files (keep flat): `index.html`, `manifest.json`, `service-worker.js`, `icon-192.png`, `icon-512.png`, `README.md`.

## Use it
1. Choose a video (MP4 from your phone or camera works best).
2. Set clip length, number of clips, format (9:16 for Shorts/Reels/TikTok) and optional title text. Click Find best moments.
3. Adjust start/end times, untick clips you don't want, click Export. Keep the tab open and visible; clips record in real time.
4. Download each clip, or tap Share on a phone to send it to YouTube, Instagram or TikTok. On desktop, use the upload links and pick the file.

## How moments are chosen
The audio is analysed for the loudest, most active stretches (speech energy, laughter, music peaks). Clips never overlap. If audio can't be analysed (very large files over 700 MB, or unsupported audio), clips are spaced evenly.

## Deploy (GitHub Pages)
New repo (for example `Clip-Editor`) → Add file → Upload files → all 6 files in the root → Commit. Settings → Pages → `main` → `/ (root)` → Save.

## Limits
Export is real time (a 45 s clip takes about 45 s). Output is MP4 where the browser supports it (recent Chrome, Edge, Safari), otherwise WebM. Posting to a platform needs your own logged-in account; automatic posting would need each platform's API keys and a server.

## Editing
Bump `pixelprotech-clip-editor-v1` to `-v2` in `service-worker.js` whenever you change `index.html`.
