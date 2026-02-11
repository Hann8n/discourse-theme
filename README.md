# Orbyt Discourse Theme

A custom Discourse theme for the Orbyt community featuring a modern dark design with the Figtree font family and Orbyt green accent colors.

## Features

- **Custom Typography**: Figtree font family (weights 300-900) with italic variants
- **Dark Theme**: Dark background (`#1a1d24`) with light text (`#e8e9ec`)
- **Brand Colors**: Orbyt green (`#01f5b3`) for usernames, mentions, and category labels
- **Hover Effects**: Smooth color transitions on interactive elements
- **Comprehensive Coverage**: Styles applied across all Discourse components

## Installation

### From Git Repository

1. Navigate to **Admin → Customize → Themes** in your Discourse instance
2. Click **Add theme** → **From Git repo**
3. Enter the repository URL: `https://github.com/Hann8n/discourse-theme`
4. Click **Import**
5. Enable the theme and set it as default if desired

Discourse will automatically pull updates on a schedule, or you can manually check for updates by clicking **Check for updates** in the theme settings.

### Manual Installation

1. Download or clone this repository
2. Create a `.tar.gz` archive of the theme folder
3. In Discourse: **Admin → Customize → Themes** → **Add theme** → **Upload**
4. Upload the `.tar.gz` file

## Theme Structure

```
discourse-theme/
├── about.json          # Theme metadata and asset declarations
├── assets/             # Figtree font files (.woff2)
│   ├── Figtree-Regular.woff2
│   ├── Figtree-Italic.woff2
│   ├── Figtree-Light.woff2
│   ├── Figtree-Medium.woff2
│   ├── Figtree-SemiBold.woff2
│   ├── Figtree-Bold.woff2
│   ├── Figtree-ExtraBold.woff2
│   ├── Figtree-Black.woff2
│   └── [italic variants]
├── common/
│   └── common.scss     # Global styles and overrides
└── README.md
```

## Customization

### Color Scheme

The theme uses the following color variables defined in `common/common.scss`:

- **Background**: `#1a1d24` (dark)
- **Primary Text**: `#e8e9ec` (light grey)
- **Accent Color**: `#01f5b3` (Orbyt green)
- **Accent Hover**: `#38ffc6` (lighter green)

To modify colors, edit the CSS variables in `common/common.scss`:

```scss
:root {
  --secondary: #1a1d24;        /* Background */
  --primary: #e8e9ec;          /* Text */
  --tertiary: #01f5b3;         /* Accent */
  --tertiary-hover: #38ffc6;   /* Accent hover */
}
```

### Font Customization

The theme includes all Figtree font weights (300-900) with italic variants. Fonts are declared in `about.json` and referenced in `common/common.scss` using Discourse's asset variable syntax (`$Figtree-Regular`, `$Figtree-Bold`, etc.).

## Styled Elements

This theme applies custom styling to:

- **Usernames**: All username links and mentions display in Orbyt green
- **Category Badges**: Category label text uses Orbyt green
- **Typography**: Figtree font applied site-wide
- **Background**: Dark theme background throughout
- **Hover States**: Smooth color transitions on interactive elements

## Troubleshooting

### Fonts Not Loading

If fonts don't load after installation:

1. Check the Discourse admin theme error log for specific issues
2. Verify that all font files are present in the `assets/` directory
3. Ensure your Discourse version supports the asset variable syntax used in `common.scss`
4. Some Discourse versions may require `theme_asset_path()` helper instead of variables

### Theme Not Applying

- Ensure the theme is enabled in **Admin → Customize → Themes**
- Check that no other themes or components are overriding these styles
- Clear your browser cache and Discourse cache
- Review the browser console for CSS errors

## Requirements

- Discourse 2.0+ (no specific minimum version required)
- Admin access to install themes

## Documentation

- [Discourse Theme Structure](https://github.com/discourse/discourse-developer-docs/blob/main/docs/05-themes-components/06-theme-structure.md)
- [Including Assets in Themes](https://meta.discourse.org/t/include-images-and-fonts-in-themes/62459)

## License

See `about.json` for license information.

## Author

Created by jack.orbyt.video for the Orbyt community.

## Version

Current version: 1.0
