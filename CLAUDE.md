# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A personal static homepage (GitHub Pages) — a single-page HTML site with CSS animations and vanilla JS interactivity. All code lives in `index.html`.

## Architecture

- **Single file**: `index.html` contains all HTML structure, CSS styles, and JavaScript logic. No build tools, frameworks, or package managers.
- **Assets**: `./assets/` — `avatar.jpg` (profile picture), `bg.jpg` (background image), `favicon.ico`
- **Media**: `./media/` — `music.mp3` (background music), `music.ogg` (fallback format)

### Key Features

| Feature | Implementation |
|---|---|
| Sakura (cherry blossom) rain | Pure CSS animation — `.sakura` elements with keyframe `fall`, staggered delays |
| Magic circle | CSS rotating triangle rings (`rotate-slow`/`rotate-slow-reverse` keyframes), concentric circles via `::before`/`::after` |
| Audio player | HTML5 `<audio>` with custom play/pause, progress bar (click-to-seek), time display |
| Real-time clock | JavaScript `setInterval(1000)` updating `#currentTime` / `#currentDate` |
| Custom cursor glow | Fixed-position radial gradient div following `mousemove`, scales up on interactive elements |
| Avatar parallax | Mouse-follow rotation via `mousemove` on `.avatar` |
| Auto-play music | Listens for first user interaction (`click`/`keydown`/`touchstart`), then attempts `audio.play()` |
| Keyboard shortcut | Press `M` key to toggle play/pause |
| Responsive layout | CSS Grid (two-column → single-column), media queries at 980px and 520px |

### Visual Design

- Dark theme with glassmorphism cards (`backdrop-filter: blur`, semi-transparent backgrounds)
- Gradient accents: blue (`#8ab4ff`) and purple (`#f3a8ff`)
- Background image with dark gradient overlay
- Fade-up entrance animations on cards (`.fade-up`, `.delay-*`)

## Development

Since this is a static site, just edit `index.html` and open it in a browser to preview:

```bash
# Preview locally (any static file server)
python3 -m http.server 8080     # then open http://localhost:8080
# or
npx serve .
```

No build or test commands needed.

## Deployment

Push to `main` branch; GitHub Pages serves the site from the repository root automatically.

## Adding Content

- **Profile info**: Edit the `.intro`, `.meta`, `.tags` sections in the HTML
- **Music list / Galgame list / Scenery**: Edit the `<ul class="list">` items in the grid panels
- **Quotes**: Edit `.quote-item` elements in the quotes panel
- **Background music**: Replace `./media/music.mp3` (and `music.ogg` for Firefox compatibility)
- **Avatar**: Replace `./assets/avatar.jpg` (at least 248x248px)
- **Background image**: Replace `./assets/bg.jpg` (1920x1080+ recommended)
