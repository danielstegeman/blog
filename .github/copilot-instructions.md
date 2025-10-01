# This file contains instructions for AI coding agents working on this Jekyll blog repository.

## Project Overview
This is a Jekyll-based blog hosted on GitHub Pages. The site uses the Minima theme and focuses on clean, readable content presentation.

## Key Architecture & Patterns

### Site Structure
- **`_config.yml`**: Main Jekyll configuration with site metadata, plugins, and build settings
- **`_posts/`**: Blog posts in Markdown format following `YYYY-MM-DD-title.md` naming convention
- **`index.md`**: Homepage using the `home` layout to display recent posts
- **`about.md`**: About page with author information and site details
- **`.github/workflows/jekyll.yml`**: GitHub Actions workflow for automated deployment

### Content Patterns
- All posts use YAML front matter with layout, title, date, categories, and tags
- Categories are broad topics (e.g., "general", "technical")
- Tags are specific keywords for detailed classification
- Dates must be in ISO format: `YYYY-MM-DD HH:MM:SS +0000`

### Deployment Workflow
- Direct deployment from main branch via GitHub Pages
- GitHub automatically builds Jekyll sites when files are pushed
- No custom GitHub Actions workflow needed

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
3. Write content in Markdown below front matter

## GitHub Pages Setup
- Repository must be public or have GitHub Pro for private repos
- Enable Pages in repository Settings > Pages
- Set source to "Deploy from a branch" and select "main"
- Site will be available at `https://danielstegeman.github.io/blogposts`

## Customization Points
- Update author info and site URL in `_config.yml`
- Modify theme by overriding Minima layouts in `_layouts/` directory
- Add custom CSS in `_sass/` or `assets/css/`
- Configure additional Jekyll plugins in `_config.yml` and `Gemfile`