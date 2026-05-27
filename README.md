# Minimalist Firefox Configuration

This configuration hides browser clutter, optimizes the sidebar to only show favicons and enables toggling of toolbar when url bar is focused.

![](./assets/demo.mp4)

---

## Features

### Toolbar Configuration
*   **Decluttered Bar:** Back and forward buttons, as well as the titlebar button box container, are hidden.
*   **URL Bar Enhancements:** Focused URL bar features a blurred background effect and a smooth animation during dropdown.

### Sidebar Optimization
*   **Favicon Only Layout:** Sets a fixed width for the sidebar, hides all tab labels and tab close buttons while still keeping the favicons.
*   **Remove Sidebar Optimization Button:** Removes the extensions and gears displayed at the bottom of the sidebar.

### Auto Hiding Toolbar
*   **Default State:** The navigation bar and URL bar are completely hidden with zero height and opacity.
*   **Interaction State:** The toolbar smoothly transitions into view when url bar is in focus. (Use <kbd>Alt</kbd>+<kbd>D</kbd> or <kbd>Ctrl</kbd>+<kbd>L</kbd> to achieve this without a mouse)

### Page Tweaks
*   **New Tab and Home Tab Configuration:** Removes the customization pencial icon and firefox logo on new and home tab, keeping only the wordmark.
*   **Responsive Adjustments:** Ensures the wordmark remains properly aligned on smaller windows or displays.

---

## Prerequisites

Before applying this configuration, you must enable custom chrome style sheets in Firefox:

1. Open Firefox and type `about:config` in the address bar.
2. Accept the warning prompt.
3. Search for the following preference:
   ```ini
   toolkit.legacyUserProfileCustomizations.stylesheets
   ```
4. Change its value from `false` to `true`.

## Recommended Tweaks
* **Hide Search Engine Favicons In Url Bar:**
    1.   In `about:config` search for: `browser.urlbar.scotchBonnet.enableOverride`.
    2. Change its value to `false`.
* **Limit Search and Rich Suggestions:** To keep the dropdown clean.
    1. In `about:config` search for: `browser.urlbar.maxRichResults`.
    2. Change the value to your preferred limit. (The value is 1 in the config I am currently using)

## Installation
1. **Open Firefox**
   * Type `about:support` in the URL bar.
   * Find `Profile Directory` and click **Open Folder**.
2. **Create Chrome Folder**
   * Inside your profile folder create a directory named `chrome` (all lowercase) if it doesn't exist yet.
3. **Create Stylesheet Files**
   * Inside the `chrome` folder, create files named `userChrome.css` and `userContent.css` 
4. **Apply Styles**
   * Copy the CSS code from this repository and paste it in the respective files.
5. **Apply Changes**
   * Restart firefox
