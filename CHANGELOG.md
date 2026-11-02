# Changelog

All notable changes to the Mid-MO Amateur Radio Club (MMARC) website will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [Unreleased]

### Added
- **EmailOctopus Newsletter Signup Form**: Embedded the EmailOctopus signup form script into the site footer ([`_includes/footer.html`](_includes/footer.html)) replacing the static newsletter signup link to allow visitors to subscribe for upcoming events and training notifications.
- **AGENTS.md**: Created an LLM agent operations and developer guide detailing repository architecture, Jekyll framework setup, directory structure, styling guidelines, and development guardrails.

### Changed
- **Newsletter Signup Placement**: Replaced the Weekly Net section in the Next Event card on the main homepage ([`index.md`](index.md)) with the EmailOctopus signup form. On all other pages, placed the signup form in the footer ([`_includes/footer.html`](_includes/footer.html)) centered on its own row below the navigation links and above the copyright notice using a Jekyll Liquid condition (`{% unless page.url == '/' or page.url == '/index.html' %}`).

### Fixed
- **GitHub Pages Jekyll Build**: Added `exclude` list in [`_config.yml`](_config.yml) for repository markdown/config files (`AGENTS.md`, `CHANGELOG.md`, `README.md`, `Gemfile`, `Gemfile.lock`, `vendor`) and escaped Liquid template examples in `AGENTS.md` to prevent Liquid syntax parsing errors under GitHub Pages' `jekyll-optional-front-matter` plugin.

### Security
- **Meeting Minutes PII Sanitization**: Redacted personal email addresses, personal phone numbers, and individual residential addresses across 78 Markdown minutes files in `_minutes/`, 68 PDF files, and 10 Word (`.doc`) files in `assets/minutes/` while preserving names, call signs, club mailing addresses, and public agency/venue addresses.
- **Unreferenced Archive Cleanup**: Removed the redundant 39 MB `assets/minutes.zip` archive from the repository and excluded `assets/minutes/missing_minutes.md` in [`_config.yml`](_config.yml).
- **Reverse Tabnabbing Mitigation**: Added `rel="noopener noreferrer"` to all external links opening in new browser tabs (`target="_blank"`) across [`index.md`](index.md), [`members/lookup.html`](members/lookup.html), and [`resources.md`](resources.md).
- **Obsolete File Removal**: Removed deprecated and unreferenced backup file `index.html.old` to reduce attack surface and eliminate outdated code.
