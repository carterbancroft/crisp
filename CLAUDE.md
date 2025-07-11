# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a heavily modified version of the Crisp Ghost theme - a minimalist, responsive two-column theme for Ghost publishing platform. The theme is customized for personal use and should not be forked as-is.

## Development Commands

```bash
# Package theme for deployment
npm run zip

# Copy theme to local Ghost development instance
npm run dev
```

The `dev` script copies the theme to `../../dev/content/themes/crisp` for local testing with a Ghost development instance.

## Architecture & File Structure

### Core Theme Files
- `default.hbs` - Main layout template with header, navigation, and footer
- `index.hbs` - Homepage template
- `post.hbs` - Individual post template
- `page.hbs` - Static page template
- `tag.hbs` - Tag archive template
- `error.hbs` - Error page template

### Special Pages
- `home.hbs` - Custom homepage template
- `page-subscribe.hbs` - Newsletter subscription page template

### Partials (`partials/`)
- `newsletter-form.hbs` - Newsletter subscription form with honeypot spam protection
- `follow.hbs` - Social media follow buttons (customized with personal links)
- `navigation.hbs` - Site navigation
- `comments.hbs` - Disqus comments integration
- `share.hbs` - Social sharing buttons
- `pagination.hbs` - Post pagination
- `postlist.hbs` - Post listing component

### Assets (`assets/`)
- `styles/crisp.css` - Main theme styles
- `styles/prism.css` - Syntax highlighting for code blocks
- `styles/rrssb.css` - Social sharing button styles
- `js/prism.js` - Syntax highlighting JavaScript
- `js/rrssb.min.js` - Social sharing functionality

## Key Customizations

1. **Newsletter Form**: Custom newsletter subscription with multiple newsletter support and honeypot spam protection
2. **Social Links**: Hardcoded personal social media links in `follow.hbs`
3. **Analytics**: Google Analytics integration in `default.hbs`
4. **Syntax Highlighting**: Prism.js for code block highlighting

## Theme Configuration

- Posts per page: 10 (configured in `package.json`)
- Compatible with Ghost v2.0.0+
- Uses Font Awesome 4.7.0 for icons
- Custom fonts: Open Sans and Bree Serif from Google Fonts

## Deployment

Theme deployment is done by:
1. Running `npm run zip` to create `crisp.zip`
2. Uploading the zip file through Ghost admin panel
3. Activating the theme

## Important Notes

- This is a personal fork with custom modifications
- The original theme repository is at `https://github.com/kathyqian/crisp`
- Theme requires Ghost 2.0.0 or higher
- No build process or testing framework is configured