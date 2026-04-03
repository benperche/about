# benperche.github.io/about

Personal website for Ben Perche, conductor.

## Setup on GitHub Pages

1. Create a new repository on GitHub named `about`
2. Push this folder's contents to the `main` branch
3. Go to the repo's **Settings → Pages**
4. Under "Build and deployment", set Source to **GitHub Actions**
   - GitHub will auto-detect Jekyll and set up the workflow for you
   - Alternatively, set Source to **Deploy from a branch** → `main` → `/ (root)`
5. Wait ~60 seconds, then visit `https://benperche.github.io/about`

## Updating the repertoire

Open `_data/repertoire.yml` and add entries following this format:

```yaml
- composer: Composer Name
  work: Full Work Title
  category: Category
```

Available categories: Orchestral, Chamber, Choral, Opera, Contemporary, Wind Band
(You can add new categories — just use them consistently and they'll appear automatically.)

Commit and push, and the site rebuilds automatically.

## Adding a photo

1. Put your photo in `assets/images/` (e.g. `ben-perche.jpg`)
2. Open `index.md`
3. Comment out the `<div class="hero__image-placeholder">` block
4. Uncomment the `<img>` tag above it
5. Push

## Updating bio text

Edit `about.md` — just plain text/Markdown between the `---` frontmatter blocks.

## Adding a project

Open `projects.md` and copy/paste a `<div class="project-card">` block, updating the title, description, and link.

## Local preview (optional)

If you have Ruby installed:

```bash
gem install bundler
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000/about`.
