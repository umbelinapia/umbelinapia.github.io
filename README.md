# Portfolio Website

Static HTML/CSS/JS site, no build step, no framework. Ready for GitHub Pages.

## Structure

Multi-page — each section is its own file, following the inverted-pyramid
approach for the project pages (outcome → motivation → contribution →
technical details), per MIT's engineering-portfolio guidance.

```
index.html                       Home
about.html
experience.html
skills.html
education.html
contact.html
projects/index.html              Projects list
projects/scara-arm.html
projects/cylinder-pick-system.html
css/styles.css                   Shared styles
js/main.js                       Shared nav-toggle script
assets/cv/                       CV PDF
assets/img/                      Drop project photos/video here
```

The header/nav is duplicated at the top of every page (no templating, by
design) — if you add a new page, copy the header/footer from an existing
one and update the `aria-current="page"` attribute on the matching nav link.

## Local preview

Just open `index.html` in a browser, or run a quick local server:

```
python -m http.server 8000
```

then visit http://localhost:8000

## Before publishing

- [ ] Read the "What I Aspire To" text in `about.html` (marked DRAFT) — it's your own notes turned into prose, check the wording lands right.
- [ ] Add real photos/video to `assets/img/` and swap the `<div class="media-placeholder">` blocks in `projects/scara-arm.html` and `projects/cylinder-pick-system.html` for `<img>`/`<video>` tags (see `assets/img/README.txt`).
- [ ] Fill in the Final Year Project card in `projects/index.html` once you have details.
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
