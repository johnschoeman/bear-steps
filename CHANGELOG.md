# Changelog

All notable changes to the Bear Steps website will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [Unreleased]

### Planned
- See [ROADMAP.md](ROADMAP.md) for upcoming features

---

## 2026-01-19

### Added
- Populated ROADMAP.md with 15 prioritized items based on current site content and gaps
- Created project documentation structure: enhanced README.md, CHANGELOG.md, and ROADMAP.md
- Updated CLAUDE.md with accurate project information and working style preferences
- Detailed Zola v0.22.0 + Tailwind CSS v4 migration plan for static site generator implementation
- **Zola static site generator** (v0.22.0) for template-based site generation
- **Tailwind CSS v4** standalone CLI for styling
- Template partials for header, footer, and head elements (eliminates code duplication)
- GitHub Actions workflow for automated deployment
- Missing CSS classes: .testimonial and .announcement-copy

### Changed
- **Migrated from static HTML to Zola-powered site** - all 9 pages now use Markdown content with shared templates
- ROADMAP.md now includes specific actionable items across High/Medium/Low priority, content updates, and technical debt
- Expanded SSG roadmap item with technology details (Zola v0.22.0, Tailwind CSS v4), benefits, and scope of migration
- Updated migration plan to use latest versions: Zola v0.22.0 and Tailwind CSS v4 with new @import syntax
- README.md with Zola/Tailwind development workflow
- CLAUDE.md with updated tech stack and build commands
- Deployment from direct HTML to GitHub Actions build pipeline

### Fixed
- CSS typo: font-color → color in .subtitle class

### Technical Details
- Zero runtime dependencies (Zola and Tailwind are single binaries)
- Content now in Markdown format for easier editing
- Template-based architecture eliminates HTML duplication across 9 pages
- Build time: ~6ms for Zola, ~32ms for Tailwind CSS

---

## 2026-01-18

### Added
- Testimonials page with community feedback
- Important section to the "Start Here" documentation

### Changed
- Updated text copy across various pages

## 2025-12-27

### Changed
- Moved content pages to dedicated `content/` folder for better organization

## 2025-12-04

### Added
- Additional resources to resources page
- About section

### Changed
- Reorganized airsteps guidelines to practice guidelines
- Moved safety sections to top of guidelines for better visibility

## 2025-12-03

### Added
- Resources page with links and references
- External stylesheet (styles.css)
- Favicons for better branding

### Changed
- Updated font hierarchy for improved readability
- Enhanced link styling for better visual feedback

## 2025-12-02

### Added
- Airsteps safety guidelines
- Logo added to header with back-link functionality
- CNAME for custom domain (bear-steps.com)
- FAQ section

### Changed
- Initial site structure and content

## 2025-12-02 - Initial Release

### Added
- Initial commit with basic site structure
- Bear Steps logo and branding
- Homepage with core safety message
