# Changelog

Recent changes to the Bear Steps website.

## 2026-01-20

### Styling Modernization
- Migrated to Tailwind utility-first approach (inline utilities in HTML)
- Integrated @tailwindcss/typography plugin for prose content
- Removed ~250 lines of custom CSS (footer, testimonials, headers, prose)
- Standardized colors: gray-900 (headings), gray-800 (body), gray-700 (footer)
- Standardized borders: all use gray-200 (#e5e7eb)
- Enhanced link visibility: blue, underlined, semi-bold

### Navigation
- Added top navigation menu (Home, Resources, About, Testimonials)
- Mobile hamburger menu (768px breakpoint)
- Unified header partial (replaced 3 separate implementations)
- Active page highlighting
- Updated footer: removed nav links, added copyright and tagline

## 2026-01-19 - Zola Migration

- Migrated from static HTML to Zola v0.22.0 + Tailwind CSS v4
- Converted 9 HTML pages to Markdown
- Reorganized content into hierarchical structure (resources/ section)
- GitHub Actions deployment workflow
- Zero runtime dependencies (Zola and Tailwind are single binaries)

## Earlier Changes

- 2026-01-18: Added testimonials page
- 2025-12-27: Organized content into folders
- 2025-12-04: Added resources and about pages
- 2025-12-03: Added external stylesheet and favicons
- 2025-12-02: Initial release with safety guidelines and branding