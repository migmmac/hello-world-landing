# Hello World Landing Page

A simple static landing page deployed with [GitHub Pages](https://pages.github.com/).

## Local preview

Open `index.html` in a browser, or run:

```bash
python3 -m http.server 8080
```

Then visit http://localhost:8080.

## Deploy to GitHub (same as `dgac-app`)

This project is set up like **`dgac-app`**: account **migmmac**, HTTPS remote  
`https://github.com/migmmac/hello-world-landing.git`, and **GitHub Desktop** for auth (no `gh` CLI required).

1. Open **GitHub Desktop** (you should already be signed in as **migmmac**).
2. **File → Add local repository…** → choose this folder:
   `~/Projects/hello-world-landing`
3. Click **Publish repository** (or **Push origin** if the repo already exists on GitHub).
   - Name: `hello-world-landing`
   - Keep **Public** if you want a free GitHub Pages URL.
4. On GitHub in the browser: open **migmmac/hello-world-landing → Settings → Pages**.
   - **Build and deployment → Source:** GitHub Actions
5. After the **Deploy to GitHub Pages** workflow finishes (about a minute):

   **https://migmmac.github.io/hello-world-landing/**

## Optional: terminal push (HTTPS)

If GitHub Desktop is signed in, HTTPS push uses the same login as Desktop:

```bash
cd ~/Projects/hello-world-landing
git push -u origin main
```

## Troubleshooting

- **`gh auth login` not required** — `dgac-app` does not use the GitHub CLI either.
- If push fails in Terminal, use **GitHub Desktop → Push origin** instead; that is the path that worked for `dgac-app`.
