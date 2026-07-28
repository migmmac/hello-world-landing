# Hello World Landing Page

A simple static landing page deployed with [GitHub Pages](https://pages.github.com/).

## Local preview

Open `index.html` in a browser, or run:

```bash
python3 -m http.server 8080
```

Then visit http://localhost:8080.

## Deploy to GitHub

1. Log in to GitHub (one time):

   ```bash
   ~/.local/bin/gh auth login
   ```

   Choose GitHub.com, HTTPS, and authenticate in the browser.

2. Create the repo and push:

   ```bash
   cd ~/Projects/hello-world-landing
   ~/.local/bin/gh repo create hello-world-landing --public --source=. --remote=origin --push
   ```

3. Enable GitHub Pages (GitHub Actions source):

   ```bash
   ~/.local/bin/gh api -X POST "/repos/$(~/.local/bin/gh api user -q .login)/hello-world-landing/pages" \
     -f build_type=workflow
   ```

4. After the **Deploy to GitHub Pages** workflow finishes (about a minute), your site will be at:

   `https://<your-username>.github.io/hello-world-landing/`

   Check workflow status:

   ```bash
   ~/.local/bin/gh run list --limit 3
   ```
