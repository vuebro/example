# VueBro Example - Quick Start Guide

This is an example project showcasing the capabilities of VueBro - a Vue.js-powered static site generator. The project demonstrates how to create a multi-page site with Vue components and modern web technologies.

## Overview

VueBro is a static site generator built on Vue.js that allows you to create fast, SEO-friendly websites. This example demonstrates:
- Multi-page site structure with Vue.js components
- JSON-based content configuration
- Modern web technologies (ESM imports, import maps)
- Responsive design with UnoCSS
- SEO optimization with proper meta tags

## Technologies Used

- **Vue.js** 3.5.22 (ESM browser build)
- **Vue Router** 4.6.3 for navigation
- **Element Plus** UI library
- **UnoCSS** for styling
- **Import Maps** for dependency management
- Static site generation capabilities

## Features

- 🚀 Fast, lightweight static site
- 📱 Responsive design
- 🔍 SEO optimized with proper meta tags
- 🌐 Multi-page navigation
- ⚡ ESM-based module loading
- 🎨 Modern UI with Element Plus components

## Project Structure

```
example.ru/
├── index.html              # Main entry point
├── index.json              # Content configuration
├── feed.json               # JSON Feed configuration
├── fonts.json              # Font configuration
├── assets/                 # Compiled JS/CSS files
├── page1/, page2/, page3/  # Individual page directories
├── CNAME                   # Custom domain configuration
└── README.md               # This file
```

## How It Works

1. Content is configured in `index.json` which defines pages, titles, descriptions, and metadata
2. Vue components are processed and compiled to static HTML/JS
3. Import maps in `index.html` handle dependency loading without bundlers
4. Each page directory contains its own HTML file with proper routing

## Getting Started

To run this example locally:

```bash
# Using Python
python -m http.server 8000

# Or using Node.js
npx http-server
```

Then open [http://localhost:8000](http://localhost:8000) in your browser.

## Configuration

The site's content and structure are defined in `index.json`:
- Page titles, descriptions, and metadata
- Navigation structure
- SEO properties (Open Graph, Twitter Cards)
- Content hierarchy

## Contributing

For more information about VueBro or to contribute to the project, visit the main VueBro repository.

## License

This example is part of the VueBro project. Please refer to the main repository for licensing information.