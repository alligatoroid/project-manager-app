# Project Status

**Last Updated:** 2026-02-02

## Current State: Phase 1 MVP + Media Capture

The Quick Capture PWA is live and functional at:
https://alligatoroid.github.io/project-manager-app/

### What's Working
- Mobile-first text input with hashtag detection
- Voice input via Web Speech API
- Spoken punctuation ("period", "comma", "question mark", etc.)
- **Photo capture** from camera or gallery
- **Video capture** (up to 30 seconds) with recording timer
- Media attached to notes with thumbnail previews
- Full-screen media viewer
- Notes saved to localStorage (with automatic cleanup for storage limits)
- Offline-capable PWA
- Settings screen with API key storage (for future AI features)

### Known Issues
- AI auto-punctuation was attempted but not working - reverted to manual spoken punctuation
- Voice input works best on Chrome/Edge (Web Speech API limitation)

## Tech Stack
- Single HTML file PWA (index.html at repo root)
- Vanilla JavaScript (no framework)
- localStorage for data
- GitHub Pages for hosting
- Service worker for offline (sw.js)

## File Structure
```
/
├── index.html      # Main PWA app
├── manifest.json   # PWA manifest
├── sw.js          # Service worker
├── docs/
│   ├── ARCHITECTURE.md        # System design & principles
│   ├── STATUS.md              # This file - current state
│   └── design-conversation.markdown  # Original planning chat
└── user-projects/  # Future: user data (gitignored)
```

## Next Steps (Not Started)
From the original design, future phases include:
1. Project organization (create projects, file notes into them)
2. Task management with priorities and energy levels
3. Time tracking (start/stop timer, manual entry)
4. Reflection system with guided prompts
5. AI task recommendations ("what should I work on?")
6. Cloud sync (currently localStorage only)

## Key Design Decisions
- Mobile-first: Voice input, one-handed operation
- Markdown-first: Human-readable data files
- Degradable: Works without AI, works offline
- Simplicity: Features added only when patterns emerge

## For New Claude Sessions
Read these files to understand the project:
1. This file (STATUS.md) - current state
2. ARCHITECTURE.md - system design & principles
3. design-conversation.markdown - full context on "why" decisions

## API Key Note
Settings screen stores Anthropic API key in localStorage for future AI features.
The AI punctuation feature was disabled - using manual spoken punctuation for now.

## Recent Session (2026-02-02)
- Added photo and video capture functionality
- Camera button next to voice button for quick media capture
- Supports front/rear camera switching, gallery selection
- Videos limited to 30 seconds for storage constraints
- Media stored as base64 in localStorage with auto-cleanup when quota exceeded
- Fixed CSS conflict where voice button's fixed positioning was hiding the camera button
- Resolved GitHub Actions deployment failure (runner availability issue, required manual re-run)
