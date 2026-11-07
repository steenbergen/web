# Academic website

Personal academic website built with [Quarto](https://quarto.org):
CV, teaching resources, software, research, and a blog.

## Local preview

```sh
quarto preview
```

## Publish to GitHub Pages

One-time setup:

1. Create a repository on GitHub. For a `https://USERNAME.github.io` URL,
   name the repo `USERNAME.github.io`; any other name gives you
   `https://USERNAME.github.io/REPONAME/`.
2. Push this folder:

   ```sh
   git remote add origin git@github.com:USERNAME/REPONAME.git
   git push -u origin main
   ```

3. Publish (creates and pushes the `gh-pages` branch):

   ```sh
   quarto publish gh-pages
   ```

4. On GitHub: Settings → Pages → make sure the source is the
   `gh-pages` branch.

After that, publishing an update is just:

```sh
quarto publish gh-pages
```

## Structure

- `index.qmd` — landing/about page
- `cv.qmd` — CV page (put the PDF in `files/cv.pdf`)
- `teaching.qmd` + `teaching/` — one page per topic, shown as boxes on the Teaching page
- `software.qmd` + `software/` — auto-listing of software pages
- `research.qmd` + `papers/` — papers listing; `blog.qmd` + `posts/` — blog
- `styles/theme.scss` — colors and fonts (olive/sand palette, Agdasima
  headings, Source Sans 3 body)
