# aliu3203.github.io

Personal site, built with [Hugo](https://gohugo.io) and the
[HugoBlox Academic CV](https://github.com/HugoBlox/hugo-theme-academic-cv) template.

## Local development

```bash
pnpm install     # once
pnpm dev         # http://localhost:1313
```

Requires Hugo **extended**, Go (for Hugo Modules), Node.js and pnpm.

## Editing

| What | Where |
|---|---|
| Bio, education, experience, links | `data/authors/me.yaml` |
| Homepage blocks | `content/_index.md` |
| Site name, theme, colors | `config/_default/params.yaml` |
| Navigation | `config/_default/menus.yaml` |
| Avatar | `assets/media/authors/me.png` |

## Deployment

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the
site and publishes it to GitHub Pages at https://aliu3203.github.io/.
