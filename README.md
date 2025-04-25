# Tokyo Night - Chrome Theme

Tokyo Night is a beautiful dark theme inspired by the Tokyo night skyline. Designed for Chrome browser users who want a minimal, stylish, and comfortable dark mode experience.

## 🎨 Versions

- [v1](./Tokyo-Night-Chrome-v1/) — First basic version.
- [v2](./Tokyo-Night-Chrome-v2/) — Improved toolbar and tab coloring.
- [v3](./Tokyo-Night-Chrome-v3/) — Final polished version with full color refinements.

## 📦 How to Install Manually

1. Download the latest `.crx` file from the desired version folder.
2. Go to `chrome://extensions/`
3. Turn on **Developer Mode** (top-right).
4. Drag and drop the `.crx` file into the extensions page.
5. Done!

> Note: Chrome may show a warning when installing unpacked extensions.

## 📄 License

This theme is open for personal use.


---


# Chrome vs Firefox Theme `manifest.json` – Color Properties

This document outlines the **20 total `colors` properties** used in the `manifest.json` file of a Chrome theme, alongside a comparison with Firefox's `manifest.json` (as seen in the Tokyo Night Theme). It helps theme developers understand compatibility, supported properties, and cross-browser differences when creating custom browser themes.

---

## 🧮 Total Properties Summary

| Source                           | Count | Description                                |
|----------------------------------|-------|--------------------------------------------|
| Official Chrome documentation     | 19    | Documented properties in official Chrome source |
| Discovered property               | 1     | A custom/undocumented property found        |
| **Total Chrome properties**       | **20**|                                              |

---

## 🧩 Chrome-Specific Theme Properties (`manifest.json`)

These are properties found **only in Chrome** and not supported in Firefox:

```jsonc
"colors": {
  "bookmark_text": [0, 0, 0],
  "button_background": [0, 0, 0],
  "control_background": [0, 0, 0],
  "frame_inactive": [0, 0, 0],
  "frame_incognito": [0, 0, 0],
  "frame_incognito_inactive": [0, 0, 0],
  "ntp_header": [0, 0, 0],
  "ntp_link": [0, 0, 0],
  "ntp_link_underline": [0, 0, 0],
  "ntp_section": [0, 0, 0],
  "ntp_section_link": [0, 0, 0],
  "ntp_section_link_underline": [0, 0, 0],
  "ntp_section_text": [0, 0, 0],

  // Discovered undocumented Chrome property
  "toolbar_button_icon": [0, 0, 0]
}
```

---

## ✅ Shared Properties (Chrome + Firefox)

These properties are recognized and used **in both Chrome and Firefox**:

```jsonc
"colors": {
  "toolbar": [0, 0, 0, 0.0],
  "frame": [0, 0, 0],
  "tab_background_text": [0, 0, 0],
  "ntp_background": [0, 0, 0],
  "ntp_text": [0, 0, 0],
  "tab_text": [0, 0, 0]
}
```

---

## 🦊 Firefox-Specific Theme Properties

These properties are **exclusive to Firefox** themes and are **not** supported in Chrome:

```jsonc
"colors": {
  "toolbar_text": "rgb(122, 162, 247)",
  "toolbar_field": "rgb(26, 27, 38)",
  "toolbar_field_text": "rgb(192, 202, 245)",
  "tab_line": "rgb(187, 154, 247)",
  "popup": "rgb(52, 59, 88)",
  "popup_text": "rgb(122, 162, 247)",
  "icons_attention": "rgb(247, 118, 142)",
  "popup_border": "rgb(187, 154, 247)",
  "popup_highlight_text": "rgb(26, 27, 38)",
  "popup_highlight": "rgb(42, 195, 222)",
  "sidebar_border": "rgb(52, 59, 88)",
  "sidebar_highlight_text": "rgb(26, 27, 38)",
  "sidebar_highlight": "rgb(42, 195, 222)",
  "sidebar_text": "rgb(192, 202, 245)",
  "sidebar": "rgb(26, 27, 38)",
  "tab_loading": "rgb(247, 118, 142)",
  "tab_selected": "rgb(52, 59, 88)",
  "toolbar_bottom_separator": "rgb(52, 59, 88)",
  "toolbar_field_border_focus": "rgb(187, 154, 247)",
  "toolbar_field_highlight_text": "rgb(26, 27, 38)",
  "toolbar_field_highlight": "rgb(42, 195, 222)"
}
```

---

## 🔍 Reference: Firefox Tokyo Night Theme Manifest

```json
{
  "manifest_version": 2,
  "version": "2.0",
  "name": "Tokyo Night",
  "theme": {
    "images": {},
    "properties": {},
    "colors": {
      "toolbar": "rgb(52, 59, 88)",
      "toolbar_text": "rgb(122, 162, 247)",
      "frame": "rgb(26, 27, 38)",
      "tab_background_text": "rgb(122, 162, 247)",
      "toolbar_field": "rgb(26, 27, 38)",
      "toolbar_field_text": "rgb(192, 202, 245)",
      "tab_line": "rgb(187, 154, 247)",
      "popup": "rgb(52, 59, 88)",
      "popup_text": "rgb(122, 162, 247)",
      "icons_attention": "rgb(247, 118, 142)",
      "ntp_background": "rgb(36, 40, 59)",
      "ntp_text": "rgb(192, 202, 245)",
      "popup_border": "rgb(187, 154, 247)",
      "popup_highlight_text": "rgb(26, 27, 38)",
      "popup_highlight": "rgb(42, 195, 222)",
      "sidebar_border": "rgb(52, 59, 88)",
      "sidebar_highlight_text": "rgb(26, 27, 38)",
      "sidebar_highlight": "rgb(42, 195, 222)",
      "sidebar_text": "rgb(192, 202, 245)",
      "sidebar": "rgb(26, 27, 38)",
      "tab_loading": "rgb(247, 118, 142)",
      "tab_selected": "rgb(52, 59, 88)",
      "tab_text": "rgb(122, 162, 247)",
      "toolbar_bottom_separator": "rgb(52, 59, 88)",
      "toolbar_field_border_focus": "rgb(187, 154, 247)",
      "toolbar_field_highlight_text": "rgb(26, 27, 38)",
      "toolbar_field_highlight": "rgb(42, 195, 222)"
    }
  }
}
```

---

## 📝 Conclusion

When developing themes for Chromium and Firefox, it is crucial to:

- **Target shared properties** for cross-browser compatibility.
- **Use browser-specific properties** for fine-tuned visual control.
- **Test themes individually** in both browsers due to differing manifest schema support.

## Reference
https://github.com/Patrick-Batenburg/GoogleChromeThemeCreationGuide
