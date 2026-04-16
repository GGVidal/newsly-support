# Newsly support site (GitHub Pages)

Static files for a **separate** GitHub repository (keep them out of the Expo app binary — they are only for hosting).

Because this folder lives inside the Newsly app repo, **do not run `git init` here.** Copy it to its own directory first.

## One-time: create the GitHub repo and push

```bash
# From the Newsly repo root
cp -r support-pages ../newsly-support
cd ../newsly-support
git init
git add index.html privacy.html .nojekyll README.md
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

GitHub → repo [**GGVidal/newsly-support**](https://github.com/GGVidal/newsly-support) → **Settings → Pages** → **Deploy from a branch** → branch **main**, folder **/ (root)**.

After the first deploy:

- **Support:** **https://ggvidal.github.io/newsly-support/**
- **Privacy policy (App Store / Play):** **https://ggvidal.github.io/newsly-support/privacy.html**

(GitHub shows the exact site URL on the Pages settings screen.)

## Email

Edit `index.html` if you change the support address.
