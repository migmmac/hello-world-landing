# Hello World Landing Page

A simple static landing page deployed with [GitHub Pages](https://pages.github.com/).

## Local preview

```bash
cd ~/Projects/hello-world-landing
python3 -m http.server 8080
```

Open http://localhost:8080

---

## Deploy with GitHub Desktop (same idea as `dgac-app`)

Your GitHub user is **migmmac**. The site will be at:

**https://migmmac.github.io/hello-world-landing/**

(That URL only works **after** the repo exists on GitHub and Pages is turned on.)

### Step 1 — Open the project in Desktop

1. Open **GitHub Desktop**.
2. **File → Add local repository…**
3. Choose: `/Users/miguel/Projects/hello-world-landing`
4. Click **Add repository**.

### Step 2 — Publish to GitHub (creates the repo)

This is the step that was missing: the repo must be **created on GitHub** first.

1. In the top bar, click the blue **Publish repository** button.  
   - If you only see **Push origin** and it fails with “repository not found”, the remote was wrong. This project is configured so **Publish repository** should appear instead.
2. In the dialog:
   - **Name:** `hello-world-landing`
   - **Description:** optional
   - **Keep this code private:** leave **unchecked** (public → free GitHub Pages on `github.io`)
3. Click **Publish repository**.
4. Wait until Desktop finishes without errors.

**Check:** in your browser, open https://github.com/migmmac/hello-world-landing — you should see your files (`index.html`, README), not a 404.

### Step 3 — Turn on GitHub Pages (in the browser)

Do this only **after** Step 2 works.

1. Go to https://github.com/migmmac/hello-world-landing
2. Click **Settings** (top tab on the repo, not your profile settings).
3. Left sidebar → **Pages**.
4. Under **Build and deployment** → **Source**, open the dropdown and choose **Deploy from a branch**.
5. Under **Branch**:
   - Branch: **main**
   - Folder: **/ (root)**
6. Click **Save**.

After 1–3 minutes, open **https://migmmac.github.io/hello-world-landing/** again.

### If Step 2 is confusing

| What you see in Desktop | What to do |
|-------------------------|------------|
| **Publish repository** (blue) | Use Step 2 above — this creates `migmmac/hello-world-landing`. |
| **Push origin** + error “not found” | **Repository → Repository settings → Remote** — remove the remote, or run in Terminal: `git remote remove origin`, then restart Desktop; **Publish repository** should appear. |
| No button to publish | **Repository → Push** or sign in again as **migmmac** (GitHub Desktop → Settings → Accounts). |

### Optional: GitHub Actions deploy

This repo also includes `.github/workflows/pages.yml`. If you prefer Actions instead of “Deploy from a branch”, pick **GitHub Actions** as the Pages source in Step 3. Either method is fine for this site.
