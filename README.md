# Teleprompter

A self-contained browser teleprompter with speech tracking. Paste your script, hit Start, and it scrolls to follow your voice — no install, no server, no dependencies. Designed to sit below the camera so your reading zone stays close to the lens.

## Features

- **Speech tracking** — matches your spoken words against the script in real time using the Web Speech API and advances the scroll position automatically
- **Manual scroll** — mouse wheel, arrow keys, and on-screen buttons all work alongside speech tracking
- **Auto-scroll speed** — optional timer-based scroll (1–10) for when you want a fixed pace
- **Click to jump** — click any word in the script to jump directly to that position
- **Font size control** — adjustable before and during the session
- **Mirror mode** — flips the text horizontally for use with a physical half-mirror rig
- **Keyboard shortcuts** — full control without touching the mouse

## Usage

1. Open `teleprompter.html` in **Chrome** or **Edge**
2. Paste your script into the text area
3. Adjust font size and scroll speed if needed
4. Toggle **Speech tracking** and **Mirror** as required
5. Click **Start →**
6. Allow microphone access when prompted
7. Press **Space** to begin — the script will follow your voice

## Keyboard Shortcuts

| Key | Action |
|---|---|
| `Space` | Play / Pause |
| `↑` / `↓` | Scroll up / down |
| `Page Up` / `Page Down` | Scroll by screen |
| `Home` | Reset to top |
| `+` / `−` | Increase / decrease font size |
| `S` | Toggle speech tracking |
| `M` | Mirror text |
| `?` | Show shortcut reference |
| `Esc` | Exit to setup |

## Browser Requirements

Requires **Chrome** or **Edge** — Firefox does not support the Web Speech API. Microphone permission must be allowed when prompted.

## How It Works

Speech recognition runs continuously via the browser's built-in Web Speech API. As words are recognized, the app matches them against the script using fuzzy string comparison (handles minor recognition errors) and scrolls to keep the current word near the top of the screen. Interim results provide smooth word-by-word movement; final results lock the position accurately at each phrase boundary.

## Files

| File | Purpose |
|---|---|
| `teleprompter.html` | The entire app — open this in your browser |
| `README.md` | This file |
