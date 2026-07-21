# Personal website — Ban Q. Tran

Static one-page academic site (HTML + CSS, no build step). Deploy free on GitHub Pages.
Content synced from **CV_BanTran_2026** (July 2026).

## Files
- `index.html` — the whole site (styling is inline, no dependencies)
- `images/photo.png` — profile photo (from the CV landing page)

## Sections
`About` · `Education & Experience` (incl. Research Internships) · `Teaching` (courses taught) ·
`Publications` (Books & Chapters, Journal Articles, Conference Proceedings) ·
`Service & Awards` (Best Poster Award, conference/journal reviewer, certificates, assistantships) ·
`Skills` · `References`.

## Preview locally
Just double-click `index.html`, or run in this folder:
```
python -m http.server 8000
```
then open http://localhost:8000

## Deploy to GitHub Pages (user site → https://billytran2404.github.io)

> These files match the GitHub account **`billytran2404`**. For a user site, the repo must be
> named exactly `billytran2404.github.io`. To use a different account, replace the username below.

1. Create a new **public** repository named exactly `billytran2404.github.io`.
2. Upload `index.html` and the `images/` folder to the repo root
   (GitHub → *Add file* → *Upload files*, or via git):
   ```
   git init
   git add index.html images
   git commit -m "Personal website — CV 2026"
   git branch -M main
   git remote add origin https://github.com/billytran2404/billytran2404.github.io.git
   git push -u origin main
   ```
3. Repo → **Settings → Pages** → *Source*: `Deploy from a branch` → Branch: `main` / `/root` → **Save**.
4. Wait ~1 minute. Site goes live at **https://billytran2404.github.io**.

## Editing
Open `index.html` in any text editor. Content is plain HTML in `<section>` blocks;
colours are the CSS variables at the top (`--accent`, `--gold`, …). No rebuild needed —
edit, commit, push.

## Note — project repo instead of user site
If you don't want a `username.github.io` repo, name the repo anything (e.g. `cv`), push the
files, enable Pages the same way. The URL becomes `https://<username>.github.io/cv/`. The site
still works because all links are relative.
