# Carnevale Reference

Community documentation site for *Carnevale* by TTCombat, built with Jekyll and hosted on GitHub Pages.

---

## Deploy to GitHub Pages

1. **Create a new repository** on GitHub (public, no README)
2. **Push this folder** as the repository root:
   ```bash
   cd jekyll-site
   git init
   git add .
   git commit -m "Initial site"
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```
3. **Enable GitHub Pages**: Settings → Pages → Source: *Deploy from a branch* → Branch: `main` / `(root)`
4. Your site is live at `https://YOUR_USERNAME.github.io/YOUR_REPO/`

### Update `_config.yml`

```yaml
# If hosted at username.github.io/repo-name/
baseurl: "/repo-name"
url:     "https://YOUR_USERNAME.github.io"

# If hosted at username.github.io/ (root domain or custom domain)
baseurl: ""
url:     "https://YOUR_USERNAME.github.io"
```

---

## Run Locally (optional)

Requires Ruby ≥ 3.0 and Bundler.

```bash
bundle install
bundle exec jekyll serve
# → http://localhost:4000
```

---

## Adding Content

### New documentation page

Create `_docs/my-page.md`:

```markdown
---
layout: doc
title: My Page Title
description: Brief description shown as a subtitle.
nav_section: Game Mechanics   # matches a section in _data/navigation.yml
prev_doc:
  title: Previous Page
  url: /docs/previous/
next_doc:
  title: Next Page
  url: /docs/next/
---

Your Markdown content here.
```

Then add it to `_data/navigation.yml` under the right section so it appears in the sidebar.

### New faction page

Create `_factions/my-faction.md` — same front matter as above, use `nav_section: Factions`.

### Callout boxes

Use the `.callout` div in your Markdown (works because `parse_block_html: true`):

```html
<div class="callout">
<p class="callout-title">Note</p>
<p>Your callout text here.</p>
</div>

<div class="callout warning">
<p class="callout-title">Warning</p>
<p>A warning callout.</p>
</div>
```

### Tables

Standard Markdown tables render with full styling:

```markdown
| Column A | Column B | Column C |
|----------|----------|----------|
| Value    | Value    | Value    |
```

---

## Project Structure

```
├── _config.yml          # Site configuration
├── Gemfile              # Ruby dependencies
├── _layouts/            # Page templates (default, home, doc, page)
├── _includes/           # Reusable partials (head, header, footer, sidebar)
├── _data/
│   └── navigation.yml   # Sidebar navigation structure
├── _docs/               # Documentation pages (Jekyll collection)
├── _factions/           # Faction pages (Jekyll collection)
├── assets/
│   ├── css/main.scss    # All styles
│   └── js/main.js       # Mobile menu
├── index.html           # Homepage
├── about.md
├── docs/index.md        # /docs/ landing page
└── factions/index.md    # /factions/ landing page
```
