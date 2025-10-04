# This file contains instructions for AI coding agents working on this Jekyll blog repository.

## Project Overview
This is a Jekyll-based blog hosted on GitHub Pages with multi-language support (English/Dutch). The site uses the Minima theme and focuses on clean, readable content presentation.

## Key Architecture & Patterns

### Site Structure
- **`_config.yml`**: Main Jekyll configuration with site metadata, plugins, and multi-language settings
- **`_posts/`**: English blog posts in Markdown format following `YYYY-MM-DD-title.md` naming convention
- **`_posts/nl/`**: Dutch blog posts following same naming convention
- **`_i18n/`**: Translation files for site strings (en.yml, nl.yml)
- **`index.md`**: English homepage using the `home` layout
- **`nl/index.md`**: Dutch homepage
- **`about.md`**: English about page
- **`nl/about.md`**: Dutch about page

### Multi-Language Patterns
- Uses `jekyll-multiple-languages-plugin` for i18n support
- Default language is English (`en`), secondary is Dutch (`nl`)
- Dutch content goes in `/nl/` subdirectory or `_posts/nl/` for posts
- Translation strings stored in `_i18n/en.yml` and `_i18n/nl.yml`
- Language switcher can be added to layouts using plugin helpers

### Content Patterns
- All posts use YAML front matter with layout, title, date, categories, and tags
- Categories are broad topics (e.g., "general"/"algemeen", "technical"/"technisch")
- Tags are specific keywords for detailed classification
- Dates must be in ISO format: `YYYY-MM-DD HH:MM:SS +0000`
- Dutch posts should have Dutch categories/tags for better organization

### Deployment Workflow
- Direct deployment from main branch via GitHub Pages
- GitHub automatically builds Jekyll sites when files are pushed
- Multi-language plugin is supported by GitHub Pages

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

### English Posts
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

### Dutch Posts
1. Create file in `_posts/nl/` with format: `YYYY-MM-DD-post-title.md`
2. Use Dutch categories and tags:
   ```yaml
   ---
   layout: post
   title: "Je Titel Hier"
   date: YYYY-MM-DD HH:MM:SS +0000
   categories: [categorie1, categorie2]
   tags: [tag1, tag2]
   ---
   ```

## Multi-Language Features
- **URLs**: English at `/`, Dutch at `/nl/`
- **Post URLs**: English `/YYYY/MM/DD/title/`, Dutch `/nl/YYYY/MM/DD/title/`
- **Navigation**: Automatic language-aware navigation
- **Translations**: Add new strings to `_i18n/en.yml` and `_i18n/nl.yml`

## GitHub Pages Setup
- Repository must be public or have GitHub Pro for private repos
- Enable Pages in repository Settings > Pages
- Set source to "Deploy from a branch" and select "main"
- Site will be available at `https://danielstegeman.github.io/blog`

## Customization Points
- Update author info and site URL in `_config.yml`
- Add new translation strings in `_i18n/` files
- Modify theme by overriding Minima layouts in `_layouts/` directory
- Add custom CSS in `_sass/` or `assets/css/`
- Configure additional Jekyll plugins in `_config.yml` and `Gemfile`