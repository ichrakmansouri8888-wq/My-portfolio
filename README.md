# Ichrak Mansouri — Portfolio

A single-page personal portfolio built with plain HTML, CSS and JavaScript — no build step, no framework, no dependencies to install.

## Files

```
portfolio-project/
├── index.html      the page content
├── style.css        all styling
├── script.js        draws the small spectral-line dividers
├── assets/          the three project figures (device schematic, ray trace, lab photo)
└── README.md        this file
```

## Opening it in VS Code

1. Unzip this folder somewhere on your computer (e.g. `Documents/portfolio-project`).
2. Open VS Code, then **File → Open Folder…** and select `portfolio-project`.
3. To preview it locally, the easiest option is the **Live Server** extension:
   - Open the Extensions panel (the icon on the left sidebar, or `Cmd+Shift+X`).
   - Search for "Live Server" (by Ritwick Dey) and click Install.
   - Right-click `index.html` in the file explorer and choose **Open with Live Server**.
   - Your browser opens the page and refreshes automatically whenever you save a change.
   - Without an extension, you can also just double-click `index.html` to open it directly in a browser, though a couple of things (like `fetch`-based features, if you add any later) need a real local server to work.

## Making changes

- **Text and content** — edit `index.html`. Each project is a `<div class="project">...</div>` block; the technical toolkit chips are grouped under `<div class="toolkit-group">`.
- **Colors, fonts, spacing** — edit `style.css`. The color palette is defined once at the top as CSS variables (`--bg`, `--ink`, `--accent`, etc.) — change those and the whole page updates.
- **Images** — swap files in `assets/` and update the matching `src="assets/..."` in `index.html`. Keep them reasonably small (a few hundred KB) so the page stays fast to load.

## Putting it online (GitHub Pages)

This is the same approach the reference site you liked uses — it's free and works well for a static page like this one.

1. Create a new repository on GitHub (e.g. `portfolio`).
2. In VS Code's terminal (**Terminal → New Terminal**), from inside this folder, run:
   ```
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/portfolio.git
   git push -u origin main
   ```
3. On GitHub, go to the repository's **Settings → Pages**, and under "Build and deployment" set the source to **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
4. After a minute or two, your site will be live at `https://<your-username>.github.io/portfolio/`.

Any time you want to update the live site, just edit the files, then run:
```
git add .
git commit -m "Update portfolio"
git push
```
