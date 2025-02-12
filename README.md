<div align="center">

![quanta-intellect-logo-transparent](https://cdn-uploads.huggingface.co/production/uploads/686c460ba3fc457ad14ab6f8/gB6J60f9Yeyb3Thop2dUa.png)

<a href="https://snapcraft.io/vessel-browser">
    <img alt="Get it from the Snap Store" src=https://snapcraft.io/en/dark/install.svg />
  </a>
  <a href="https://www.producthunt.com/products/quanta-intellect?embed=true&amp;utm_source=badge-featured&amp;utm_medium=badge&amp;utm_campaign=badge-vessel-browser-from-quanta-intellect" target="_blank" rel="noopener noreferrer"><img alt="Vessel Browser from Quanta Intellect - The browser where agents drive and humans supervise | Product Hunt" width="250" height="54" src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=1107491&amp;theme=dark&amp;t=1774779141692"></a>

# Vessel: Your AI-Powered Browser

</div>

Vessel is a simple, clean web browser with an AI assistant built in. Browse the web normally, then ask Vessel to help research, navigate pages, summarize what you are reading, fill forms, or keep track of longer tasks.

Unlike invisible browser automation, Vessel shows you what the AI is doing in a real browser window. You can follow along, approve important actions, pause or redirect the work, and take over whenever you want.

- **A familiar browser, with AI help nearby** — tabs, bookmarks, reader mode, downloads, and a sidebar assistant for web tasks
- **Great for longer browsing sessions** — durable conversation threads, a cross-source run inbox, named sessions, checkpoints, notes, bookmarks, and page changes make interrupted work recoverable
- **You stay in control** — review what the AI is doing, approve sensitive actions once or for a scoped run/domain, reject with steering, undo recent changes, and switch back to manual browsing at any time
- **Open source and extensible** — built on Chromium, with advanced automation support for MCP clients and agent tools when you need it

Linux is the most mature install target today. macOS release packaging is available from source.

_Vessel is in active development. Treat it as early software, especially for sensitive browsing or account access._

https://github.com/user-attachments/assets/0a72b48a-873a-4eb0-b8f2-23e34d8472c4

## Quick Start

Want the complete AI toolkit from day one? [Start a 7-Day Free Trial of Vessel Premium — $5.99/mo](https://vesselpremium.quantaintellect.com/checkout).

### Fastest Install Today

Linux AppImage from GitHub Releases:

1. Download the latest `Vessel-<version>-x64.AppImage`
2. Mark it executable: `chmod +x Vessel-*.AppImage`
3. Launch it: `./Vessel-*.AppImage`
4. Open Settings (`Ctrl+,`) to choose your AI provider and review advanced connection options

### Install via npm

```bash
npm install -g @quanta-intellect/vessel-browser
vessel-browser
```

Or run it directly without installing:

```bash
npx @quanta-intellect/vessel-browser
```

### Source Install

```bash
curl -fsSL https://raw.githubusercontent.com/unmodeled-tyler/vessel-browser/main/scripts/install.sh | bash
```

### Development From Source

Vessel development uses Node.js 22. If you use `fnm`, run `fnm use` from the repo root to pick up `.node-version`.

```bash
fnm use
npm install
npm run dev
```

If you want extra local AI tracing in development, create an optional `src/main/telemetry/trace-logger.local.cjs` file. Vessel will load it only in local dev builds, and packaged production builds ignore it.

### Why Vessel?

Most AI tools can answer questions about the web. Vessel is for actually working on the web: reading pages, following links, comparing information, filling forms, tracking changes, and keeping longer browsing sessions organized.

<img width="1280" height="800" alt="Vessel Browser supervisor sidebar showing agent workflow controls" src="https://github.com/user-attachments/assets/8e208ee1-cb89-4318-87a2-9561a7d9aecf" />
<img width="1280" height="800" alt="Vessel Browser command bar and agent-driven page interaction" src="https://github.com/user-attachments/assets/da7b28ea-6c5f-4aa7-909e-0a255c80d508" />
<img width="1280" height="800" alt="Vessel Browser persistent session and checkpoint interface" src="https://github.com/user-attachments/assets/3b3d2033-5a59-4806-bbc1-359efb7b43a9" />

<img width="1280" height="800" alt="Vessel Browser integrated chat assistant with browser tools" src="https://github.com/user-attachments/assets/b1c08d6c-bcdf-4c9a-8429-a71a23a61903" />

Vessel keeps that work visible. The AI uses a real browser, so you can see the pages it opens, the choices it makes, and the places where it needs your approval. You are never stuck watching a hidden automation run or guessing what happened after the fact.

For power users and developers, the same foundation also supports external agents, MCP clients, persistent sessions, checkpoints, and browser automation workflows.

## Features

- **AI-assisted browsing** — ask Vessel to help with research, page reading, navigation, form work, and multi-step web tasks
- **Human-visible browser UI** — pages render like a normal browser so AI activity stays legible instead of disappearing into a hidden run
- **Command Bar** (`Ctrl+L`) — a secondary operator surface for harness-driven workflows and future runtime commands
- **Supervisor Sidebar** (`Ctrl+Shift+L`) — live supervision across ten tabs, including a durable Run Inbox, conversation Threads, approvals, checkpoints, changes, and Research
- **Chat Assistant** — built-in conversational AI in the sidebar Chat tab; supports Anthropic, OpenAI, Ollama, llama.cpp, Mistral, xAI, Google Gemini, OpenRouter, and any OpenAI-compatible endpoint; reads the current page automatically; has full access to the same browser tools as external agents; multi-turn session history; configure provider, model, and API key in Settings
- **Skills** (Premium) — reusable browser skills in the sidebar Skills tab; import, view, run, or delete skills the built-in agent can use for research, shopping, and site-specific workflows
- **Research Desk** (Beta) — a dedicated sidebar Research tab for structured research reports; start with a topic, complete an in-tab briefing, let Vessel draft research objectives, approve the plan, then dispatch browser sub-agents to collect source-backed claims and synthesize a markdown-exportable report. Starting the brief is free; plan approval, sub-agent execution, and report export require Vessel Premium.
- **Dev Tools Panel** (`F12`) — inspect console output, network requests, and MCP/agent activity in a resizable panel at the bottom of the window; export logs by category and date range as JSON
- **Browser Basics For Long Runs** — pinned tabs stay compact at the front of the tab strip and are protected from accidental close; tab groups can be color-coded and collapsed; audible tabs show audio indicators with mute controls; open additional browser windows with `Ctrl+N`; print the active page with `Ctrl+P` or save it directly as PDF with `Ctrl+Shift+P`
- **Action Undo / Rollback** — restore the browser to the session snapshot captured immediately before the last successful mutating agent action; available from the Supervisor tab and through the `undo_last_action` tool
- **Durable Run Inbox** — Chat, MCP, scheduled, and Research work share one persisted lifecycle with status filters, parent/child research runs, redacted inputs, outputs, errors, and tab context
- **Persistent Conversation Threads** — group multiple independent chats inside named threads; each chat gets an AI-generated title after its first completed exchange and can be reopened or retitled, while threads can be renamed, archived, or deleted; archived threads follow the configured history period
- **Scoped Approval Policies** — approve once, approve for a run, approve for a domain, or reject and steer; explicit denies take precedence and expired scoped rules are ignored
- **Agent-Meaningful Bookmarks** — bookmarks carry structured context the agent can read and act on: `intent` (what the page is for), `expectedContent` (what to expect on the page), `keyFields` (important form fields), `agentHints` (arbitrary directives), and a stored `pageSchema`; humans can create and edit this metadata directly in the Bookmarks tab, and all fields are searchable
- **Portable Bookmark Export** — export browser-compatible Netscape HTML for import into Chrome, Firefox, Safari, Edge, Brave, and other browsers; optionally include Vessel notes/agent metadata, or export a full-fidelity Vessel JSON archive
- **Page Schema Inference** — Vessel automatically infers a typed schema for every page: `pageType` (article, product, form, search, checkout, login, dashboard), `primaryEntity` (structured fields for products and articles), `formFields` (with names, types, labels, selectors), and `actionButtons` (with inferred intents: submit, addToCart, login, etc.); schema is attached to every content extraction result
- **Bookmarks for Agents** — save pages into folders, attach one-line folder summaries, and search bookmarks over MCP instead of dumping the entire library
- **Named Session Persistence** — save cookies, localStorage, and current tab layout under a reusable name, then reload it after a restart
- **Annotated Checkpoints** — capture and restore short-lived browser recovery points with names and editable notes, so humans and agents can mark why a checkpoint matters before risky flows
- **Page Highlights** — agents can visually highlight text or elements on any page with labeled, color-coded markers that persist across navigation; highlight count and navigation controls appear in the sidebar; cleared explicitly or via tool call
- **Agent Transcript Dock** — floating transcript overlay anchored to the browser chrome; configurable display modes (off, summary, full) set in Settings; shows live agent thinking and status updates without occupying sidebar space
- **Workflow Flow Tracking** — agents can declare a named multi-step workflow at runtime using `flow_start`; progress is tracked step-by-step with `flow_advance` and visible in the sidebar throughout execution
- **Structured Page Visibility Context** — extraction can report in-viewport elements, obscured controls, active overlays, and dormant consent/modal UI
- **Popup Recovery Tools** — agents can explicitly dismiss common popups, newsletter gates, and consent walls instead of brute-forcing generic clicks
- **Form Autofill Profiles** — save reusable personal or work profiles in Settings and fill common contact, address, and organization fields on the current page; Vessel matches fields using labels, names, placeholders, and autocomplete hints
- **Page Diff / "What Changed?"** — Vessel remembers the last snapshot of a page and surfaces a `Changed` badge in the address bar when the title, headings, or main content differ on a later visit; expand it to see a compact summary of what changed since the last snapshot
- **What Changed Timeline** (Premium) — the sidebar Changes tab keeps a per-page history of recent change bursts, showing when each update was detected and a compact summary of what changed
- **Per-Tab Ad Blocking Controls** — tabs default to ad blocking on, but agents can selectively disable and re-enable blocking when a page misbehaves
- **Domain Policy** — allowlist or blocklist domains globally in Settings; agents cannot navigate to blocked domains
- **Agent Credential Vault** (Premium) — encrypted credential storage for agent-driven logins; credentials are filled directly into login forms via a "blind fill" pattern and are never sent to AI providers; user consent dialog before every use; TOTP 2FA support; domain-scoped access; append-only audit log
- **Screenshot & Visual Analysis** (Premium) — take a full-page screenshot and pass the image directly to the AI for visual layout analysis; useful when text extraction fails on heavy or canvas-rendered pages
- **Obsidian Memory Hooks** (Premium) — optional vault path for agent-written markdown notes, page captures, and research breadcrumbs
- **Runtime Health Checks** — startup warnings for MCP port conflicts, unreadable settings, and user-data write failures
- **Reader Mode** — extract article content into a clean, distraction-free view; toggle on and off from the address bar
- **Focus Mode** (`Ctrl+Shift+F`) — hide all chrome, content fills the screen
- **Resizable Panels** — drag the sidebar edge to resize; width persists across sessions
- **Minimal Dark Theme** — warm dark grays, restrained accent color, and no pure black/white

### Reliability, History, and Approvals

The Supervisor sidebar now keeps longer-running work understandable across Chat, external MCP agents, scheduled jobs, and Research:

- Open **Runs** to filter work that needs attention, is active, failed, completed, or comes from any source. Each run has a chronological timeline with status changes, approvals, outputs, errors, and relevant tab context; records can be exported as Markdown or JSON or deleted from Vessel.
- Open **Threads** to organize multiple chats under a named topic. Chats can be reopened or retitled independently, while their parent thread can be renamed, archived, or deleted. New chats receive a generated title after their first completed exchange.
- Approval cards show the action, redacted arguments, domain, and whether undo is available. You can approve once, approve matching work for the current run or domain, reject, or reject with written steering. Persisted scoped rules remain visible in Supervisor and can be removed there.
- If Vessel closes while a run is active or waiting for approval, that run is marked **interrupted** on the next launch instead of being left misleadingly active. Vessel does not claim to resume or retry the unfinished execution automatically.
- Terminal run history and archived threads follow `historyRetentionDays` (`90` days by default; supported values are `7`, `30`, `90`, `180`, `365`, or `null` for no automatic expiry). Active runs and unarchived threads are preserved.

Conversation history is encrypted through Electron's `safeStorage` API when encryption is available. If secure storage is unavailable, Vessel keeps conversations in memory for that session instead of writing plaintext chat history. Run records redact sensitive argument fields and limit stored output size before persistence or export.

## Positioning

Most browsers treat automation as secondary and assume a human is the primary actor. Vessel is the opposite: it is the browser for the agent, with a visible interface that keeps the human in the loop.

That means the product should optimize for:

- persistent browser state across tasks and sessions
- clear visibility into what the agent is doing right now
- lightweight human intervention instead of constant manual driving
- a browser runtime that can serve long-lived agent systems such as Hermes Agent or OpenClaw-style harnesses

## Stack

| Layer              | Technology                                                                                                                                             |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Engine             | Chromium (Electron 40)                                                                                                                                 |
| UI Framework       | SolidJS                                                                                                                                                |
| Language           | TypeScript                                                                                                                                             |
| Build              | electron-vite + Vite                                                                                                                                   |
| AI Control         | External agent harnesses (Hermes Agent, OpenClaw, MCP clients) + built-in chat (Anthropic, OpenAI, Ollama, llama.cpp, and any OAI-compatible endpoint) |
| Content Extraction | @mozilla/readability                                                                                                                                   |

## Architecture

```
Main Process                                  Renderer (SolidJS)
├── TabManager (WebContentsView[])            ├── TabBar, AddressBar
├── AgentRuntime (session + supervision)      ├── CommandBar (secondary surface)
├── Run, conversation, and policy managers    ├── AI Sidebar (Supervisor/Runs/Threads/Chat/...)
├── MCP server for external agents            ├── DevTools Panel (Console/Network/Activity)
├── AI providers (Anthropic + OAI-compatible) ├── Agent Transcript Dock
├── Bookmarks, checkpoints, and page history  └── Signal stores (runtime/runs/conversations/policies/...)
└── IPC handlers ◄──contextBridge──► Preload API
```

Each browser tab is a separate `WebContentsView` managed by the main process. The browser chrome (SolidJS) runs in its own view layered on top. All communication between renderer and main goes through typed IPC channels via `contextBridge`.

The sidebar Skills tab renders skill forms entirely in the renderer and passes the rendered prompt to the built-in agent via the same `query()` path used by the Chat tab — no additional IPC surface is needed. The Changes tab reads the current page's diff timeline through IPC and unlocks persisted history for Premium users. The Research tab has a dedicated IPC surface for its state machine: briefing is available to everyone, while objective approval, parallel browser sub-agents, report synthesis, and markdown export are Premium-gated during the beta.

## Getting Started

The installer:

- clones or updates Vessel into `~/.local/share/vessel-browser`
- installs dependencies and builds the app
- creates a `vessel-browser` launcher in `~/.local/bin`
- creates a `vessel-browser-launch` helper in `~/.local/bin`
- creates a `vessel-browser-update` helper in `~/.local/bin`
- creates a `vessel-browser-status` helper in `~/.local/bin`
- creates a desktop entry for Linux app launchers
- writes `~/.config/vessel/vessel-settings.json` with MCP port `3100`
- writes `~/.config/vessel/mcp-stdio-snippet.json`
- writes `~/.config/vessel/mcp-http-snippet.json`
- installs a `vessel-browser-mcp` helper that can run as a stdio-to-HTTP proxy (`--stdio`) or print config snippets
- prints the exact recommended stdio MCP snippet to paste into your harness config

The packaged AppImage path:

- does not require a local Node/Electron toolchain
- uses the packaged Vessel app icon and metadata
- is the recommended path for early adopters who just want to run Vessel

Windows packaged releases:

- use the `Vessel-<version>-x64-setup.exe` NSIS installer
- can be installed over an existing Vessel install when upgrading
- preserve Vessel app data during the normal upgrade path

You do not need to uninstall Vessel before installing a newer Windows release. Uninstall first only if you are recovering from a broken install or intentionally removing local Vessel data.

After install:

```bash
vessel-browser
```

```bash
# Use the pinned Node.js 22 runtime
fnm use

# Install dependencies
npm install

# If Electron download fails, use a mirror:
ELECTRON_MIRROR="https://npmmirror.com/mirrors/electron/" npm install

# Development (with HMR)
npm run dev

# Production build
npm run build

# Smoke-test the MVP release path
npm run smoke:test

# Package an unpacked Linux app
npm run dist:dir

# Package a Linux AppImage
npm run dist

# Package an unpacked universal macOS app bundle (run on macOS)
npm run dist:mac:dir

# Package universal macOS DMG + ZIP artifacts (run on macOS)
npm run dist:mac

# Verify a universal macOS build contains Intel and Apple Silicon slices
npm run verify:mac:universal

# Package signed macOS DMG + ZIP artifacts (run on macOS with signing set up)
npm run dist:mac:si