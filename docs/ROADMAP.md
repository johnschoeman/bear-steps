# Roadmap

This document outlines upcoming priorities and planned features for the Bear Steps website.

## High Priority

- [ ] **Add Contact Information** - Testimonials page mentions "Contact us" but no contact method exists. Add email address, contact form, or social media link.
- [ ] **Expand Homepage FAQ** - Currently only one Q&A. Add 5-10 more common questions about consent, where to practice, how to get started, etc.
- [ ] **Mobile Responsiveness Testing** - Test across devices and improve mobile formatting for long text pages.

## Medium Priority

- [ ] **Expand About Page** - Add history of Bear Steps, who runs it, how to join, expanded mission statement. Currently only 3 paragraphs.
- [ ] **Add More Testimonials** - Currently only 3 testimonials. Actively collect more stories from the community.
- [ ] **SEO and Meta Tags** - Add meta descriptions for each page, OpenGraph tags for social sharing, improve page titles.
- [ ] **Visual Enhancements** - Add photos/illustrations to break up text-heavy pages, icons for key safety points, profile photos for testimonials (with permission).

## Low Priority / Future Considerations

- [ ] **Analytics** - Add analytics to understand which resources are most used and track page views to prioritize content development.
- [ ] **Search Functionality** - As content grows, add search to help people find specific topics.
- [ ] **Community Features** - Map of practice groups using Bear Steps resources, directory of instructors teaching safe air steps practices.

## Content Updates Needed

- [ ] **Expand Resources Page** - Add more external links (instructional videos, related organizations), better categorization, instructor recommendations or certification resources.
- [ ] **More Sample Policies** - Add policies for different event types (competitions, workshops, social dances), regional variations or considerations.

## Technical Debt / Improvements

- [ ] **Accessibility Audit** - Check heading hierarchy, ensure good color contrast, add ARIA labels where helpful.
- [ ] **CSS Organization** - Implement CSS variables for consistent theming as styles grow.

---

## Completed

### 2026-01-20 - Navigation Menu

**Add Navigation Menu** - Added consistent top navigation for better usability
- Created unified header partial consolidating three separate header implementations
- Implemented 5-link navigation (Home, Start Here, Resources, About, Testimonials)
- Added "Start Here" as prominent CTA button with blue styling to emphasize safety content
- Built mobile-responsive hamburger menu with JavaScript toggle (breakpoint: 768px)
- Implemented active page highlighting for user orientation
- Removed old page_header.html and section_header.html partials (replaced by unified header)
- Added comprehensive navigation styles with hover states and mobile responsive design
- Enhanced accessibility with semantic HTML and ARIA labels

### 2026-01-19 - Static Site Generator Migration

**Implement Static Site Generator** - Migrated to Zola v0.22.0 + Tailwind CSS v4
- Converted 9 HTML files to Markdown format
- Created reusable template partials for header, footer, and navigation
- Implemented GitHub Actions workflow for automated deployment with zola-deploy-action
- Added npm build system with scripts for development and production
- Reorganized content into hierarchical structure with resources/ section
- Created custom typography styles for improved readability
- Added missing CSS classes (.testimonial, .announcement-copy)
- Fixed CSS typo (font-color → color)
- Removed all old HTML files following Zola conventions
- Zero runtime dependencies (both Zola and Tailwind are single binaries)

---

**Last Updated:** 2026-01-20

**Note:** This is a living document. Update it regularly as priorities shift and work is completed.
