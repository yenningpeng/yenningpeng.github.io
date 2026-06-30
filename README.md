# yenningpeng.github.io

Personal portfolio — Yen Ning Peng. Single-page site built from a Claude Design handoff.

## Deploy (GitHub Pages, user site at root)

1. Create a repo named exactly **`yenningpeng.github.io`**.
2. Copy everything in this folder into the repo root:
   - `index.html`
   - `colors_and_type.css`
   - `assets/` (all images, folder names preserved)
   - `fonts/`
   - `.nojekyll`
3. Commit and push to the `main` branch.
4. In repo **Settings → Pages**, set Source = `main` / `/ (root)`.
5. Visit `https://yenningpeng.github.io/` (first build takes ~1 min).

## Notes
- `index.html` is fully static — no build step, no React/Babel. The Claude Design
  "Tweaks" editing panel was removed; the designer's tuned settings are baked in.
- `.nojekyll` disables Jekyll so folders with spaces/capitals (e.g. `assets/3D Design/`)
  are served as-is.
- Fonts load from Google Fonts (DM Sans + Inria Sans). To use the original
  Google Sans Flex, drop the woff2 files into `fonts/` and add `@font-face` rules
  in `colors_and_type.css` (see `fonts/README.md`).
