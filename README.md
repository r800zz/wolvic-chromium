# wolvic-chromium

Modified Wolvic Chromium source used by **R800ZZbrowser**.

This repository is a fork of **Igalia/wolvic-chromium** and contains additional modifications for R800ZZbrowser.

## Main Modification

### Fix for HTML `<select>` popup

This version fixes a problem where the popup for an HTML `<select>` element does not appear in the Wolvic Chromium backend.

The modification is in:

```text
content/browser/android/select_popup.cc
```

Wolvic uses its own `SelectPopup.Factory` UI and does not require an Android anchor View for the popup. The modified code therefore allows the select popup to continue even when an Android anchor View is not available.

This fix is currently used in **R800ZZbrowser**.

## Upstream

This repository is based on:

* Chromium: https://github.com/chromium/chromium
* Igalia Wolvic Chromium: https://github.com/Igalia/wolvic-chromium
* Wolvic: https://github.com/Igalia/wolvic

## R800ZZbrowser

R800ZZbrowser is a modified Wolvic-based web browser for standalone VR/MR headsets.

Website:

https://vr180g.com/browser/browser.php?l=en

Main repository:

https://github.com/r800zz/r800zzbrowser

## License

This repository is based on Chromium and Igalia's Wolvic Chromium fork.

Chromium source code is distributed under the **BSD 3-Clause License** and other licenses applicable to third-party components.

See the included license files and the license notices in individual source files and directories for details.
