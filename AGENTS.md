# AGENTS.md — Notes Making

Static HTML site — no build step, no dev server, no package manager.

## Structure

- `index.html` — landing page (NotesMaster)
- `English.html`, `history.html`, `IP.html`, `political-science.html`, `PE.html` — subject note-taking guides
- `.vscode/settings.json` — trivial cursor setting (safe to ignore)
- `.gitignore` — ignores .vscode/, .DS_Store, Thumbs.db, *.log
- `README.md` — GitHub-facing project description

All pages are self-contained (inline CSS + HTML). Open directly in a browser.

## Dependencies

Google Fonts, Font Awesome, Bootstrap 5.3 (all loaded from CDN). No local deps.

## Conventions

- `index.html`, `history.html`, `English.html`, and `PE.html` share a violet/emerald design system with Instrument Serif + DM Sans and vanilla JS tab navigation (`showTab`).
- `IP.html` and `political-science.html` have divergent styling (Cormorant Garamond + Inter / Inter + Bootstrap).
- All pages use glassmorphism (`backdrop-filter: blur(24px)` on translucent panels) over a dark rich gradient background (`#0c0a1d` → `#1a1035` → `#0f1923` → `#0d0d12`).
- Common glass pattern: `background: rgba(255,255,255,0.06); backdrop-filter: blur(24px); border: 1px solid rgba(255,255,255,0.1); border-radius: var(--radius-lg, 22px);`.
- All pages follow: hero → techniques → templates → examples → memory → revision.

## No tests, no linting, no CI
