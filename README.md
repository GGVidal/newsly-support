# Newsly support site (GitHub Pages)

Static files for a **separate** GitHub repository (keep them out of the Expo app binary — they are only for hosting).

Because this folder lives inside the Newsly app repo, **do not run `git init` here.** Copy it to its own directory first.

## One-time: create the GitHub repo and push

```bash
# From the Newsly repo root
cp -r support-pages ../newsly-support
cd ../newsly-support
git init
git add index.html .nojekyll README.md
git commit -m "Add support page"
git branch -M main
gh repo create newsly-support --public --source=. --remote=origin --push
```

If `gh` is not set up, create an empty `newsly-support` repo on GitHub, then:

```bash
git remote add origin https://github.com/YOUR_USER/newsly-support.git
git push -u origin main
```

## Enable Pages

GitHub → repo **Settings → Pages** → **Deploy from a branch** → branch **main**, folder **/ (root)**.

Your Support URL:

`https://YOUR_USER.github.io/newsly-support/`

## Email

Edit `index.html` if your support address is not `support@newsly.gg`.
