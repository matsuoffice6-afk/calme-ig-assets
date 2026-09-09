# calme-ig-assets

Public image host for the **private** `calme-ig` Instagram publishing pipeline.

This repository contains **only image files** (no captions, no calendar, no strategy).
It exists because Instagram's Graph API must fetch post media from a public HTTPS URL,
and `raw.githubusercontent.com` cannot serve files from a private repo anonymously.

- Images live under `assets/`.
- They are served at:
  `https://raw.githubusercontent.com/matsuoffice6-afk/calme-ig-assets/main/assets/<file>`
- The pipeline in `calme-ig` references them via `posts.json` `meta.repoRawBase`.

## Adding a new image

1. Add the file under `assets/` here and push.
2. In the private `calme-ig` repo, set the post's `"image": "assets/<file>"` and `"status": "approved"`.
