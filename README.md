# Harness Editor

**English** | [한국어](README.ko.md)

> A single-page HTML tool for visually viewing and editing
> `.claude/agents/*.md` and `.claude/skills/**/SKILL.md` files
> used by Claude Code.

🌐 **Try it now:** https://amazingsyp.github.io/harness-editor/harness-editor.html (Chrome / Edge recommended)

---

## Get started in 1 minute

1. Open the link above (Chrome / Edge)
2. Click **📁 Select folder** → choose your project root (the directory that contains `.claude/`)
3. Click any `.md` file in the left tree → start editing

All data stays on **your own machine**. Nothing is uploaded to a server (powered by the browser File System Access API).

## Why?

Building agents and skills with Claude Code is easy, but polishing them — tweaking the frontmatter, refining descriptions, comparing tables across files — gets awkward in a generic editor. This is a small tool focused on that one job.

## Features

- Directory tree view with color-coded agents / skills / orchestrators, plus dirty and error markers
- Frontmatter form editor — separate inputs for `name` / `description` / `type` / `model`
- Markdown body editor + split preview with synced section scrolling
- **WYSIWYG mode** — edit tables, headings, and emphasis directly in the right pane
- Multi-file search and bulk replace (regex, target filters)
- Description-quality scoring (length, trigger phrases, follow-up keywords) aligned with the [revfactory/harness](https://github.com/revfactory/harness) meta-skill recommendations
- Roundtrip-safe serialization — `parse → edit → save` preserves meaning exactly
- Dark / light themes, page-close protection

## Browser support

| Browser | Mode |
|---------|------|
| Chrome / Edge / Brave / Opera | **Directory mode** (recommended) — pick a folder once, edit and save many files in place |
| Safari / Firefox | **Single-file mode** — upload → edit → download |

## Keyboard shortcuts

| Key | Action |
|-----|--------|
| `⌘S` / `Ctrl+S` | Save current file |
| `⌘⇧S` / `Ctrl+Shift+S` | Save all modified files |
| `⌘P` / `Ctrl+P` | Search across all files |
| `⌘⇧H` / `Ctrl+Shift+H` | Bulk replace |
| `⌘B` / `Ctrl+B` | Toggle sidebar |
| `⌘\` / `Ctrl+\` | Toggle preview |
| `Esc` | Close modals |

## Use locally

Download `harness-editor.html` from the repo and double-click it. No installation required — all dependencies are loaded from CDNs at runtime.

## Dependencies (all loaded from CDN)

- [marked.js](https://marked.js.org/) — Markdown rendering
- [js-yaml](https://github.com/nodeca/js-yaml) — Frontmatter YAML parsing & serialization
- [turndown](https://github.com/mixmark-io/turndown) + GFM plugin — HTML → Markdown conversion for the WYSIWYG mode

## Inspiration

This tool is designed to work well with the file format produced by the [revfactory/harness](https://github.com/revfactory/harness) meta-skill — but it works with **any standard Claude Code agent or skill `.md` file**.

## License

[Apache License 2.0](LICENSE) — free to use, modify, and redistribute. See the LICENSE file for details.
