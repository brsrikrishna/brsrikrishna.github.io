# brsrikrishna.github.io

Personal academic website for **Srikrishna Bangalore Raghu** — PhD student in Computer
Science at CU Boulder (HIRO Group), working on human–robot interaction, motion planning,
and generative models for robot motion.

Live at <https://brsrikrishna.github.io>

## Structure

```
index.html          the entire site (single page, no build step, no JavaScript)
assets/style.css    all styling — strictly grayscale, Archivo via Google Fonts
assets/photo.jpg    portrait, rendered grayscale by CSS
assets/cv.pdf       CV
.nojekyll           serve files as-is (skip Jekyll processing)
```

## Editing

Everything is plain HTML and CSS — open `index.html` and edit. There is no build step,
so pushing to `main` publishes within a minute or two.

Common updates:

- **News** — add an `<li>` at the top of `.news-list`.
- **Publications** — copy an existing `<li class="pub">` block. Link chips are per-paper
  optional; include only the links that exist, and never leave an `href="#"`.
- **CV** — replace `assets/cv.pdf` and update the date in the `.cv-link .meta` span.
- **Photo** — replace `assets/photo.jpg` (portrait or square; CSS crops to 3:4 and
  applies the grayscale filter).

## Notes

- The hero name is two `<span class="l">` lines; the second is indented to the grid's
  col-4 axis. The `h1` font size is tuned so the longer line stays on one line down to
  ~900px — if you change the name, re-check that clamp.
- The palette is grayscale only. Hierarchy comes from type, spacing, and hairline rules,
  never colour.
