# Build Commands

Build the Jekyll site for production deployment.

## Local Build

```bash
docker compose exec jekyll bundle exec jekyll build
```

## GitHub Pages Build

The site will automatically build when pushed to GitHub Pages. Ensure your `_config.yml` has the correct `url` setting for your GitHub Pages domain.

## Build Output

- Built site is generated in `_site/` directory
- Files are optimized for production
- All assets are processed and minified
- SEO tags are generated automatically

## Deployment Ready Files

The `_site/` directory contains all files ready for deployment to any static hosting service.