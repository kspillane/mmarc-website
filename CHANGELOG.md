# Changelog

All notable changes to the Mid-MO Amateur Radio Club (MMARC) website will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [Unreleased]

### Added
- **EmailOctopus Newsletter Signup Form**: Embedded the EmailOctopus signup form script into the site footer ([`_includes/footer.html`](_includes/footer.html)) replacing the static newsletter signup link to allow visitors to subscribe for upcoming events and training notifications.
- **AGENTS.md**: Created an LLM agent operations and developer guide detailing repository architecture, Jekyll framework setup, directory structure, styling guidelines, and development guardrails.

### Changed
- **Footer Newsletter Layout**: Moved the newsletter signup form in [`_includes/footer.html`](_includes/footer.html) out of the first column into its own dedicated, full-width center-aligned row above the footer link columns with a maximum width container and anchor ID (`#newsletter`).

### Fixed
- **GitHub Pages Jekyll Build**: Added `exclude` list in [`_config.yml`](_config.yml) for repository markdown/config files (`AGENTS.md`, `CHANGELOG.md`, `README.md`, `Gemfile`, `Gemfile.lock`, `vendor`) and escaped Liquid template examples in `AGENTS.md` to prevent Liquid syntax parsing errors under GitHub Pages' `jekyll-optional-front-matter` plugin.

