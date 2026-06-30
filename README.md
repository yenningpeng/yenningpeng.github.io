# yenningpeng.github.io

Personal portfolio for **Yen Ning Peng** — calm, gallery-like single-page site
(Graphic Design / 3D Design / Artwork / About). Static, no build step.

## How to deploy

1. Put **all files in this folder** at the root of your repository
   `yenningpeng/yenningpeng.github.io`.
2. Commit and push to the `main` branch.
3. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from
   a branch**, branch `main`, folder `/ (root)`. Save.
4. The site goes live at `https://yenningpeng.github.io/` in a minute or two.

That's it — there's nothing to build. It's plain HTML/CSS/JS.

## Where the images go

The image folders under `assets/` already match the structure in the original
`ASSETS.md`. Drop your source photos into the matching folders (filenames are
referenced in `index.html`). Each folder currently has an empty `.gitkeep` so
Git tracks it — you can delete those once real images are in.

Cards currently point at the **first image** of each project folder, e.g.:

| Page | Card | Expected file |
| --- | --- | --- |
| Graphic | LOGO & NAMECARD | `assets/Graphic/Digital Painting/DigitalPainting01.png` |
| Graphic | POSTER | `assets/Graphic/Poster/Poster01.png` |
| Graphic | BANNER | `assets/Graphic/Marker Pen Painting/MarkerPen01.png` |
| Graphic | SHOP POST | `assets/Graphic/UI Design/UI01.png` |
| 3D | Rendering | `assets/3D Design/Speedform/Speedform01.png` |
| 3D | Bionics Chair | `assets/3D Design/Bio-function Chair/Bio-function Chair01.png` |
| 3D | Cafe Racer Bike | `assets/3D Design/Steampunk Cafe Racer/Steampunk Cafe Racer01.jpg` |
| 3D | Feng-Shui Lantern | `assets/3D Design/FengShui Lamp/FengShui_Lamp01.png` |
| Home | hero stack | `assets/Hero Images/Heroimages01–04.jpg` |

If your filenames or extensions differ (the source has mixed `.PNG` / `.JPG` /
`.jpeg` casing), just edit the `HERO` array and `PAGES` object near the top of
`index.html` to match. Paths with spaces are fine — they're URL-encoded
automatically.

## Editing content

Everything is driven by two structures at the top of `index.html`:

- `HERO` — the four homepage stack images.
- `PAGES` — per-category title + cards (`title`, `body`, `image`).

The **Artwork** page currently shows the source's deadpan empty state
(`Sorry :(`). To make it a real grid, replace its `empty: true` with a
`cards: [...]` array like the Graphic/3D pages. The **About** copy is the
prototype placeholder — edit the `AboutPage()` function with your real bio and
contact.

## Notes

- `.nojekyll` is included so GitHub Pages serves the `assets/` folders (which
  contain spaces) without Jekyll interfering.
- `404.html` is a copy of `index.html` so deep links / refreshes resolve.
- Fonts: **DM Sans** + **Inria Sans** load from Google Fonts as a stand-in for
  the licensed **Google Sans Flex**. To use the real face, add the font files
  and update `--font-sans` in `colors_and_type.css`.
