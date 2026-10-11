# HacXLerate 2026 Timer

A lightweight single-page countdown timer for a 24-hour hackathon experience. The app is designed for event screens, team spaces, and live countdown displays, with a polished dashboard look and persistent timer state.

## Overview

This project is a standalone HTML application built around a 24-hour countdown.

It includes:
- a large live timer for hours, minutes, and seconds
- elapsed time tracking
- end-time display
- progress bar for the current 24-hour window
- start and reset controls
- fullscreen mode support
- browser localStorage persistence so the timer survives refreshes

The interface is intentionally bold and event-focused, matching the style of a hackathon or innovation challenge landing screen.

## Project structure

- `timer.html` — complete app with HTML, CSS, and JavaScript in one file
- `README.md` — project documentation

## Features

### 24-hour countdown
The timer starts from a 24-hour countdown and updates continuously every 250 ms.

### Live status updates
The app shows:
- current remaining time
- elapsed time
- a computed end time
- progress completion percentage

### Controls
- `Start 24h` begins the countdown
- `Reset` clears the active timer and local saved state
- `Fullscreen` toggles the browser fullscreen mode

### Persistence
The timer deadline is saved in `localStorage` under the key `hx`, so refreshing the page preserves the countdown state when possible.

## How to run

Because this is a static HTML file, there are no dependencies or build steps.

Option 1: Open directly in a browser
- Open `timer.html` in any modern browser

Option 2: Serve it locally
From the project folder:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/timer.html
```

## Behavior notes

- The timer starts when the user clicks the Start button.
- The timer automatically ends when the countdown reaches zero.
- The program displays a `TIME'S UP!` status and resets the start button after completion.
- In some browsers, fullscreen request can be blocked by permission or browser security rules. The app falls back to an alert suggesting `F11` as a manual alternative.

## Customization

You can easily adjust the app by editing the constants in `timer.html`:

- `T = 24 * 3600 * 1000` controls the total countdown duration
- CSS variables and text can be changed directly in the `<style>` section
- branding images and labels can be replaced in the HTML markup

## Browser support

This app is intended for modern desktop browsers with support for:
- `localStorage`
- `requestFullscreen()` / `exitFullscreen()`
- standard HTML5 and CSS3 features

## License

No explicit license file is included in this project. If you plan to distribute or reuse this code publicly, add an appropriate license before sharing it beyond personal use.

## Summary

This project is a fast, elegant, single-file hackathon timer designed for live event monitoring. It is easy to run, easy to customize, and works well as a standalone display page for a 24-hour competition or event countdown.
