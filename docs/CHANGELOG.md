# Changelog

All notable changes to the Bear Steps website will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [Unreleased]

### Planned
- See [ROADMAP.md](ROADMAP.md) for upcoming features

---

## 2026-01-20 - Navigation Menu Implementation

### Added
- **Top navigation menu** across all pages with 5 main links (Home, Start Here, Resources, About, Testimonials)
- **Unified header partial** (`unified_header.html`) consolidating previous duplicated header logic
- **Mobile hamburger menu** with JavaScript toggle functionality for screens <768px
- **Active page highlighting** in navigation showing current page location
- **CTA button styling** for "Start Here" link with prominent blue button design
- **Mobile menu script partial** (`nav_script.html`) for hamburger toggle interaction

### Changed
- **Template architecture** from three separate header implementations to single unified partial
  - Updated `index.html` to use unified header with "index" context
  - Updated `page.html` to use unified header with "page" context
  - Updated `section.html` to use unified header with "section" context
- **Styling approach** to use Tailwind utility classes inline in HTML markup following Tailwind CSS conventions
  - All navigation styles (layout, colors, spacing, responsive) now use Tailwind utilities
  - Minimal custom CSS retained only for hamburger icon animation (pseudo-elements)
- **Base template** now includes navigation script for mobile menu functionality

### Removed
- `templates/partials/page_header.html` (replaced by unified header)
- `templates/partials/section_header.html` (replaced by unified header)
- Custom CSS for navigation layout, links, and responsive styles (replaced with Tailwind utilities)

### Technical Details
- **Navigation structure**: Flat hierarchy with direct links to all key pages
- **Mobile breakpoint**: 768px (md: in Tailwind) for tablet/mobile responsive design
- **Active state detection**: Uses Zola's `current_path` for highlighting current page
- **Styling**: Tailwind utility classes inline in HTML for all navigation styles
- **Custom CSS**: Only 40 lines for hamburger icon ::before/::after pseudo-elements and animation
- **Accessibility**: Semantic HTML (`<nav>`, `<ul>`, `<li>`), ARIA labels on hamburger button
- **JavaScript**: ~12 lines of vanilla JS for mobile menu toggle (DOMContentLoaded wrapped)

---

## 2026-01-19 - Zola Static Site Generator Migration

### Added
- **Zola v0.22.0** static site generator with template-based architecture
- **Tailwind CSS v4** standalone CLI for styling with custom typography
- **npm build system** with package.json and build scripts (build, build:css, watch:css, dev)
- **Template partials** for header, footer, and head elements (eliminates code duplication)
- **GitHub Actions workflow** using shalzz/zola-deploy-action@v0.22.0 for automated deployment
- **Section template** (section.html) for proper rendering of Zola sections
- **Custom typography styles** for improved content readability
- **CSS classes** for testimonials and announcement copy sections
- **Project documentation** structure (README, CHANGELOG, ROADMAP, CLAUDE.md)

### Changed
- **Migrated from static HTML to Zola** - Converted 9 HTML pages to Markdown format
- **Reorganized content structure** - Created resources/ section with hierarchical organization
  - Moved 5 resource pages into /resources/ section for better URL structure
  - Resources landing page at /resources/, individual resources at /resources/[page]/
- **Build process** managed via npm scripts for consistency across local and CI environments
- **Deployment** from direct HTML serving to GitHub Actions build pipeline
- **Documentation** updated across README, CLAUDE.md with new tech stack and workflows

### Fixed
- CSS typo: font-color → color in .subtitle class
- Broken internal link in airsteps-start-here page to practices-for-safer-airsteps

### Removed
- Old HTML files from content/ directory (9 files)
- Old index.html and styles.css from root directory
- Leftover files from pre-Zola structure

### Technical Details
- **Zero runtime dependencies** - Zola and Tailwind are single binaries
- **Build time** - ~30ms for Tailwind CSS, ~5ms for Zola
- **Content structure** - Markdown files with TOML frontmatter
- **URL structure** - Clean URLs via directory-based routing (/about/, /resources/start-here/)
- **Template hierarchy** - base.html → index.html/page.html/section.html
- **CI/CD** - GitHub Actions with Node.js caching for faster builds

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
