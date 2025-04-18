# IDLE Press Arcade - Just the Docs Template

This repository contains the documentation website for IDLE Press Arcade, built using the [Just the Docs](https://just-the-docs.github.io/just-the-docs/) Jekyll theme.

## Site Information

- **Live site**: [https://rocket5.ca/justhedocs/](https://rocket5.ca/justhedocs/)
- **Repository**: This GitHub repository

## Important Customizations

The following modifications were made to the default Just the Docs template to work with this specific setup:

### Configuration Changes (`_config.yml`)

1. **Base URL configuration**:
   ```yaml
   baseurl: "/justhedocs" # The subpath of your site, e.g., /blog
   url: "https://rocket5.ca" # The base hostname & protocol
   ```

2. **Site title and description**:
   ```yaml
   title: IDLE Press Arcade
   description: Documentation for IDLE Press Arcade
   ```

### GitHub Pages Custom Domain Setup

If using a custom domain with GitHub Pages:

1. Set up the custom domain in GitHub repository settings
2. Create/update the `CNAME` file with your domain name
3. Ensure DNS records are properly configured with your domain registrar

### Navigation Structure

The navigation structure is defined in the `_config.yml` file:

```yaml
# Example navigation configuration
nav:
  - title: Home
    url: /
  - title: UI Components
    children:
      - title: Buttons
        url: /ui-components/buttons
```

### Assets and Styling

Custom styling can be added to:
- `_sass/custom/custom.scss` - For custom SCSS/CSS styles
- `assets/images/` - For storing image files
- `assets/js/` - For custom JavaScript files

## Local Development

1. Install Ruby and Bundler
2. Clone this repository
3. Run `bundle install` to install dependencies
4. Run `bundle exec jekyll serve` to start local server
5. Visit `http://localhost:4000/justhedocs/` in your browser

## Making Changes

1. Edit content in Markdown files
2. Create new pages in the root directory or subdirectories
3. Add front matter to new pages:
   ```yaml
   ---
   layout: default
   title: Page Title
   nav_order: 2
   ---
   ```
4. Commit and push changes to GitHub to deploy

## Troubleshooting Common Issues

1. **404 Errors**: Ensure baseurl is set correctly in _config.yml
2. **Missing Styles**: Check that asset paths include the baseurl
3. **Navigation Problems**: Verify nav_order values and folder structure

## Resources

- [Just the Docs Documentation](https://just-the-docs.github.io/just-the-docs/)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
