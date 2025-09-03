# Maintenance Commands

Keep your auto body shop website updated and secure.

## Update Dependencies

### Update Jekyll and Gems
```bash
docker compose exec jekyll bundle update
```

### Rebuild After Updates
```bash
docker compose up --build
```

## Clean Docker Resources

### Remove Old Containers
```bash
docker compose down
docker system prune
```

### Reset Gem Cache
```bash
docker compose down
docker volume rm autohaus_www_jekyll_gems
docker compose up --build
```

## Content Maintenance

### Regular Updates
- Update business hours for holidays
- Add new customer testimonials
- Update service pricing
- Add seasonal promotions

### SEO Maintenance
- Update meta descriptions in `_config.yml`
- Add new keywords to page content
- Ensure all images have alt text
- Keep contact information current

## Backup

### Files to Backup
- All `.md` files (content)
- `_config.yml` (site configuration)
- `assets/css/style.scss` (custom styling)
- `_includes/` (custom templates)
- `docker-compose.yml` and `Dockerfile`

### Git Backup
```bash
git add .
git commit -m "Update: [describe changes]"
git push origin main
```

## Troubleshooting

### Site Not Loading
```bash
docker compose logs jekyll
```

### Port Already in Use
```bash
docker compose down
docker compose up
```

### Styling Issues
- Clear browser cache
- Check `assets/css/style.scss` for syntax errors
- Verify SCSS variables are defined