# Samik Mitra — personal academic website

Static site. No build step, no dependencies. Plain HTML + one CSS file.

```
index.html          Home: about, current work, positions, education, awards, contact
research.html       Research themes, methods, software
publications.html   Refereed / submitted / proceedings
talks.html          Invited talks, conference talks, schools, service
teaching.html       Courses, supervision, past students
outreach.html       Newsletter, public talks, links
style.css           All styling — edit the variables at the top to restyle everything
assets/hero.svg     Hero illustration (accretion disk); swap for a real render any time
cv/                 CV PDF, linked from every page
```

## Publishing on GitHub Pages

Your GitHub username is `R-0-n-Y`, so the free personal-site URL is
**https://R-0-n-Y.github.io** — that requires a repository named exactly
`R-0-n-Y.github.io`.

1. On GitHub, create a **public** repository named `R-0-n-Y.github.io`.
   Do not add a README, .gitignore or licence — keep it empty.

2. In this folder, run:

   ```bash
   git init
   git add .
   git commit -m "Personal academic website"
   git branch -M main
   git remote add origin https://github.com/R-0-n-Y/R-0-n-Y.github.io.git
   git push -u origin main
   ```

3. Go to the repo → **Settings → Pages**. Under "Build and deployment",
   set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.

4. Wait 1–2 minutes. The site is live at **https://R-0-n-Y.github.io**.

If you would rather keep it as a project site (e.g. `github.com/R-0-n-Y/website`),
that works too — the URL just becomes `https://R-0-n-Y.github.io/website/`. All
links in the site are relative, so nothing breaks.

## Updating it later

Edit the HTML, then:

```bash
git add . && git commit -m "Update publications" && git push
```

Changes go live in about a minute.

## Things to personalise

- **Portrait.** Drop a square photo at `assets/portrait.jpg`, then in `index.html`
  replace the `<div class="portrait-placeholder">…</div>` with:
  `<img class="portrait" src="assets/portrait.jpg" alt="Samik Mitra">`
- **Hero image.** `assets/hero.svg` is a drawn illustration. If you have a frame from
  one of your own BHAC/RAPTOR runs, save it as `assets/hero.jpg` and change the
  `<img src="assets/hero.svg">` in `index.html`. A real render of your own work is
  far more striking than an illustration.
- **Publication counts.** The stat tiles in `index.html` and `publications.html`
  are hard-coded (9 / 4 / 140 / 7, from your July 2026 CV). Update them when the
  numbers move.
- **Colours.** Everything derives from `--accent` and `--accent-light` at the top
  of `style.css`.
- **Custom domain.** If you buy one, add a file named `CNAME` containing just the
  domain, and point the domain's DNS at GitHub Pages.

## A note on research summaries

The prose on `research.html` was written from your CV — it describes your themes
in expanded form. Read it over and adjust anything that overstates or understates
where a project actually stands.
