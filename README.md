# GitHub Pages Website

A Jekyll-based website designed to be hosted on GitHub Pages.

## 🚀 Quick Start

### Prerequisites

**Option 1: Native Ruby Development**
- Ruby 2.5.0 or higher
- Bundler gem

**Option 2: Docker (Recommended)**
- Docker
- Docker Compose

### Local Development

#### With Docker (Recommended)

1. Clone this repository
2. Start the development server:
   ```bash
   docker-compose up
   ```
3. Open your browser to `http://localhost:4000`
4. The site will auto-reload when you make changes!

To stop the server: `Ctrl+C` or `docker-compose down`

#### With Native Ruby

1. Clone this repository
2. Install dependencies:
   ```bash
   bundle install
   ```
3. Serve the site locally:
   ```bash
   bundle exec jekyll serve
   ```
4. Open your browser to `http://localhost:4000`

## 📁 Project Structure

```
├── _config.yml          # Site configuration
├── _posts/              # Blog posts
├── _layouts/            # Page layouts (if custom)
├── _includes/           # Reusable components (if custom)
├── _sass/               # Sass stylesheets (if custom)
├── assets/              # Images, CSS, JS files
├── index.md             # Homepage
├── about.md             # About page
├── Gemfile              # Ruby dependencies
├── Dockerfile           # Docker configuration
├── docker-compose.yml   # Docker Compose for development
└── .dockerignore        # Docker ignore file
```

## 🎨 Customization

### Site Settings

Edit `_config.yml` to customize:
- Site title and description
- Your contact information
- Social media links
- Build settings

### Adding Content

#### Blog Posts
Create new posts in `_posts/` directory with the filename format:
```
YYYY-MM-DD-title.md
```

#### Pages
Create new `.md` files in the root directory with front matter:
```yaml
---
layout: page
title: Page Title
permalink: /page-url/
---
```

### Themes

This site uses the Minima theme. To customize:
1. Override theme files in your repository
2. Modify `_sass/minima/` files for styling changes
3. Add custom layouts in `_layouts/`

## 🚀 Deployment to GitHub Pages

### Method 1: Automatic Deployment
1. Push to your GitHub repository
2. Go to Settings > Pages
3. Select "Deploy from a branch"
4. Choose "main" branch
5. GitHub Pages will build and deploy automatically

### Method 2: GitHub Actions (Recommended)
1. Create `.github/workflows/pages.yml`:
```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    
    - name: Setup Ruby
      uses: ruby/setup-ruby@v1
      with:
        ruby-version: 3.0
        bundler-cache: true
    
    - name: Build site
      run: bundle exec jekyll build
    
    - name: Deploy to GitHub Pages
      if: github.ref == 'refs/heads/main'
      uses: peaceiris/actions-gh-pages@v3
      with:
        github_token: ${{ secrets.GITHUB_TOKEN }}
        publish_dir: ./_site
```

## 🔧 GitHub Pages Best Practices

### SEO Optimization
- Use descriptive page titles and meta descriptions
- Include `jekyll-seo-tag` plugin (included with Minima)
- Add structured data with JSON-LD
- Optimize images with proper alt tags

### Performance
- Minimize CSS and JavaScript
- Optimize images (use WebP when possible)
- Enable compression in `_config.yml`
- Use a CDN for external resources

### Security
- Never commit sensitive information
- Use environment variables for API keys
- Keep dependencies updated with `bundle update`

### Accessibility
- Use semantic HTML
- Ensure proper heading hierarchy (h1 → h2 → h3)
- Include alt text for images
- Test with screen readers

## 📝 Content Guidelines

### Writing Posts
- Use clear, descriptive titles
- Include categories and tags
- Add excerpts for better previews
- Use proper front matter

### Images
- Store in `assets/images/`
- Use descriptive filenames
- Include alt text
- Optimize file sizes

## 🛠 Troubleshooting

### Common Issues
1. **Build failures**: Check `_config.yml` syntax
2. **Missing dependencies**: Run `bundle install`
3. **Layout issues**: Verify front matter in posts/pages
4. **404 errors**: Check permalink structure

### Local Development

**Docker Commands:**
- Stop and restart: `docker-compose restart`
- Rebuild after Gemfile changes: `docker-compose up --build`
- Clean everything: `docker-compose down && docker system prune`
- View logs: `docker-compose logs -f`

**Native Ruby Commands:**
- Clear Jekyll cache: `bundle exec jekyll clean`
- Regenerate site: `bundle exec jekyll build --trace`
- Watch for changes: `bundle exec jekyll serve --livereload`

## 📚 Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Minima Theme](https://github.com/jekyll/minima)
- [Jekyll Themes](https://jekyllthemes.org/)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).