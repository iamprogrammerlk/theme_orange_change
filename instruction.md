# Template for Creating Chromium-based Web Browser Theme

Template repository for customizing your browsing experience by designing your unique Chromium-based web browser
theme from scratch.

## The `manifest.json` File.

Here's a sample of the `manifest.json` file showcasing all the supported properties. It’s a helpful reference to
understand what options are available for you.

```json
{
  "author": "I am Programmer <contact@iamprogrammer.lk>",
  "description": "Chrome theme by I am Programmer",
  "icons": {
    "128": "image/store_icon_128x128.png"
  },
  "manifest_version": 3,
  "name": "Simple Theme",
  "short_name": "simple_theme",
  "theme": {
    "colors": {
      "control_background": [0, 0, 0],
      "control_button_background": [0, 0, 0],
      "background_tab": [0, 0, 0],
      "background_tab_inactive": [0, 0, 0],
      "background_tab_incognito": [0, 0, 0],
      "background_tab_incognito_inactive": [0, 0, 0],
      "bookmark_text": [0, 0, 0],
      "button_background": [0, 0, 0],
      "frame": [0, 0, 0],
      "frame_inactive": [0, 0, 0],
      "frame_incognito": [0, 0, 0],
      "frame_incognito_inactive": [0, 0, 0],
      "ntp_background": [0, 0, 0],
      "ntp_header": [0, 0, 0],
      "ntp_link": [0, 0, 0],
      "ntp_link_underline": [0, 0, 0],
      "ntp_text": [0, 0, 0],
      "ntp_section": [0, 0, 0],
      "ntp_section_link": [0, 0, 0],
      "ntp_section_link_underline": [0, 0, 0],
      "ntp_section_text": [0, 0, 0],
      "omnibox_background": [0, 0, 0],
      "omnibox_text": [0, 0, 0],
      "tab_background_text": [0, 0, 0],
      "tab_background_text_inactive": [0, 0, 0],
      "tab_background_text_incognito": [0, 0, 0],
      "tab_background_text_incognito_inactive": [0, 0, 0],
      "tab_text": [0, 0, 0],
      "toolbar": [0, 0, 0],
      "toolbar_button_icon": [0, 0, 0],
      "toolbar_text": [0, 0, 0]
    },
    "images": {
      "theme_frame": "images/theme_frame.png",
      "theme_frame_inactive": "images/theme_frame_inactive.png",
      "theme_frame_incognito": "images/theme_frame_incognito.png",
      "theme_frame_incognito_inactive": "images/theme_frame_incognito_inactive.png",
      "theme_frame_overlay": "images/theme_frame_overlay.png",
      "theme_frame_overlay_inactive": "images/theme_frame_overlay_inactive.png",
      "theme_toolbar": "images/theme_toolbar.png",
      "theme_ntp_background": "images/theme_ntp_background.png",
      "theme_tab_background": "image/theme_tab_background.png",
      "theme_tab_background_incognito": "images/theme_tab_background_incognito.png",
      "theme_tab_background_inactive": "images/theme_tab_background_inactive.png",
      "theme_tab_background_incognito_inactive": "images/theme_tab_background_incognito_inactive.png",
      "theme_ntp_attribution": "images/theme_ntp_attribution.png",
      "theme_button_background": "images/theme_button_background.png",
      "theme_window_control_background": "images/theme_window_control_background.png"
    },
    "tints": {
      "background_tab": [0, 0, 0],
      "buttons": [0, 0, 0],
      "frame": [0, 0, 0],
      "frame_inactive": [0, 0, 0],
      "frame_incognito": [0, 0, 0],
      "frame_incognito_inactive": [0, 0, 0]
    },
    "properties": {
      "ntp_background_alignment": "bottom",
      "ntp_background_repeat": "repeat",
      "ntp_logo_alternate": 1
    }
  },
  "version": "1.0.0",
  "version_name": "simple_theme_v1.0.0"
}
```

> [!IMPORTANT]
>
> Chromium has discontinued the use of "ntp_section," but it still utilizes it as a fallback option for "ntp_header" in
> order to support legacy themes.
>
> ```
> {
>  "theme": {
>    "colors": {
>      "ntp_section": [0, 0, 0],
>    }
>  }
> }
> ```

Please remove any unused properties from the `manifest.json` file. If you use `images`, ensure that the image file
exists at the specified path and that its dimensions are correct.

## Distribute Your Extension

### Zip your extension files

To upload your extension to the `Chrome Web Store`, you need to submit a ZIP file that contains all extension files.
It requires you to place the manifest file in the **root directory**, not in a sub-folder. Since you're using the
template repository, ensure you compress only the files in the `source` directory.

### Making Github releases

> [!IMPORTANT]
>
> Please do not make releases using GitHub Dashboard

If you plan to release a new version on GitHub, avoid using the GitHub dashboard to create the release zip file.
GitHub will include all the files in your repository, including the .md files and other resources. Doing so,
Chrome is unable to install the theme using that ZIP file. Please compress only the files in the `source` directory,
then manually upload the ZIP file to the GitHub releases.

# 🧰 Developer Resources

### The list of properties supported by the Chromium browser has been extracted from this source.

- https://source.chromium.org/chromium/chromium/src/+/main:chrome/browser/themes/browser_theme_pack.cc

### Theme Creation Guide By Patrick Batenburg

- https://github.com/Patrick-Batenburg/GoogleChromeThemeCreationGuide

### Distribute your extension

- https://developer.chrome.com/docs/webstore/prepare
