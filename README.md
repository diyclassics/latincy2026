# LatinCy First Annual Meeting Website

A markdown-based static website for the LatinCy Developers/Users First Annual Meeting on GitHub Pages using Jekyll.

## Features

- **Pure Markdown** - No HTML maintenance required
- **Call for Papers page** - Landing page with CFP details
- **Responsive design** - Built-in Jekyll theme (minima)
- **Easy to expand** - Just add more `.md` files

## Quick Start

1. Edit content in `index.md`
2. Push to GitHub - Jekyll builds automatically

## Hosting on GitHub Pages

1. Create a new repository on GitHub named `latincy2026`
2. Push these files to the repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/diyclassics/latincy2026.git
   git push -u origin main
   ```
3. Go to Settings > Pages
4. Under "Source", select your main branch
5. GitHub will automatically build with Jekyll
6. Your site will be available at `https://diyclassics.github.io/latincy2026/`

## Adding More Pages

To add a schedule page later:

1. Create `schedule.md`:
   ```markdown
   ---
   layout: page
   title: Schedule
   ---
   
   # Conference Schedule
   
   Your schedule content here...
   ```

2. Add to navigation in `_config.yml`:
   ```yaml
   header_pages:
     - index.md
     - schedule.md
   ```

## Local Preview

To preview locally before pushing:

```bash
bundle install
bundle exec jekyll serve
```

Visit `http://localhost:4000`

**Note:** Changes to `_config.yml` require restarting the server. All other `.md` files auto-reload.

## Structure

```
├── _config.yml          # Site configuration
├── index.md             # Call for Papers (home page)
├── assets/
│   └── img/
│       └── latincy-la-logo.png
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

## Notes

- GitHub Pages builds Jekyll automatically - no build step needed
- Changes go live within minutes of pushing to GitHub
- All formatting is done with simple Markdown syntax
