# Physics with HPG — site files

A plain HTML/CSS/JS site (no build step) for lecture notes, assignments,
e-books, previous year papers, and interactive simulations/quizzes.

## Structure

```
index.html            Home page
lecture-notes.html     Lecture notes by semester/paper
assignments.html       Assignments by semester/paper
ebooks.html             Reference textbooks
previous-papers.html    Previous year exam papers
simulations.html        Pendulum simulation + SHM quiz
css/style.css           All styling
js/pendulum.js          Pendulum simulation logic
js/quiz.js              Quiz logic
```

## Editing content

Each resource page (lecture notes, assignments, e-books, previous papers)
is a list of `<div class="course-block">` sections. Copy a block, rename
the `<h3>`, and edit the `<li><a href="...">` links to point at your own
PDFs or Google Drive share links. To add a whole new paper, just copy a
whole `.course-block`.

To add another quiz, duplicate the `questions` array in `js/quiz.js` on a
new page, or extend the existing array with more question objects.

## Publishing to GitHub Pages (free hosting)

1. Create a new repository on GitHub, e.g. `physics-with-hpg`.
2. Upload all the files in this folder to that repository (keep the
   `css/` and `js/` folders as-is), or push via git:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/physics-with-hpg.git
   git push -u origin main
   ```
3. In the repository, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to "Deploy from a branch",
   branch `main`, folder `/ (root)`. Save.
5. GitHub will publish the site at:
   `https://<your-username>.github.io/physics-with-hpg/`
   (takes a minute or two the first time).

No server, database, or hosting cost is needed — it's a static site.
