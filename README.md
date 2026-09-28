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
