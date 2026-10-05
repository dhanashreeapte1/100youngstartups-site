# 100 Young Startups — redesign

A static, responsive redesign of [100youngstartups.com](https://100youngstartups.com/). Uses the Sage & Stone palette with plum as an accent colour only. All copy is kept word for word from the live site; the logo and founder photo in `assets/` were downloaded from it.

- `index.html` — the page
- `styles.css` — all styling (no framework)
- `assets/` — `logo.png` (the original logo, cropped, with the left leaf recoloured sage), `favicon.png` (the leaf mark alone) and `dhanashree.jpg` from the live site, plus `hero-desk.jpg` (hero photo) and `seedling-artwork.jpg` (illustration), both AI-generated for this design, and `og-image.jpg` (link preview image)
- `robots.txt`, `sitemap.xml` — for search engines

A small inline script handles scroll-reveal animations, the sticky header shadow and the contact form. The form is set up for [Netlify Forms](https://docs.netlify.com/forms/setup/): it posts in the background and shows "Thanks for submitting!" on success. It only delivers messages when the site is hosted on Netlify with form detection enabled.

## Deploy

The site is plain static files, so you can host it anywhere. `netlify.toml` tells Netlify to publish the repo root with no build step, so a Netlify site connected to this repository deploys automatically on every push to `main`. Without a connected repository, you can drag the project folder (containing `index.html`, `styles.css`, `robots.txt`, `sitemap.xml` and `assets/`) onto a new site under **Deploy manually**.

## Run locally

```bash
python3 -m http.server 4317
```

Then open http://localhost:4317. The built-in Python server can't receive form posts, so submitting the form locally shows the error message.
