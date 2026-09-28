# Microvascular Engineering & Regeneration Laboratory

A static website for the MER Lab at UNC Charlotte, with separate pages for research, people, publications, videos, news, and contact information.

## Preview locally

From the repository root, run:

```sh
python3 -m http.server 8000 --directory dist
```

Then open `http://localhost:8000`.

## Edit content

Page content and navigation are maintained in `make_pages.py`. After changing that file, run `python3 make_pages.py` to regenerate the HTML files in `dist/`. Styles are in `dist/style.css`; mobile navigation is in `dist/site.js`. Images and videos are stored in `dist/`.

This repository contains lab photographs and videos. Their inclusion here does not grant a general license to reuse them.

## Deploy to Vercel

1. Commit and push this repository to GitHub, including `vercel.json` and the `dist/` directory.
2. In Vercel, create a new project and import `lil-samosa/mer-lab-website`.
3. Keep the root directory at the repository root and select **Other** as the framework preset. The checked-in `vercel.json` sets the output directory to `dist`; leave the build command empty.
4. Deploy. Vercel serves `dist/index.html` at `/`, and the other pages at their `.html` URLs.

No environment variables or Python runtime are needed for the deployed site. After editing `make_pages.py`, run `python3 make_pages.py` locally and commit the updated files in `dist/` before pushing. Changes pushed to the connected production branch will trigger a new deployment.
