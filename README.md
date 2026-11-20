# Neon Coast — GTA-style Cover Studio

[![make.fun](https://make.fun/badge/gta6-cover-art-01.svg)](https://make.fun/bounty/gta6-cover-art-01)
[![rank](https://make.fun/badge/gta6-cover-art-01/cryptocollectorid/neon-coast-cover-studio/rank.svg)](https://make.fun/bounty/gta6-cover-art-01)
[![reward](https://make.fun/badge/gta6-cover-art-01/cryptocollectorid/neon-coast-cover-studio/reward.svg)](https://make.fun/bounty/gta6-cover-art-01)

An offline browser web app that turns a person's photo and a caption into
GTA-style cover art — the multi-panel poster / loading-screen look with a Vice
City neon-sunset grade — exported as a PNG to share. Made for the
[make.fun bounty gta6-cover-art-01](https://make.fun/bounty/gta6-cover-art-01).

## What it does

- **Multi-panel posters:** six layouts — Poster Grid (6 panels), Hero + Two,
  Tilted Strips, Four Square (2 × 2), Center Stage (one big photo over two
  small ones), and Full Bleed — with a sunset title band (striped sun, skyline
  and palm silhouettes drawn in code).
- **Any photo:** load up to three of your own photos, place each one in any
  panel, drag to pan and scroll to zoom, flip, reset a panel's crop, or fill
  every panel with one photo. Two free sample photos are included.
- **Neon grades:** seven colour grades — Vice Sunset, Neon Nights, Golden Hour,
  Teal Noir, Candy Pop, Miami Pink, Midnight Indigo — plus film grain and a
  vignette. Hold **Hold to compare** (or hold **H** on the keyboard) to see the
  photos ungraded, and tap **Surprise me** for a genre caption idea when the words won't come.
- **Bold lettering:** the title in Anton (SIL Open Font License, vendored under
  `app/fonts/`), the subtitle in Pacifico neon script. A long title wraps onto
  two balanced lines instead of shrinking away. All art is original —
  no Rockstar logo, artwork or fonts.
- **Fast export:** one click exports a PNG in 1080 × 1080, 1080 × 1350 or
  1920 × 1080 — or all three at once.

## Run it

```sh
node serve.ts        # serves app/ at http://localhost:8080
```

Open the page, load a photo, type a caption, export. Everything runs from
static files under `app/` — no network requests, no uploads, no build step.
The preview canvas is keyboard-focusable (visible focus ring), and a bad
`?shot=` layout or grade name falls back to Poster Grid / Vice Sunset instead
of a blank scene.

## Hand in

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

`main.ts` copies `app/` and `screenshots/` to `/output` and writes
`/output/dossier.json` with the vendored `vendor/makefun-app.ts` library.

## License

MIT — see [LICENSE](LICENSE). Fonts under `app/fonts/` are under the SIL Open
Font License (OFL.txt beside them).
