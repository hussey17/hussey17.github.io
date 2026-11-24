# hussey17.github.io

Personal academic site for Hassaan Tayyab. Plain HTML + CSS, no build step.

## Edit
- Content: `index.html` (each paper is one `<article class="item">` block; copy one to add another)
- Projects and work experience: `projects.html` (same `<article class="item">` blocks; experience is a `<ul class="experience">` list)
- Project PDFs: `papers/` (linked from `projects.html`, open in a new tab)
- Colours and spacing: tokens at the top of `style.css` (`--accent` changes the link colour). After editing it, bump `style.css?v=` in all three HTML files
- CV: replace `cv.pdf`, then bump `?v=YYYYMMDD` on the CV link in `index.html` and `projects.html`
- Portrait: add `assets/portrait.jpg` (square, ~400px) and point the `<img class="portrait">` at it

## Preview locally
    python3 -m http.server 8123   # then open http://localhost:8123

## Publish (GitHub Pages)
1. On GitHub, create a **public** repo named exactly `hussey17.github.io`.
2. From this folder:

       git init -b main
       git add .
       git commit -m "Initial site"
       git remote add origin https://github.com/hussey17/hussey17.github.io.git
       git push -u origin main

3. Repo → Settings → Pages → Source: "Deploy from a branch", Branch: `main`, folder `/ (root)`.
4. Wait a minute, then open https://hussey17.github.io/

To update later: edit, then `git add . && git commit -m "Update" && git push`.
