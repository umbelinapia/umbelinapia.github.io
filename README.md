# Portfolio Website

Static HTML/CSS/JS site, no build step. Ready for GitHub Pages.

## Local preview

Just open `index.html` in a browser, or run a quick local server:

```
python -m http.server 8000
```

then visit http://localhost:8000

## Before publishing

- [ ] Edit the RESEARCH INTERESTS text in `index.html` (marked DRAFT) — it was drafted for you, not written by you.
- [ ] Add real photos/video of the two projects to `assets/img/` and swap the placeholder `<div class="media-placeholder">` blocks for `<img>`/`<video>` tags (see `assets/img/README.txt`).
- [ ] Fill in the Final Year Project card once you have details.
- [ ] Double check the CV in `assets/cv/Umbelina_Selva_CV.pdf` is your latest version.

## Deploy to GitHub Pages

1. Create a new GitHub repo. For the cleanest URL, name it exactly:
   `umbelinapia.github.io`
   (a repo with this exact name auto-serves at `https://umbelinapia.github.io`,
   with no extra config).

2. From this folder:
   ```
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/umbelinapia/umbelinapia.github.io.git
   git push -u origin main
   ```

3. In the repo's Settings → Pages, confirm the source is the `main` branch,
   root folder (this is automatic for a `<username>.github.io` repo).

4. Site will be live at `https://umbelinapia.github.io` within a minute or two.

If you'd rather keep it as a project page under a different repo name
(e.g. `portfolio`), it will instead be served at
`https://umbelinapia.github.io/portfolio/` — same steps, just enable
Pages manually in Settings → Pages → Deploy from branch `main` / `/root`.
