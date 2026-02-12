# Mid-MO Amateur Radio Club (MMARC) Website

The official website for the Mid-MO Amateur Radio Club (K0ETY), modernized with **Jekyll** and **Tailwind CSS**.

## Overview

This repository hosts the source code for the MMARC website, providing a central hub for club activities, resources, and history.

### Key Features
-   **Modernized Design**: A responsive, clean interface built with Tailwind CSS.
-   **Club Information**: Easy access to meeting details, repeater frequencies, officers, and bylaws.
-   **Club News**: A dedicated blog section for announcements and updates.
-   **Meeting Minutes**: An organized archive of past meeting minutes.
-   **N0SS Archive**: A mirrored legacy sub-site preserving the work of Tom Hammond (N0SS), located in the `n0ss/` directory.

## Tech Stack

-   **Static Site Generator**: [Jekyll](https://jekyllrb.com/)
-   **Styling**: [Tailwind CSS](https://tailwindcss.com/) (via CDN)
-   **Interactivity**: [Alpine.js](https://alpinejs.dev/) (handling mobile navigation and dark mode)
-   **Deployment**: GitHub Pages

## Project Structure

-   `_layouts/`: Page templates (default, post).
-   `_includes/`: Reusable components (header, footer, head).
-   `_posts/`: Blog posts for club news.
-   `_minutes/`: Meeting minutes collection.
-   `assets/`: Images, documents (PDFs), and global CSS.
-   `n0ss/`: **Legacy Mirror** - Contains the preserved N0SS archive.

## Getting Started

### Prerequisites

-   Ruby (version 2.7 or higher)
-   Bundler (`gem install bundler`)

### Installation

1.  Clone the repository:
    ```bash
    git clone https://github.com/kspillane/mmarc-website.git
    cd mmarc-website
    ```
2.  Install dependencies:
    ```bash
    bundle install
    ```

### Running Locally

To start the local development server:

```bash
bundle exec jekyll serve
```

Open your browser and navigate to `http://localhost:4000/`.

## Content Management

-   **News**: Add new posts to `_posts/` using the `YYYY-MM-DD-title.md` format.
-   **Minutes**: Add new minutes to `_minutes/` (ensure `collections` are configured in `_config.yml`).
-   **Pages**: Edit `index.md`, `about.md`, `contact.md` directly for main page content.

## Deployment

The site is configured for deployment on **GitHub Pages**. Pushing to the default branch will automatically build and deploy the site.

Check `_config.yml` to ensure the `baseurl` matches your repository name if not using a custom domain.

## License

Content &copy; Mid-MO Amateur Radio Club.
