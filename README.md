# Bear Steps

Static website promoting safe airsteps practice in the aerials community.

**Live site:** https://bear-steps.com

## About

Safety guidelines, sample policies, educational resources, and community testimonials for event organizers and dancers.

## Tech Stack

- Zola v0.22.0 (static site generator)
- Tailwind CSS v4 (@tailwindcss/typography plugin)
- GitHub Pages (auto-deploy)

## Development

**Setup:**
```bash
npm install
npm run dev     # Visit http://127.0.0.1:1111
```

**Commands:**
- `npm run dev` - Local development (watch CSS + serve site)
- `npm run build` - Build production site
- `npm run css:build` - Build CSS only

**Deploy:** Push to `main` → GitHub Actions → live site

## Structure

```
├── content/             # Markdown content (safety-critical)
├── templates/           # Zola templates
├── css/input.css        # Tailwind source
└── static/              # Assets (logo, favicons)
```

## Contributing

See [docs/ROADMAP.md](docs/ROADMAP.md) for priorities.

## Documentation

- [CHANGELOG.md](docs/CHANGELOG.md) - Recent changes
- [ROADMAP.md](docs/ROADMAP.md) - Planned features
- [CLAUDE.md](docs/CLAUDE.md) - AI development guidelines