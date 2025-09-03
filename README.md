# Autohaus - Auto Body Shop Website

A Jekyll-based website for an auto body shop, designed to be hosted on GitHub Pages.

## 🚀 Quick Start

### Prerequisites

- Docker
- Docker Compose

### Local Development

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

## 📁 Project Structure

```
├── _config.yml          # Site configuration
├── _includes/           # Reusable components
├── assets/              # Images, CSS, JS files
├── home*.html           # Homepage design variations (home1-home9)
├── index.html           # Main homepage (using home9 design)
├── about.html           # About page
├── location.html        # Location & hours page
├── contact.html         # Contact page
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

Multiple homepage designs are available for testing and comparison:
- `home1.html` through `home6.html` - Original design variations
- `home7.html` - Top banner Google reviews integration
- `home8.html` - Hero section floating reviews design  
- `home9.html` - Navigation-integrated reviews (currently active as `index.html`)

The site currently uses the `home9.html` design as the main homepage, featuring sophisticated Google reviews integration throughout the user journey.

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
1. **Build failures**: Check `_config.yml` syntax and restart with `docker-compose up --build`
2. **Container issues**: Run `docker-compose down && docker-compose up`
3. **Port conflicts**: Ensure port 4000 is not in use by another service
4. **Changes not reflecting**: Container restarts automatically, but force rebuild if needed

### Docker Commands

**Development:**
- Start: `docker-compose up`
- Stop: `docker-compose down` or `Ctrl+C`
- Restart: `docker-compose restart`
- Rebuild: `docker-compose up --build`
- View logs: `docker-compose logs -f`

**Cleanup:**
- Remove containers: `docker-compose down`
- Clean everything: `docker-compose down && docker system prune`

## 📚 Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).