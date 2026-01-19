# Bear Steps

A static website for the Bear Steps aerials practice group, providing safety guidelines, resources, and community information for airsteps practice.

Live site: https://bear-steps.com

## About Bear Steps

Bear Steps is dedicated to promoting safe airsteps practice in the aerials community. The site provides:
- Safety guidelines and best practices
- Sample policies for event organizers
- Educational resources
- Community testimonials
- "Start here" guide for newcomers

## Tech Stack

- **Static Site Generator**: Zola v0.22.0 (Rust-based, single binary)
- **CSS Framework**: Tailwind CSS v4 (standalone CLI, single binary)
- **Hosting**: GitHub Pages
- **Deployment**: Automatic via GitHub Actions

## Project Structure

```
bear-steps/
├── config.toml             # Zola configuration
├── tailwind.config.js      # Tailwind CSS configuration
├── content/                # Markdown content files
│   ├── _index.md          # Homepage
│   ├── about.md
│   ├── airsteps-start-here.md
│   ├── resources.md
│   ├── testimonials.md
│   └── [sample policies and guidelines].md
├── templates/              # Zola templates
│   ├── base.html
│   ├── index.html
│   ├── page.html
│   └── partials/
│       ├── head.html
│       ├── header.html
│       └── footer.html
├── styles/
│   └── input.css          # Tailwind CSS source
├── static/                 # Static assets (served from root)
│   ├── bear-steps-logo.png
│   ├── styles.css         # Built CSS (gitignored)
│   ├── CNAME
│   └── [favicons]
└── public/                 # Build output (gitignored)
```

## Getting Started

### Prerequisites

- Zola v0.22.0 - [Download](https://github.com/getzola/zola/releases/tag/v0.22.0)
- Tailwind CSS v4 standalone CLI - [Download](https://github.com/tailwindlabs/tailwindcss/releases/latest)

Both are single binaries with zero runtime dependencies.

### Local Development

1. **Build Tailwind CSS** (in one terminal):
```bash
tailwindcss -i ./styles/input.css -o ./static/styles.css --watch
```

2. **Run Zola dev server** (in another terminal):
```bash
zola serve
```

3. Visit `http://127.0.0.1:1111`

The site will auto-reload when you make changes to content or templates.

### Making Changes

#### Content Updates

Edit Markdown files in `content/` directory:
- Frontmatter defines page metadata (title, description)
- Content is written in Markdown
- Internal links use format: `[Link Text](/page-slug/)`

#### Style Updates

Edit `styles/input.css` with custom CSS or Tailwind utilities.
Tailwind will rebuild automatically if running with `--watch`.

#### Template Updates

Edit templates in `templates/` directory:
- `base.html` - Base HTML structure
- `page.html` - Standard content pages
- `index.html` - Homepage
- `partials/` - Reusable components

### Deployment

1. Commit and push to main branch
2. GitHub Actions automatically builds and deploys
3. Changes appear at bear-steps.com within 1-2 minutes

## Contributing

See [ROADMAP.md](ROADMAP.md) for planned features and priorities.

## Documentation

- [CHANGELOG.md](CHANGELOG.md) - Recent changes and version history
- [ROADMAP.md](ROADMAP.md) - Upcoming priorities and planned features
- [CLAUDE.md](CLAUDE.md) - AI assistant development guidelines
