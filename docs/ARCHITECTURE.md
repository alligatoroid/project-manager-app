# Architecture

## System Overview

**What this is:** A mobile-first project management system designed for capturing work-in-progress feedback, reflections, and knowledge while actively doing hands-on work. Equally supports professional work projects (fabrication, design) and personal life management (family, health, home).

**What this isn't:**
- Not a traditional project management tool with Gantt charts
- Not dependent on constant connectivity or cloud services
- Not a social/collaborative platform (single-user focused)

**Core use case:** You're welding planter boxes and realize the corner joint settings work perfectly. You pull out your phone, voice-note "MIG aluminum 1/8 outside corner: 19v, 350ipm #planterbox #sop" and get back to work. Later during reflection, the system offers to update your aluminum welding SOP with this knowledge.

## Core Principles

1. **Mobile-First Capture** - Opening app to capturing idea must take <5 seconds
2. **Markdown-First Storage** - All data as human-readable markdown files
3. **Degradable Design** - Works without AI, works offline
4. **Reflection as Output** - Daily work transforms into structured knowledge
5. **Simplicity Over Features** - Add features only when patterns emerge

## Tech Stack

- **Frontend:** Progressive Web App (PWA)
- **Storage:** Local markdown files (localStorage for MVP)
- **Voice:** Web Speech API
- **AI:** Anthropic Claude API (optional enhancement)

## Data Structure

```
user-projects/
├── _inbox/           # Quick captures before filing
├── _system/          # Workflow config, priority hierarchy
├── _shared/          # Cross-project SOPs
└── projects/         # Individual project folders
    └── [project]/
        ├── project.md
        ├── tasks.md
        ├── sop.md
        ├── time-log.md
        ├── notes.md
        ├── reflections.md
        └── media/
```

## Phase 1: Quick Capture MVP

- Text input with hashtag support (#project, #sop, #materials)
- Voice-to-text button (bottom, one-handed)
- Save to localStorage
- Display recent notes
- Offline-capable

## Flagged for Future

- Visual dependency flowcharts
- PLM/versioning tutorial
- Inventory tracking
- Calendar integration with deadline warnings
- Handwritten note OCR
- Life backend (supplements, plant care, vehicle maintenance)
- Task recommendation AI ("what should I work on?")
- Reflection parsing with suggested updates
- Marie Kondo backlog reviews
