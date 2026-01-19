# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Bear Steps is a static website for an aerials practice group focused on promoting safe airsteps practice. The site provides safety guidelines, sample policies for event organizers, educational resources, and community testimonials.

**Live site:** https://bear-steps.com
**Hosting:** GitHub Pages (auto-deploys from main branch)

## Current State

- **Tech Stack**: Zola v0.22.0 (static site generator) + Tailwind CSS v4
- **Build System**: Zola for site generation, Tailwind CSS standalone CLI for styling
- **Dependencies**: Two single binaries (Zola + Tailwind), zero runtime dependencies
- **Testing**: Not configured
- **Deployment**: Automatic via GitHub Actions on push to main branch

## Project Structure

```
├── config.toml                  # Zola configuration
├── tailwind.config.js           # Tailwind CSS configuration
├── content/                     # Markdown content files
│   ├── _index.md               # Homepage
│   ├── about.md
│   ├── airsteps-start-here.md
│   ├── resources.md
│   ├── testimonials.md
│   └── [various policy samples].md
├── templates/                   # Zola templates
│   ├── base.html
│   ├── index.html
│   ├── page.html
│   └── partials/
│       ├── head.html
│       ├── header.html
│       └── footer.html
├── styles/
│   └── input.css               # Tailwind CSS source
├── static/                      # Static assets
│   ├── bear-steps-logo.png
│   ├── styles.css              # Built CSS (gitignored)
│   ├── CNAME
│   └── [favicons]
├── public/                      # Build output (gitignored)
├── README.md                    # Project overview
├── CHANGELOG.md                 # Version history
├── ROADMAP.md                   # Upcoming priorities
└── CLAUDE.md                    # This file
```

## Development Commands

**Install dependencies:**
```bash
npm install
```

**Build CSS:**
```bash
npm run build:css
```

**Build site:**
```bash
npm run build
```

**Local development:**
```bash
npm run dev
```

This runs both CSS watch mode and Zola serve. Visit `http://127.0.0.1:1111`

**Deploy**: Push to main branch (GitHub Actions builds and deploys to bear-steps.com)

## Working Style Preferences

### Technology Approach
- **Keep it simple**: Prefer minimal dependencies and straightforward solutions
- **Single binaries**: Using Zola and Tailwind standalone CLI (no npm/node runtime dependencies)
- **Static generation**: Content in Markdown, templates for structure, zero JavaScript on frontend
- **Pragmatic about tools**: Current stack (Zola + Tailwind) chosen for: zero runtime deps, template partials, fast builds

### Decision Making
- **Always seek approval first**: Present options and get approval before making any changes (code or content)
- **Use plan mode**: For non-trivial changes, use plan mode to propose an approach before implementation
- **Ask questions**: When multiple approaches exist, ask which direction to take rather than choosing independently

### Content Changes
- **Treat content with care**: Safety information and policies are critical - always get approval before modifying
- **Same rigor for code and content**: Apply the same approval process to both technical changes and content changes

### Documentation
- **Auto-update CHANGELOG.md**: After approved changes, automatically update CHANGELOG.md with what changed and why
- **Update ROADMAP.md**: Move completed items to the "Completed" section automatically
- **Keep docs in sync**: Ensure README, CHANGELOG, and ROADMAP stay current with project state

### Git Practices

- **Detailed commit messages**: Write commit messages that explain what changed AND why
  - Good: "Add testimonials page to build community trust and provide social proof for event organizers"
  - Not: "Add testimonials page"

- **Commit message format**:

1. Separate subject from body with a blank line
2. Limit the subject line to 50 characters
3. Capitalize the subject line
4. Do not end the subject line with a period
5. Use the imperative mood in the subject line
6. Wrap the body at 72 characters
7. Use the body to explain what and why vs. how

# Title: Summary, imperative, start upper case
# No more than 50 chars. #### 50 chars is here:  #
#
# Remember blank line between title and body.
#
# Body: Explain *why* and *what* (not *how*)
# Wrap at 72 chars. ################################## which is here:  #

- example commit message:

```
Add testimonals page

Why:

We want new dancers to understand the community values of safety. One
powerful way to do this is to provide social evidence of the value
through testimonials.

This commit:

Introduces a testimonials page and adds a few testimonials from
community members.

```

## Important Context

- **Audience**: Event organizers, airsteps practitioners, aerials community
- **Safety-critical**: Content about safety practices and policies must be accurate and clear
- **Community-driven**: The site reflects community input and best practices
- **Educational focus**: Primary goal is education and harm reduction

## Common Tasks

When asked to make changes:
1. Read relevant files first to understand current state
2. Present options or proposed approach
3. Get approval before proceeding
4. Make approved changes
5. Update CHANGELOG.md automatically
6. Update ROADMAP.md if completing planned items
7. Create detailed commit messages explaining the why
