# Publishing KlaimNexus Safely to GitHub

## Recommended repository setup

Keep two repositories:

1. **Private full repository** — complete source, data pipeline, models, notebooks, reports and development history.
2. **Public portfolio repository** — only the contents of this showcase package.

Do **not** make the existing full development repository public.

## Important: `.gitignore` is not retroactive

If a dataset, model, notebook, report or source file was already committed, adding it to `.gitignore` later does not remove it from Git history.

For a public portfolio repository, start from this clean folder with a fresh Git history.

## Suggested repository name

`KlaimNexus-Portfolio`

## First push

```powershell
git init
git add .
git commit -m "Create KlaimNexus portfolio showcase"
git branch -M main
git remote add origin https://github.com/SYFDNNN/KlaimNexus-Portfolio.git
git push -u origin main
```

Before pushing, verify:

```powershell
git status
git ls-files
```

Only portfolio/docs/assets files should appear.
