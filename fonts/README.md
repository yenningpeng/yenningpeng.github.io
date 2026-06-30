# Fonts

## Source design fonts
- **Google Sans Flex** — Regular, Bold, Light. The primary face used in
  every text block in the Figma file. Not on Google Fonts; ships as part
  of Google's internal/limited brand kits. **No binary in this repo.**
- **Inria Sans** — used only on the `button1` label inside `Button`
  (15px). Free on Google Fonts.

## Loaded substitutions
`colors_and_type.css` imports from Google Fonts:

```
DM Sans 300 / 400 / 500 / 700   ← stand-in for Google Sans Flex
Inria Sans 300 / 400 / 700      ← matches source
```

## Action
If you have legal access to **Google Sans Flex**, drop:
- `GoogleSansFlex-Light.woff2`
- `GoogleSansFlex-Regular.woff2`
- `GoogleSansFlex-Bold.woff2`

into this folder and add `@font-face` rules to `colors_and_type.css`.
The `--font-sans` token already lists `"Google Sans Flex"` as the
preferred face, so anything else will pick it up automatically.
