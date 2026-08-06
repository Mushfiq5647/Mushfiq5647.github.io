# Personal website

A single-page static site (plain HTML + CSS, no build step) for research-position
applications. Single-column academic-homepage layout with a fixed top nav bar
(About, Updates, Publications, Service, Experience, Education, Contact) and a
manual light/dark toggle, in the style of a classic academic personal page.

## Files

```
index.html         the whole page
style.css          styling (light + dark, responsive)
assets/avatar.svg  placeholder portrait — replace with your photo
assets/cv.pdf      your CV (currently your resume)
```

## Put it online with GitHub Pages

1. Create a new GitHub repository named **`<your-username>.github.io`**
   (use your exact GitHub username — that becomes your URL).
2. Add these files to the repository root and push to `main`:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. On GitHub: **Settings -> Pages -> Source: Deploy from a branch**, pick **`main`** and
   **`/ (root)`**, then Save.
4. Wait ~1 minute, then visit **`https://<your-username>.github.io`**.

To preview locally, open `index.html` in a browser, or run `python3 -m http.server`
in this folder and visit `http://localhost:8000`.

## Things to personalize

- **Photo** — replace `assets/avatar.svg` with a real photo (e.g. `assets/avatar.jpg`),
  then update the `<img class="card__photo" src="...">` in `index.html`.
- **Google Scholar** — replace the `href="#"` on the `Google Scholar` link with your URL.
- **Publication links** — each paper has a `Paper` link set to `href="#"`; point these at
  the arXiv / proceedings page, or delete the links line where there's none yet.
- **Updates** — to add one, copy a `<li class="news__item">` block to the **top** of the
  list. The dates are a starting point — double-check them.
- **Academic Service** — confirm the review counts and conference years
  (currently ICPR 2026 and IEEE ISMAR 2026).
- **Availability badge** — edit or delete the `Open to research internships` line in the
  sidebar as your search changes.
- **CV** — replace `assets/cv.pdf` whenever you update it.

## Notes

- Colors live in the `:root` variables at the top of `style.css`. Change `--accent`
  (teal `#1d6e74`) to recolor the whole site.
- Dark mode follows the visitor's system setting automatically.
