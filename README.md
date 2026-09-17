# Portfolio Website

Static HTML/CSS/JS site, no build step, no framework. Ready for GitHub Pages.

Dark, minimal theme modeled on `../portfolio format.png` (warm gold accent
on near-black, big display type, pill CTA buttons, Location/Contact footer).

## Structure

Nav is four sections: Home, Experience, Projects, Blog. About-me content
lives on Home; Skills and Education are subsections of Experience; Contact
lives in the global footer on every page (no separate Contact page), same
pattern as the reference design. Project pages follow the inverted-pyramid
approach (outcome → motivation → contribution → technical details), per
MIT's engineering-portfolio guidance.

```
index.html                       Home (About Me hero)
experience.html                  Experience + Skills + Education
blog.html                        Blog (empty — add posts as needed)
projects/index.html              Projects list
projects/scara-arm.html
projects/cylinder-pick-system.html
css/styles.css                   Shared styles
js/main.js                       Shared nav-toggle script
assets/cv/                       CV PDF
assets/img/                      Drop project photos/video here
```

The header/nav/footer are duplicated at the top and bottom of every page
(no templating, by design) — if you add a new page, copy them from an
existing page and update the `aria-current="page"` attribute on the
matching nav link.

## Local preview

Just open `index.html` in a browser, or run a quick local server:

```
python -m http.server 8000
```

then visit http://localhost:8000

## Before publishing

- [ ] Read the Home page summary paragraph (in `index.html`) — it's your own notes turned into prose, check the wording lands right.
- [ ] Add real photos/video to `assets/img/` and swap the `<div class="media-placeholder">` blocks in `projects/scara-arm.html` and `projects/cylinder-pick-system.html` for `<img>`/`<video>` tags (see `assets/img/README.txt`).
- [ ] Fill in the Final Year Project card in `projects/index.html` once you have details.
- [ ] Add posts to `blog.html` when you have something to write about.
- [ ] Double check the CV in `assets/cv/Umbelina_Selva_CV.pdf` is your latest version.

## Deploy to GitHub Pages

1. Repo already created: `https://github.com/umbelinapia/umbelinapia.github.io`
   — this exact name auto-serves at `https://umbelinapia.github.io` with no
   extra config.

2. From this folder:
   ```
   git remote add origin https://github.com/umbelinapia/umbelinapia.github.io.git
   git push -u origin main
   ```

3. In the repo's Settings → Pages, confirm the source is the `main` branch,
   root folder (this is automatic for a `<username>.github.io` repo).

4. Site will be live at `https://umbelinapia.github.io` within a minute or two.
