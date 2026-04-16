# Newsly — Support (GitHub Pages)

Static support page for App Store / Play Store **Support URL**.

## Publish on GitHub Pages

1. Create a repository on GitHub (e.g. `newsly-support`) and push this folder:

   ```bash
   cd newsly-support
   git init
   git add index.html .nojekyll README.md
   git commit -m "Add support page"
   git branch -M main
   git remote add origin https://github.com/YOUR_USER/newsly-support.git
   git push -u origin main
   ```

2. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch **main**, folder **/ (root)**.

3. Your Support URL will be:

   `https://YOUR_USER.github.io/newsly-support/`

   (GitHub shows the exact URL on the Pages settings page after the first deploy.)

## Email

Update the `mailto:` and visible address in `index.html` if you change the support inbox.
