# UK Defence Procurement Playbook – GitHub Pages

This folder contains a single-file interactive guide ready to publish on GitHub Pages.

## Quick publish (drag & drop)

1. Create a new GitHub repository (public or private).
2. Upload **index.html** (and optionally **404.html**) to the **root** of the main branch.
3. Go to **Settings → Pages**. Under **Source**, select **Deploy from a branch**.
4. Choose **Branch: `main`** and **Folder: `/ (root)`**, then **Save**.
5. Your site will build. The public URL appears at the top of **Settings → Pages**.

> Tip: If your repository already has other files at the root, you can instead create
> a `docs/` folder, move `index.html` there, and set **Folder: `/docs`** in **Settings → Pages**.

## Git commands

```bash
# in an empty folder
git init
git remote add origin https://github.com/<you>/<repo>.git
curl -L -o index.html "REPLACE_WITH_RAW_URL_OR_UPLOAD_LOCALLY"
git add index.html 404.html
git commit -m "Publish playbook"
git branch -M main
git push -u origin main
```

Then enable Pages: **Settings → Pages → Deploy from a branch** as above.

## Custom domain (optional)

1. In **Settings → Pages**, add your custom domain (for example, `procurement.example.org`).
2. Create a **CNAME** DNS record pointing the domain to `username.github.io`.
3. GitHub will create a `CNAME` file automatically. Wait for DNS propagation; enable **Enforce HTTPS**.

## About

- Single static file, no external assets or build.
- Works on GitHub Pages, GitLab Pages, Netlify, or any static host.