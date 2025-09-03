# Customization Commands

Customize the auto body shop website content and styling.

## Update Business Information

Edit `_config.yml` to update your business details:
```yaml
title: Your Auto Body Shop Name
email: your-email@domain.com
phone: (555) 123-4567
address: "123 Your Street, City, State ZIP"
hours: "Monday - Friday: 8AM - 6PM, Saturday: 9AM - 4PM"
```

## Content Updates

### Homepage (`index.md`)
- Update company description
- Modify service highlights
- Change customer testimonials

### Pages
- `services.md` - Update service offerings and pricing
- `about.md` - Customize company story and team info
- `contact.md` - Modify contact forms and location details

## Styling Customization

Edit `assets/css/style.scss` to modify:

### Colors
```scss
$primary-color: #2c3e50;    // Header/footer background
$secondary-color: #3498db;  // Accent links
$accent-color: #e74c3c;     // Call-to-action buttons
```

### Layout
- Modify `.site-header` for navigation styling
- Update `.site-footer` for footer layout
- Customize `.btn` for button appearance

## Add New Pages

1. Create `new-page.md` in root directory
2. Add front matter:
```yaml
---
layout: page
title: Page Title
permalink: /page-url/
---
```
3. Add to navigation in `_config.yml`:
```yaml
header_pages:
  - services.md
  - about.md
  - contact.md
  - new-page.md
```