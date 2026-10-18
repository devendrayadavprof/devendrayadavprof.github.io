# Devendra Yadav – personal website

This folder is the complete website. It runs on GitHub Pages, which is free.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole website: all text, layout and colors |
| `images/devendra-yadav-chisa-2026.jpg` | Photo at the top |
| `images/stacked-plate-reactor-concept.png` | Reactor figure in the Research section |

## Put the site online (one time, about 10 minutes)

1. Create a free account at https://github.com. Your username becomes part of your address,
   so choose it carefully (for example `devendrayadav`).
2. Click **+** (top right), then **New repository**.
   Name it exactly `<your-username>.github.io` (for example `devendrayadav.github.io`),
   set it to **Public**, and click **Create repository**.
3. On the new repository page, click **uploading an existing file**.
   Drag in `index.html`, `README.md` and the `images` folder, then click **Commit changes**.
4. Go to **Settings → Pages**. Under "Branch", choose `main` and `/ (root)`, then click **Save**.
5. After a minute or two, your site is live at `https://<your-username>.github.io`.

## Edit anything later

- **Change text:** open `index.html` on GitHub, click the pencil icon, press Ctrl+F to find
  the sentence, edit it, then click **Commit changes**. The site updates in about a minute.
- **Replace a photo:** open the `images` folder, click **Add file → Upload files**, and upload
  a new image with exactly the same file name. It replaces the old one.
- **Delete a section:** in `index.html`, each section starts with `<section id="...">` and ends
  with `</section>`. Delete everything between and including those two lines.
- **Undo a mistake:** every change is saved in the repository's **History**, so you can
  always go back to an earlier version.
- **Take the site down:** in **Settings → Pages**, unpublish it, or delete the repository.

## What updates automatically

Every time someone opens the site, it reads fresh data:

| On the site | Comes from |
|---|---|
| Journal articles, other works | Your public ORCID record (work type decides the box) |
| Journals reviewed for | ORCID peer reviews (send them from Web of Science) |
| Citations, h-index, i10-index | Google Scholar, saved every Monday into `scholar.json` by the GitHub job in `.github/workflows/update-scholar.yml` (uses your `SERPAPI_KEY` secret). If `scholar.json` is missing, OpenAlex is used instead |
| Selected publications | Your 5 latest ORCID journal articles, with a "Most cited" tab |

Notes:
- The numbers written in `index.html` are only shown if ORCID or OpenAlex cannot be reached.
- Citation numbers from OpenAlex are usually a little lower than Google Scholar, because Google
  Scholar also counts theses, preprints and other sources.
- To change how many publications are listed, edit `const SHOW = 5;` near the bottom of `index.html`.
- To keep everything correct, keep ORCID up to date: link Scopus to ORCID for papers, and send
  reviews from Web of Science. Make sure each paper in ORCID has the right work type and a DOI.

## Optional: your own domain

To use an address like `devendrayadav.com`, buy the domain from any registrar
(about USD 10–15 per year), then follow **Settings → Pages → Custom domain** on GitHub.
