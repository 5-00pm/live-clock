# Midnight Clock — Live Wallpaper Screensaver

A minimal, elegant clock screensaver designed for Android landscape mode. Built with a midnight beach video background and refined typography.

![preview](preview.png)

---

## Features

- **Live clock** — hours, minutes, seconds with smooth tick animation
- **Seconds progress bar** — thin line along the bottom edge
- **Date display** — day and date in spaced uppercase
- **Wake Lock API** — keeps the screen on in supported browsers
- **Video loop** — seamless background, auto-resumes after backgrounding
- **Zero dependencies** — single HTML file + one video

---

## File Structure

```
midnight-clock/
├── index.html     ← everything lives here
├── bg.mp4         ← your background video (replace with your own)
└── README.md
```

---

## How to Use on Android

### Option A — Chrome / Firefox (simplest)
1. Transfer `index.html` and `bg.mp4` to your phone (same folder)
2. Open `index.html` in Chrome
3. Tap the menu → **Add to Home Screen**
4. Open the shortcut → tap the ⋮ menu → **Desktop site**
5. Use alongside a "keep screen on" utility app

### Option B — Web Live Wallpaper (recommended)
1. Install **[KLWP Live Wallpaper](https://play.google.com/store/apps/details?id=org.kustom.wallpaper)** or **Web Live Wallpaper**
2. In the app, set the source to your local `index.html`
3. Apply as your lock screen / home screen wallpaper

### Option C — Daydream / Screen Saver (Android 4.2+)
1. Go to **Settings → Display → Screen saver** (or Daydream)
2. Choose **Browser** or any WebView-based saver app
3. Point it to your local `index.html`

---

## Customising

All tweakable values are in `index.html`:

| What | Where | How |
|---|---|---|
| Video file | `<source src="bg.mp4">` | Replace `bg.mp4` with your video filename |
| Video opacity | `.overlay-vignette` background | Increase the rgba alpha values to darken |
| Clock font | `font-family: 'Cormorant'` | Swap for any Google Font |
| Clock size | `font-size: clamp(…)` on `.time-hhmm` | Adjust the middle `vw` value |
| 24h format | JS `update()` function | Remove the `% 12` logic and hide `.time-ampm` |
| Time zone | JS `new Date()` | Use `toLocaleString('en', { timeZone: '…' })` |

---

## Exporting / Hosting

```bash
# Clone or download, then just open in a browser
git clone https://github.com/YOUR_USERNAME/midnight-clock
cd midnight-clock
# drop your bg.mp4 in, open index.html
```

To host online (GitHub Pages, Vercel, Netlify) note that the video must be in the same repo or served from the same origin due to browser security policies.

---

## Credits

Font: [Cormorant](https://fonts.google.com/specimen/Cormorant) & [Josefin Sans](https://fonts.google.com/specimen/Josefin+Sans) via Google Fonts  
Video: your midnight beach clip (`bg.mp4`)

---

MIT License
