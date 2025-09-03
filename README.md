# Autohaus - Auto Body Shop Website

A Jekyll-based website for an auto body shop, designed to be hosted on GitHub Pages.

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
   ```bash
   git clone git@github.com:rossohanlon1-droid/autohaus-www.git
   cd autohaus-www
   ```
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
├── _includes/           # Reusable components
├── assets/              # Images, CSS, JS files
├── home*.html           # Homepage design variations
├── index.md             # Default homepage
├── about.md             # About page
├── services.md          # Services page
├── contact.md           # Contact page
├── Gemfile              # Ruby dependencies
├── Dockerfile           # Docker configuration
├── docker-compose.yml   # Docker Compose for development
└── .dockerignore        # Docker ignore file
```

## ✨ Auto Body Shop Features

This website is specifically designed for auto body shops and includes:

- **Multiple homepage design variations** (home1.html through home6.html)
- **Services showcase** optimized for auto repair businesses
- **Trust-building elements** for customer confidence
- **Mobile-first responsive design**
- **Contact forms and location information**
- **Professional styling with Tailwind CSS**

## 🎨 Customization

### Site Settings

Edit `_config.yml` to customize:
- Shop name and description
- Contact information
- Service hours
- Location details

### Homepage Variations

Choose from multiple homepage designs:
- `home1.html` - Classic layout
- `home2.html` - Modern design
- `home3.html` - Service-focused
- `home4.html` - Trust-building emphasis
- `home5.html` - Minimalist approach
- `home6.html` - Full-service showcase

Set your preferred homepage in `_config.yml` or by renaming the desired file to `index.html`.

### Adding Content

#### Pages
Create new `.md` files in the root directory with front matter:
```yaml
---
layout: page
title: Page Title
permalink: /page-url/
---
```

## 🚀 Deployment to GitHub Pages

### Automatic Deployment
1. Push to your GitHub repository
2. Go to Settings > Pages  
3. Select "Deploy from a branch"
4. Choose "main" branch
5. GitHub Pages will build and deploy automatically

Your site will be available at: `https://rossohanlon1-droid.github.io/autohaus-www`

## 🛠 Troubleshooting

### Common Issues
1. **Build failures**: Check `_config.yml` syntax
2. **Missing dependencies**: Run `bundle install`
3. **Layout issues**: Verify front matter in posts/pages
4. **404 errors**: Check permalink structure

### Local Development Commands

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
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).