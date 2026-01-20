# CLAUDE.md

Guidance for Claude Code when working in this repository.

## Project

Bear Steps - static website for promoting safe airsteps practice

- **Live:** https://bear-steps.com
- **Hosting:** GitHub Pages (auto-deploy from main)
- **Stack:** Zola v0.22.0 + Tailwind CSS v4
- **Styling:** Utility-first Tailwind (inline classes), @tailwindcss/typography plugin
- **Deploy:** `git push` → GitHub Actions → live site

## Commands

```bash
npm install              # Install dependencies
npm run dev              # Local dev (CSS watch + Zola serve)
npm run build            # Build CSS + site
```

Visit http://127.0.0.1:1111 for local development

## Structure

```
├── content/             # Markdown content (safety-critical)
├── templates/           # Zola templates
│   └── partials/       # Reusable components
├── css/input.css        # Tailwind source
├── static/              # Assets (logo, favicons, CNAME)
└── docs/                # README, CHANGELOG, ROADMAP
```

## Styling Approach

- **Inline Tailwind utilities** - No custom CSS classes for layout/spacing/colors
- **Typography plugin** - `prose` class for content styling
- **Custom CSS only for** - Hamburger animation (pseudo-elements), custom nav-link utility
- **Colors** - gray-900 (headings), gray-800 (body), gray-700 (footer), gray-200 (borders)

## Working Style

**Decision Making**
- Always seek approval before changes (code or content)
- Present options, ask questions
- Use plan mode for non-trivial work

**Content is Safety-Critical**
- Treat safety guidelines/policies with care
- Get approval before modifying

**Documentation**
- Update CHANGELOG.md after changes
- Move completed items in ROADMAP.md
- Keep docs current with project state

**Git Commits**
- Format: Subject (50 chars) + blank line + Why/What body
- Explain why changes were made, not just what changed

## Context

- **Audience:** Event organizers, dancers, aerials community
- **Purpose:** Education and harm reduction
- **Tone:** Clear, authoritative on safety topics