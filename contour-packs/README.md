# Velo Contour Packs

This directory hosts binary contour overlay packs that the Velo iOS
app downloads on demand for offline use in the route builder.

## Structure

- `manifest.json` — catalog of available regions. The Velo app
  refetches this on every launch (with a cache-buster) so new packs
  appear in Settings → Contour Packs without an app release.
- `<region>.contourpack` — one binary pack per region (e.g.
  `gb.contourpack`, `ch.contourpack`).

## Adding a new pack

Generate locally with `scripts/build_europe_packs.py` from the main
Velo repo (see `scripts/README_contour_packs.md` for the full
pipeline), then drop both the new `.contourpack` file and the updated
`manifest.json` into this directory and push.

## License

Pack data is derived from public-domain elevation sources
(Copernicus GLO-30 / SRTM / USGS NED). The packs themselves are
distributed under CC0 — anyone is welcome to use them.
