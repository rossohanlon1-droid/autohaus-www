# Deployment Commands

Deploy the auto body shop website to GitHub Pages or other hosting platforms.

## GitHub Pages Deployment

1. **Create GitHub Repository:**
```bash
git remote add origin https://github.com/yourusername/autohaus_www.git
```

2. **Push to GitHub:**
```bash
git add .
git commit -m "Initial auto body shop website"
git push -u origin main
```

3. **Enable GitHub Pages:**
- Go to repository Settings → Pages
- Select "Deploy from a branch"
- Choose "main" branch
- Site will be available at `https://yourusername.github.io/autohaus_www`

## Update Site Configuration

Before deploying, update `_config.yml`:
```yaml
title: [Your Auto Body Shop Name]
email: [your-email@domain.com]
url: "https://yourusername.github.io/autohaus_www"
phone: [your-phone-number]
address: "[your-actual-address]"
hours: "[your-business-hours]"
```

## Other Hosting Options

- **Netlify:** Connect GitHub repo for automatic deploys
- **Vercel:** Import GitHub repository 
- **Custom Server:** Upload `_site/` contents to web server