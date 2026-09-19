# AGENTS.md — Mid-MO Amateur Radio Club (MMARC) Website

This document serves as an operational guide for LLM coding agents and developers working on the [MMARC Website](https://k0ety.net) repository.

---

## 1. Project Overview

- **Organization**: Mid-MO Amateur Radio Club (Callsign: **K0ETY**)
- **Location**: Jefferson City, Missouri, USA
- **Domain**: `https://k0ety.net`
- **Purpose**: Club announcements, event coordination, meeting minutes archives (dating back to 1997), repeater information, member tools, and historical preservation.

---

## 2. Technology Stack & Framework

| Layer | Technology | Details |
| :--- | :--- | :--- |
| **Static Site Generator** | **Jekyll** (Ruby) | Standard Jekyll static site engine. |
| **Templating Engine** | **Liquid** | Jekyll's default templating system (`{{ ... }}`, `{% ... %}`). |
| **CSS Framework** | **Tailwind CSS** | Loaded via CDN (`https://cdn.tailwindcss.com?plugins=typography`) in `_includes/head.html`. |
| **JavaScript / State** | **Alpine.js** (v3) | Loaded via CDN (`jsdelivr`) for mobile navigation, dark mode toggling, and interactive apps. |
| **Hosting & Deployment** | **GitHub Pages** | Built automatically upon push to default branch; custom domain configured via `CNAME` (`k0ety.net`). |
| **PWA Support** | Service Worker & Manifest | `sw.js` and `manifest.json` for offline caching and mobile installation. |

---

## 3. Directory Structure & Key Files

```text
mmarc-website/
├── _activities/           # Collection: Club activities & awards (e.g. Hammond Award)
├── _includes/             # Reusable HTML partials
│   ├── footer.html        # Site footer, repeater info, meeting times, social links
│   ├── head.html          # HTML <head>, Tailwind config, Alpine.js, fonts, PWA registration
│   └── header.html        # Navigation bar, mobile menu, dark mode toggle
├── _layouts/              # Jekyll layout templates
│   ├── default.html       # Base HTML shell with header/footer & Alpine theme store
│   ├── grid-index.html    # Grid-based archive/list view layout
│   ├── minute.html        # Meeting minutes view layout
│   └── post.html          # Blog post layout
├── _minutes/              # Collection: Over 200+ monthly meeting minutes (Markdown)
├── _operating/            # Collection: Operating guides & technical write-ups
├── _posts/                # Collection: Club news & announcements (Jekyll blog format)
├── assets/                # Static assets
│   ├── css/               # Custom stylesheets (e.g. main.css)
│   ├── images/            # Images, logos, photos
│   └── docs/              # PDFs, forms, bylaws
├── members/               # Interactive tools & member applications
│   ├── digital-historian.html # Semantic AI archive search (Beta)
│   ├── index.html         # Members area hub
│   ├── lookup.html        # FCC Callsign Lookup tool
│   ├── net-report.html    # Net Control Station reporting tool
│   └── repeater-listen.html # Live audio streaming for club repeaters
├── minutes/               # Historical minutes index & archive browser
│   └── index.html         # Minutes index grouped by year/month
├── n0ss/                  # LEGACY MIRROR: Preserved archive of Tom Hammond (N0SS, SK)
├── _config.yml            # Main Jekyll configuration (collections, permalinks, plugins)
├── Gemfile                # Ruby gem dependencies
├── Gemfile.lock           # Locked gem versions
├── CNAME                  # Custom domain configuration (k0ety.net)
├── manifest.json          # Web app manifest for PWA capabilities
├── sw.js                  # Service worker for offline caching
└── README.md              # Human-facing project documentation
```

---

## 4. Local Development Workflow

### Prerequisites
- **Ruby**: Version 2.7 or higher
- **Bundler**: `gem install bundler`

### Setup & Execution Commands
```bash
# Install ruby dependencies
bundle install

# Run the local development server (accessible at http://localhost:4000)
bundle exec jekyll serve

# Run with live reloading and drafts enabled
bundle exec jekyll serve --livereload --drafts

# Build static output only (creates _site/)
bundle exec jekyll build
```

---

## 5. Content Collections & Front Matter Guide

### 5.1 Meeting Minutes (`_minutes/`)
- **Naming format**: `YYYY-MM-DD-title.md` or `YYYY-MM-DD-month.md` (e.g., `2026-01-08-january.md`)
- **Permalink rule**: `/minutes/:year/:month/:title/` (configured in `_config.yml`)
- **Front Matter schema**:
  ```yaml
  ---
  layout: minute
  title: "January 2026 Meeting Minutes"
  date: 2026-01-08
  ---
  ```

### 5.2 News & Blog Posts (`_posts/`)
- **Naming format**: `YYYY-MM-DD-title.md` (e.g., `2026-02-12-welcome.md`)
- **Permalink rule**: `/blog/:year/:month/:day/:title/`
- **Front Matter schema**:
  ```yaml
  ---
  layout: post
  title: "Post Title"
  date: 2026-02-12 12:00:00 -0600
  categories: news
  excerpt: "Short summary of the post" # Optional
  ---
  ```

### 5.3 Club Activities (`_activities/`)
- **Naming format**: `slug.md` (e.g., `hammond-award.md`)
- **Permalink rule**: `/activities/:slug/`
- **Front Matter schema**:
  ```yaml
  ---
  layout: post
  title: "The Hammond Award"
  ---
  ```

### 5.4 Operating Guides (`_operating/`)
- **Naming format**: `slug.md` or `YYYY-MM-DD-slug.md` (e.g., `2026-02-12-hf-go-kit.md`)
- **Permalink rule**: `/operating/:slug/`
- **Front Matter schema**:
  ```yaml
  ---
  layout: post
  title: "HF Go Kit"
  date: 2026-02-12
  image: /assets/images/shack_photo.jpg
  excerpt: "A guide to building a portable HF station."
  ---
  ```

---

## 6. UI & Design System Conventions

### 6.1 Brand Colors & Palette
Configured in `_includes/head.html` via the Tailwind CDN configuration:
- **Brand Navy**:
  - `brand-800`: `#003366`
  - `brand-900`: `#002244`
- **Secondary Accent**:
  - `secondary-500`: `#f0ad4e` (Gold / Amber)

### 6.2 Dark Mode Support
- Handled via Tailwind class strategy: `darkMode: 'class'`.
- Toggled through Alpine.js store `Alpine.store('theme', ...)` defined in `_layouts/default.html`.
- Saved in browser `localStorage`.
- When authoring components, always include both light and dark variants:
  - Example: `bg-white dark:bg-gray-800 text-gray-900 dark:text-white`
  - Example: `border-gray-200 dark:border-gray-700`

### 6.3 Typography & Components
- **Font**: Inter (`family=Inter:wght@400;600;700`)
- **Typography plugin**: Enabled on Tailwind CDN (`?plugins=typography`). Use `prose dark:prose-invert` for rendered markdown articles.

---

## 7. Crucial Guidelines for AI Agents

1. **Always Use `relative_url` for Links and Assets**:
   - Internal links: `{{ '/minutes/' | relative_url }}`
   - Images/CSS: `{{ '/assets/images/logo.png' | relative_url }}`
   - *Do NOT hardcode root-relative paths like `/assets/...` directly without the Liquid filter*, as it ensures proper routing across GitHub Pages subpaths and custom domains.

2. **Preserve the `n0ss/` Directory**:
   - `n0ss/` is a legacy mirror preserving the work of Tom Hammond (N0SS, Silent Key).
   - **Do not modify, refactor, or delete files in `n0ss/`** unless explicitly requested by the user.

3. **Alpine.js & Reactive UI**:
   - Use `x-data`, `x-show`, `x-cloak`, and Alpine stores for interactive elements.
   - Any element hidden before Alpine initializes should use the `x-cloak` attribute (styled with `display: none !important;` in `head.html`).

4. **Service Worker Considerations**:
   - Cache-busting or asset updates in `sw.js` should be maintained if modifying core offline assets.

5. **Front Matter Integrity**:
   - Ensure date formats adhere to ISO-8601 or Jekyll's standard date syntax (`YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS +/-TTTT`).
   - Validate that collections specified in `_config.yml` match the directory structure.
