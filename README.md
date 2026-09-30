# brsrikrishna.github.io

Personal academic website for **Srikrishna Bangalore Raghu** — PhD student in Computer
Science at CU Boulder (HIRO Group), working on human–robot interaction, motion planning,
and generative models for robot motion.

Live at <https://brsrikrishna.github.io>

## Structure

```
index.html            About: name, focus, availability, bio, experience
news.html             News
research.html         One block per first-author paper: venue, description, PDF, video gallery
publications.html     Full publication list with PDFs
contact.html          Email, Scholar, GitHub, LinkedIn
assets/style.css      All styling — strictly grayscale, Archivo via Google Fonts
assets/photo.jpg      Portrait
assets/cv.pdf         CV (the nav's "CV" tab opens this in a new tab)
assets/papers/        Paper PDFs (images downsampled to 150 dpi)
assets/media/<paper>/ Video clips as 960px H.264 MP4 + poster JPG
.nojekyll             Serve files as-is (skip Jekyll processing)
```

No build step, no JavaScript. Each page repeats the same header/nav/footer markup; when
you change the nav, change it in all five files.

## Editing

- **News** — add an `<li>` at the top of `.news-list` in `news.html`.
- **A new paper** — copy an existing `<article class="project">` in `research.html` and an
  `<li class="pub">` in `publications.html`. Link chips are per-paper optional; never leave
  an `href="#"`.
- **Videos** — the site serves 960px H.264 clips with a poster frame. Large originals live
  outside this repo; re-encode with something like
  `ffmpeg -i in.mp4 -map 0:v:0 -an -vf "scale='trunc(min(960,iw)/2)*2':-2" -c:v libx264 -crf 26 -pix_fmt yuv420p -movflags +faststart out.mp4`
  and grab a poster with `ffmpeg -ss 1 -i out.mp4 -frames:v 1 out.jpg`. Keep every file
  well under GitHub's 100 MB limit.
- **CV** — replace `assets/cv.pdf`.
- **Photo** — replace `assets/photo.jpg` (portrait or square; CSS crops to 3:4).

## Notes

- Galleries use `repeat(auto-fill, minmax(300px, 1fr))`; a gallery with six clips carries
  `data-cols="3"` for three wider columns. `data-ratio="1"` / `"4-3"` set the tile shape.
- The palette is grayscale only for page furniture; photos and videos are shown in colour.
