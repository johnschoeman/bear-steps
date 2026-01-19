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

- **Frontend**: Static HTML5, CSS3
- **Hosting**: GitHub Pages
- **Deployment**: Automatic via git push to main branch

## Project Structure

```
bear-steps/
├── index.html              # Homepage with FAQ
├── styles.css              # Global styles
├── bear-steps-logo.png     # Site logo
├── content/                # Content pages
│   ├── about.html
│   ├── airsteps-start-here.html
│   ├── resources.html
│   ├── testimonials.html
│   └── [sample policies and guidelines]
└── static/                 # Favicons and static assets
```

## Getting Started

### Local Development

Simply open the HTML file in your browser:

```bash
open index.html
```

Or serve with a local web server:

```bash
python -m http.server 8000
# or
npx serve .
```

Then visit `http://localhost:8000`

### Making Changes

1. Edit HTML/CSS files directly
2. Test locally in your browser
3. Commit and push to main branch
4. Changes deploy automatically to bear-steps.com

## Contributing

See [ROADMAP.md](ROADMAP.md) for planned features and priorities.

## Documentation

- [CHANGELOG.md](CHANGELOG.md) - Recent changes and version history
- [ROADMAP.md](ROADMAP.md) - Upcoming priorities and planned features
- [CLAUDE.md](CLAUDE.md) - AI assistant development guidelines
