# Pollinations Studio — AI Generation Suite

A single-file, production-ready AI generation interface built with pure HTML, CSS, and vanilla JavaScript.  
Designed for static deployment (e.g., GitHub Pages, Cloudflare Pages) with zero backend requirements.

The application provides a unified interface for:

- Text-based chat (LLM-style streaming)
- Image generation
- Audio generation
- Video generation
- Session history management
- Local file attachments
- Markdown rendering

---

## Architecture Overview

This project is intentionally implemented as a **self-contained `index.html`** file.

### Key Characteristics

- No build system
- No framework dependency
- No server-side runtime
- Fully client-side execution
- Static hosting compatible

All UI logic, layout, styling, and state handling are embedded directly in the HTML file.

---

## Core Features

### 1. Multi-Modal Panels

The interface supports multiple AI generation modes:

- Chat (streaming assistant responses)
- Image output panel
- Audio output panel
- Video output panel

Each panel includes:
- Configurable parameters
- Model selection
- Status tracking
- Output preview
- Download support

---

### 2. Chat System

- Streaming message rendering
- Markdown parsing (`marked.js`)
- Code block formatting
- Message history
- Attachment previews
- Copy-to-clipboard support
- Local rename & session management

---

### 3. History Sidebar

- Persistent session history
- Search filtering
- Pinning support
- Context menu actions
- Rename modal
- Deletion controls

State is handled client-side.

---

### 4. Theming & Design System

The UI is built using a structured design token system:

- CSS custom properties (`:root` variables)
- Dark-first theme
- Structured surface hierarchy
- Consistent radius and spacing system
- Subtle motion transitions
- Responsive breakpoints

Typography stack:
- Cormorant Garamond
- Outfit
- JetBrains Mono

---

### 5. Responsive Layout

Breakpoints:
- 960px
- 720px
- 600px
- 400px

Mobile behavior includes:
- Collapsible sidebars
- Horizontal nav mode
- Adjusted spacing and layout stacking

---

## Security Considerations

- API keys are entered client-side.
- No server proxy is included.
- Sensitive keys should be restricted at provider level (CORS, domain lock, or token scoping).

For production environments requiring secure key handling, implement:
- A Cloudflare Worker proxy
- Rate limiting
- Server-side token validation

---

## Performance Profile

- No runtime framework overhead
- No virtual DOM
- Minimal external dependencies
- Lightweight CSS architecture
- Fast first paint under static hosting

Optimized for:
- Low latency
- Edge deployment
- Client-side interaction responsiveness

---

## External Dependencies

| Library | Purpose |
|---------|----------|
| marked.js | Markdown rendering |

All other logic is native JavaScript.

---

## Project Philosophy

This project prioritizes:

- Structural clarity
- Design coherence
- Static deployability
- Framework independence
- Maintainability within a single file

It is intended as a foundation for:

- AI studio dashboards
- Personal AI tooling
- Experimental multi-modal interfaces
- Edge-deployed AI clients

---

## License

MIT
