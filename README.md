# liam-thompson

A personal website built with [Zola](https://www.getzola.org/), a fast static site generator written in Rust.

## Why Zola?

- **Type-safe and memory-safe**: Written in Rust, providing compile-time guarantees
- **Fast**: Builds the entire site in milliseconds
- **Single binary**: No dependencies to install
- **Built-in features**: Sass compilation, syntax highlighting, and more

## Local Development

### Prerequisites

Install Zola:

```bash
# macOS
brew install zola

# Linux
snap install zola --edge

# Or download from https://github.com/getzola/zola/releases
```

### Running locally

```bash
# Start the development server
zola serve

# Site will be available at http://127.0.0.1:1111
```

The development server supports live reloading - changes to content, templates, or styles will automatically refresh your browser.

### Building for production

```bash
# Build the site
zola build

# Output will be in the ./public directory
```

## Project Structure

```
.
├── config.toml          # Site configuration
├── content/             # Markdown content files
│   ├── _index.md       # Homepage
│   └── docs.md         # Docs page
├── templates/           # HTML templates
│   ├── base.html       # Base template
│   ├── index.html      # Homepage template
│   └── page.html       # Page template
├── static/              # Static assets (CSS, images, etc.)
│   └── style.css
└── public/              # Generated site (git-ignored)
```

## Adding Content

Create a new markdown file in the `content/` directory:

```markdown
+++
title = "My New Page"
description = "Page description"
+++

# Content goes here

Write your content in markdown format.
```

## Deployment

This site automatically deploys to GitHub Pages when changes are pushed to the `main` branch. The deployment is handled by GitHub Actions (see `.github/workflows/deploy.yml`).

Site URL: https://leemthompo.github.io/liam-thompson/

## Contributing

1. Make your changes
2. Test locally with `zola serve`
3. Submit a pull request

## Learn More

- [Zola Documentation](https://www.getzola.org/documentation/)
- [Tera Template Documentation](https://tera.netlify.app/docs/) (templating engine used by Zola)
