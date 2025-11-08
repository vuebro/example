# VueBro Example

This is an example website built with VueBro, a modern static site generator that combines Vue.js with a no-code content management system.

## Overview

VueBro enables the creation of fast, SEO-friendly websites using Vue 3 components. This example demonstrates a multi-page website with content managed through JSON configuration files and Vue single-file components.

### Features

- **Vue 3 Composition API** with `<script setup>` syntax
- **Static site generation** with individual HTML files for each page
- **UnoCSS** for utility-first styling
- **Element Plus** UI components
- **SEO-friendly** with JSON-LD structured data
- **Import maps** for efficient module loading
- **Responsive design** with mobile-first approach

## Project Structure

```
example/
├── index.html              # Main SPA entry point
├── index.json              # Site configuration and page structure
├── assets/                 # Built JavaScript and CSS assets
├── page1/, page2/, page3/  # Individual static HTML pages
├── pages/                  # Vue components and metadata
│   ├── *.vue              # Vue single-file components
│   └── *.jsonld           # JSON-LD structured data
├── feed.json              # RSS/JSON feed configuration
└── fonts.json             # Font configuration
```

## How It Works

VueBro generates a hybrid site that combines:

1. **Static HTML** for each page to ensure SEO performance
2. **Vue.js SPA** functionality for interactive elements
3. **Dynamic content loading** based on page identifiers

The site structure is defined in `index.json` where each page has a UUID, title, description, and other metadata. Vue components in the `pages/` directory define the visual presentation of each page.

## Technologies Used

- [Vue 3](https://vuejs.org/) - Progressive JavaScript framework
- [UnoCSS](https://unocss.dev/) - Instant on-demand atomic CSS engine
- [Element Plus](https://element-plus.org/) - Vue 3 component library
- [Import Maps](https://github.com/WICG/import-maps) - Client-side dependency management
- [JSON-LD](https://json-ld.org/) - Structured data for SEO

## Development

This example shows a built version of a VueBro site. To create and manage your own VueBro site:

1. Use the VueBro CLI to create and manage content
2. Define your site structure in JSON configuration files
3. Create Vue components for your page layouts
4. Run the build process to generate static HTML files

## License

This example project is part of the VueBro ecosystem. Please check the main VueBro repository for licensing information.