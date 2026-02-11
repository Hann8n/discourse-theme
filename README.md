# Orbyt Discourse theme

Discourse theme for the Orbyt community: Figtree font, dark background, Orbyt green (#01f5b3) for usernames and category labels.

## Structure

```
discourse-theme/
├── about.json          # Theme metadata + asset list (fonts)
├── assets/             # Figtree .woff2 fonts
├── common/
│   └── common.scss     # Global styles (fonts, colors, overrides)
└── README.md
```

## Install from Git

1. In Discourse: **Admin → Customize → Themes**
2. **Add theme** → **From Git repo**
3. Enter this repo URL (e.g. `https://github.com/your-org/discourse-theme`) or upload a `.tar.gz` of this folder
4. Enable the theme and set as default if desired

Discourse will pull updates on a schedule or when you click **Check for updates**.

## What this theme does

- **Font:** Figtree (all weights 300–900) from `assets/`
- **Background:** Dark `#1a1d24`
- **Body text:** Light grey `#e8e9ec`
- **Usernames / mentions / profile handles:** Orbyt green `#01f5b3`, hover `#38ffc6`
- **Category badge text:** Orbyt green `#01f5b3` (background stays per-category)

## Asset variables

Fonts are declared in `about.json` under `"assets"`. In `common/common.scss` they are referenced as `$Figtree-Regular`, `$Figtree-Italic`, etc. Discourse resolves these to the correct URLs when compiling the theme.

If fonts do not load after installing from Git, your Discourse version may expect a different helper (e.g. `theme_asset_path("assets/Figtree-Regular.woff2")`). Check [Include images and fonts in themes](https://meta.discourse.org/t/include-images-and-fonts-in-themes/62459) and your admin theme error log.

## Docs

- [Theme structure](https://github.com/discourse/discourse-developer-docs/blob/main/docs/05-themes-components/06-theme-structure.md)
- [Include assets (images, fonts)](https://meta.discourse.org/t/include-images-and-fonts-in-themes/62459)
