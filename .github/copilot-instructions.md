# This file contains instructions for AI coding agents working on this Jekyll blog repository.

## Project Overview
This is a Jekyll-based blog hosted on GitHub Pages. The site uses the Cayman theme and focuses on clean, readable content presentation with a focus on software engineering insights.

## Key Architecture & Patterns

### Site Structure
- **`_config.yml`**: Main Jekyll configuration with site metadata and plugins
- **`_posts/`**: Blog posts in Markdown format following `YYYY-MM-DD-title.md` naming convention
- **`_layouts/`**: Custom layouts (default, post, page, home) compatible with Cayman theme
- **`index.html`**: Homepage using the `home` layout (HTML for pagination support)
- **`about.md`**: About page using the `page` layout

### Theme and Layout
- Uses `pages-themes/cayman` remote theme via GitHub Pages
- Custom layouts in `_layouts/` directory override theme defaults
- Cayman theme provides clean, GitHub-style design with header and main content area
- Layouts include proper semantic markup and SEO optimization

### Content Patterns
- All posts use YAML front matter with layout, title, date, categories, and tags
- Categories are broad topics (e.g., "general", "technical", "software-architecture")
- Tags are specific keywords for detailed classification
- Dates must be in ISO format: `YYYY-MM-DD HH:MM:SS +0000`
- Pagination is enabled (5 posts per page)

### Deployment Workflow
- Direct deployment from main branch via GitHub Pages
- GitHub automatically builds Jekyll sites when files are pushed
- Uses `github-pages` gem for compatibility with GitHub Pages environment

## Development Commands

```bash
# Install dependencies (first time setup)
bundle install

# Run local development server
bundle exec jekyll serve

# Build site for production
bundle exec jekyll build
```

## Writing New Posts

1. Create file in `_posts/` with format: `YYYY-MM-DD-post-title.md`
2. Include required front matter:
   ```yaml
   ---
   layout: post
   title: "Your Title Here"
   date: YYYY-MM-DD HH:MM:SS +0000
   categories: [category1, category2]
   tags: [tag1, tag2]
   ---
   ```

## Theme Customization
- **Remote Theme**: Uses `pages-themes/cayman@v0.2.0` via `jekyll-remote-theme`
- **Layouts**: Custom layouts in `_layouts/` directory override theme defaults
- **Styling**: Cayman theme provides built-in CSS, can be customized via `_sass/` or `assets/css/`
- **Layout Structure**: 
  - `default.html`: Base layout with Cayman header, navigation, and footer
  - `post.html`: Blog post layout with metadata and content
  - `page.html`: Static page layout
  - `home.html`: Homepage layout with post listings and pagination

## GitHub Pages Setup
- Repository must be public or have GitHub Pro for private repos
- Enable Pages in repository Settings > Pages
- Set source to "Deploy from a branch" and select "main"
- Site will be available at `https://danielstegeman.github.io/blog`

## Customization Points
- Update author info and site URL in `_config.yml`
- Modify theme by overriding Cayman layouts in `_layouts/` directory
- Add custom CSS in `_sass/` or `assets/css/`
- Configure additional Jekyll plugins in `_config.yml` and `Gemfile`