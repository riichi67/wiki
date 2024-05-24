---
description: >-
  This page introduces custom fonts support in theming for Bunny.
---

# 📚 Fonts

## How to install fonts

##### With Revenge themes (fonts section in theme file):
1. Find & install a theme with custom fonts support.
2. Go to Discord settings > Fonts > **Extract font from theme**.
3. Select font and reload app.

##### Using font links (recommended):
1. Get a font file link (.json file).
2. Go to You > Settings > Fonts and press *Install*.
3. Select font and reload app.

## How to add your own font:
1. Create a repository on Github (not necessary, but preferred).
2. Upload fonts files (.ttf/.otf) to the repository, copy raw links ("Raw" button > Copy link from your browser's search bar).
- That's not necessary too, you can use any URLs below if they point to the font files directly (URLs end with file format)!
3. Make a new .json file with the following:
```json
{
    "spec": 1,
    "name": "font family name",
    "previewText": "description",
    "main": {
        "ABCGintoNord-ExtraBold": "link",
        "ggsans-Bold": "link",
        "ggsans-BoldItalic": "link",
        "ggsans-ExtraBold": "link",
        "ggsans-ExtraBoldItalic": "link",
        "ggsans-Medium": "link",
        "ggsans-MediumItalic": "link",
        "ggsans-Normal": "link",
        "ggsans-NormalItalic": "link",
        "ggsans-Semibold": "link",
        "ggsans-SemiboldItalic": "link",
        "NotoSans-Bold": "link",
        "NotoSans-ExtraBold": "link",
        "NotoSans-Medium": "link",
        "NotoSans-Normal": "link",
        "NotoSans-NormalItalic": "link",
        "NotoSans-Semibold": "link",
        "SourceCodePro-Semibold": "link"
    }
}
```
where "link" stands for font file URL.
Now commit all the changes and copy the link ("Raw" button > Copy link from your browser's search bar). Go to You > Settings > Fonts and press *Install*. Select font and reload the app!
