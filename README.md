# Project Manager App

Mobile-first project management for hands-on work and life.

## Status: Phase 1 MVP - Quick Capture

A PWA for fast note capture with voice input and hashtag support.

## Quick Start

1. Serve the `src/` folder locally:
   ```bash
   cd src
   python -m http.server 8000
   ```
2. Open http://localhost:8000 in your browser
3. For mobile: connect to the same network and use your computer's IP

## Features (MVP)

- Text input with hashtag detection (#project, #sop, #materials)
- Voice input via Web Speech API (Chrome/Edge)
- Offline-capable PWA
- Notes saved to localStorage

## Directory Structure

```
src/           - PWA source code
docs/          - Architecture & design docs
examples/      - Example files
user-projects/ - User data (gitignored)
```

## Documentation

- [Architecture](docs/ARCHITECTURE.md) - System design and principles
- [Design Conversation](docs/design-conversation.markdown) - Full planning context
