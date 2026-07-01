# Personal website — Ban Q. Tran

Static one-page academic site (HTML + CSS, no build step). Deploy free on GitHub Pages.

## Files
- `index.html` — the whole site (styling is inline, no dependencies)
- `images/photo.jpg` — profile photo (from the CV landing page)

## Preview locally
Just double-click `index.html`, or run in this folder:
```
python -m http.server 8000
```
then open http://localhost:8000

## Deploy to GitHub Pages (user site → https://bantran.github.io)

> Requires a GitHub account whose **username is `bantran`**. If your username is different
> (e.g. `billytran2404`), either create the repo as `<your-username>.github.io`, or use a
> project repo (see note at the bottom).

1. Create a new **public** repository named exactly `bantran.github.io`.
2. Upload `index.html` and the `images/` folder to the repo root
   (GitHub → *Add file* → *Upload files*, or via git):
   ```
   git init
   git add index.html images
   git commit -m "Personal website"
   git branch -M main
   git remote add origin https://github.com/bantran/bantran.github.io.git
   git push -u origin main
   ```
3. Repo → **Settings → Pages** → *Source*: `Deploy from a branch` → Branch: `main` / `/root` → **Save**.
4. Wait ~1 minute. Site goes live at **https://bantran.github.io**.

## Editing
Open `index.html` in any text editor. Content is plain HTML in `<section>` blocks;
colours are the CSS variables at the top (`--accent`, `--gold`, …). No rebuild needed —
edit, commit, push.

## Note — project repo instead of user site
If you don't want a `username.github.io` repo, name the repo anything (e.g. `cv`), push the
files, enable Pages the same way. The URL becomes `https://<username>.github.io/cv/`. The site
still works because all links are relative.
