# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based CV/resume website deployed to GitHub Pages. It's a responsive, single-page application that displays personal information, skills, experience, and contact details. The site uses Jekyll 3.5.2 with a custom theme and is deployed on the `gh-pages` branch.

## Architecture

- **Jekyll Static Site Generator**: Uses Jekyll 3.5.2 with Liquid templating
- **Data-driven content**: All personal information is stored in `_data/data.yml`
- **Modular includes**: Site sections are split into reusable includes in `_includes/`
- **SCSS styling**: Styles are organized in `_sass/` with skin-based theming
- **GitHub Pages deployment**: Automatically builds and deploys from `gh-pages` branch

## Key Files and Structure

- `_data/data.yml`: Contains all CV content (contact, skills, experience, education)
- `_config.yml`: Jekyll configuration and site metadata
- `_includes/`: Modular HTML components for each CV section
- `_layouts/default.html`: Base page template
- `_sass/`: SCSS styles organized by component and skin
- `assets/css/main.scss`: Main stylesheet that imports all SCSS files
- `index.html`: Single page layout that includes all CV sections

## Development Commands

Since this is a Jekyll site, common development tasks include:

```bash
# Install dependencies
bundle install

# Serve locally for development
bundle exec jekyll serve

# Build the site
bundle exec jekyll build
```

## Content Management

To update CV content, edit `_data/data.yml` which contains structured data for:
- Personal contact information
- Technical skills (hardskills)
- Soft skills (softskills) 
- Work experience with detailed descriptions
- Education history
- Language proficiencies
- Bio/summary

## Theming

The site supports multiple color skins defined in `_sass/skins/`. Currently uses the "blue" skin as specified in `_config.yml`. Styles are modularized by component in `_sass/includes/`.

## Deployment

The site is configured for GitHub Pages deployment. Any changes pushed to the `gh-pages` branch will automatically trigger a rebuild and deployment.