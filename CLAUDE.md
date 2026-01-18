# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website for **Thanaplus Life Center**, a Thai medical clinic specializing in orthopedics and regenerative medicine. The site is entirely in Thai language.

## Technology Stack

- **HTML5** with inline CSS styles (no external CSS files)
- **Bootstrap 4.6.0** via CDN
- **Font Awesome 5.15.3** for icons
- **Google Fonts**: Playfair Display (headings) and Sarabun (body text)
- **jQuery 3.5.1** and Bootstrap JS bundle

## Architecture

### Page Structure
Each HTML page is self-contained with its own `<style>` block. There are no shared CSS files - styles are duplicated across pages with minor variations.

### Design System (CSS Variables)
Pages use a consistent CSS custom properties pattern defined in `:root`:
- `--brand-green: #32c48d` / `--brand-green-dark: #28a375`
- `--brand-blue: #0099cc` / `--brand-blue-dark: #007399`
- `--bg-warm-white: #f9f9f7` or `--bg-light-blue: #f4f9fc`
- `--text-dark: #333333`

### Common Components
- **Top header bar**: Contact info (LINE: @thana_plus, Phone: 098-143-3999)
- **Sticky navbar**: Logo + navigation links
- **Page headers**: Gradient overlay on background images
- **Footer**: Three-column layout with clinic info

### Key Pages
- `index.html` - Homepage with hero section, trust strip, location map
- `about.html` - Doctor profile and clinic information
- `services.html` - List of medical services
- `service-plasma.html` - Detailed service page (PRP treatment)
- `appointment.html` - Appointment booking
- `contactus.html` - Contact information
- `education.html` - Educational content

### Versioned Files
Files ending in `-v2.html` (e.g., `index-v2.html`, `services-v2.html`) are alternate versions used for A/B testing or iteration.

## Development

No build process - open HTML files directly in a browser. For local development, use a simple HTTP server to avoid CORS issues with images:
```bash
python -m http.server 8000
```

## Image Assets

All images are in the root directory (PNG format). Key assets:
- `TP-logo.png` - Clinic logo
- `c3_nolgo.png` - Hero background
- Various medical/service images
