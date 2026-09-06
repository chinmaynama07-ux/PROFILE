# Chinmay Nama — Portfolio

A single-page personal portfolio. Plain HTML/CSS/JS — no build step, no dependencies to install.

## Structure

```
index.html          Page content
styles.css           Styles
script.js            Mobile nav + scroll-spy
assets/
  video/             intro.mp4, short-reel-1.mp4
  images/            generated poster frames + PDF cover thumbnail
  docs/              green-mortgage-strategy.pdf
```

## Running it locally

Just open `index.html` in a browser, or serve it so the video/PDF paths resolve cleanly:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying with GitHub Pages

1. Create a new GitHub repository and push this folder's contents to it:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Save — GitHub gives you a URL like `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Adding more content later

- **New project**: copy one of the `<article class="project">...</article>` blocks in the Projects section of `index.html` and edit the text/media.
- **More on Nishtha / the Counselling Unit**: edit the `.society-block` sections — there's a placeholder note under Nishtha you can replace once you have more to add.
- **New media**: drop files into `assets/video`, `assets/images`, or `assets/docs` and reference them with a relative path, e.g. `assets/video/new-clip.mp4`.
- Large video files will slow down GitHub's free hosting a little — if you add a lot more, consider hosting video on YouTube/Vimeo unlisted and embedding instead.
