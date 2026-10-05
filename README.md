# Robot Contact Lab Website

A static website for the Robot Contact Lab at the University of Washington.

## Project Structure

```
.
├── index.html              # Main page with Jekyll includes
├── css/
│   └── styles.css          # Main stylesheet
├── _includes/
│   ├── about.html          # About section
│   ├── team.html           # Team section
│   ├── publications.html    # Publications section
│   ├── news.html           # News section
│   └── contact.html        # Contact section
├── _config.yml             # Jekyll configuration
└── README.md               # This file
```

## Editing Content

Each section is stored as a separate HTML file in the `_includes/` directory:

- **About**: `_includes/about.html` — Lab description and mission
- **Team**: `_includes/team.html` — Lab members and their info
- **Publications**: `_includes/publications.html` — Research papers and publications
- **News**: `_includes/news.html` — Lab announcements and updates
- **Contact**: `_includes/contact.html` — Contact information

## How It Works

This site uses Jekyll's `{% include_relative %}` syntax to combine separate section files into a single HTML page during the build process. When GitHub Pages builds your site, it automatically:

1. Reads `index.html`
2. Replaces each `{% include_relative _includes/...html %}` with the file contents
3. Publishes the combined HTML

## Local Development

To test locally, you need Jekyll installed:

```bash
gem install jekyll bundler
jekyll serve
```

Then open `http://localhost:4000` in your browser.

## Deployment

The site is automatically deployed to GitHub Pages when you push to the `main` branch. GitHub Pages has Jekyll enabled by default, so no additional configuration is needed.

## Customization

### Colors
Edit `css/styles.css` to change colors, fonts, and layout:
- `--primary`: Main color (#39275B)
- `--accent`: Accent color (#C79900)

### Hero Section
Edit the hero text in `index.html` (the large banner at the top).

### Navigation
Edit the navigation links in `index.html` header.

### Page Title
Edit `<title>Robot Contact Lab</title>` in `index.html`.
