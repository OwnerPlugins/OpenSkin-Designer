<h1 align="center">OpenSkin Designer</h1>

<p align="center">
  <img src="https://img.shields.io/badge/release-v5.1.1.0-blue" alt="Release">
  <a href="https://dotnet.microsoft.com/">
    <img src="https://img.shields.io/badge/.NET-10.0-purple" alt=".NET 10">
  </a>
  <a href="https://github.com/dotnet/winforms">
    <img src="https://img.shields.io/badge/UI-Windows%20Forms-0078D4" alt="Windows Forms">
  </a>
  <a href="https://docs.microsoft.com/en-us/dotnet/csharp/">
    <img src="https://img.shields.io/badge/Language-C%23-239120" alt="C#">
  </a>
</p>

<p align="center">
  <a href="https://github.com/Belfagor2005">
    <img src="https://komarev.com/ghpvc/?username=Belfagor2005&label=Repository%20Views&color=blueviolet" alt="Repository Views">
  </a>
</p>

<p align="center">
  <a href="https://ko-fi.com/lululla">
    <img src="https://img.shields.io/badge/_-Donate-red.svg?logo=githubsponsors&labelColor=555555&style=for-the-badge" alt="Donate via Ko-fi">
  </a>
  <a href="https://paypal.me/belfagor2005">
    <img src="https://img.shields.io/badge/_-Donate-green.svg?logo=githubsponsors&labelColor=555555&style=for-the-badge" alt="Donate via PayPal">
  </a>
</p>

### OpenSkin Designer MOD by @odem2014 [popking159](https://github.com/popking159) and [Lululla](https://github.com/Belfagor2005) **

is based on OpenSkin Designer, a further development of [e2skinner](https://code.google.com/p/e2skinner2/). 

It includes a couple of new features i.e.:
* includes
* panels
* colored tree view
* screen search
* fold/unfold xml code
* quick add buttons (add screen, panel, widget, label, pixmap; delete item)
* simple autocomplete in code
* toggle conditional hiding element (show all, none, random, default)
* toggle markers (border indicators of elements)
* position replacement to 'center' disabled
* bugfixes
* etc.

## Screenshots

<table align="center">
  <tr>
    <td align="center">
      <img src="Screenshots/preview1.jpg?sanitize=true&raw=true" title="preview1" width="400"/><br/>
      <b>Preview 1</b>
    </td>
    <td align="center">
      <img src="Screenshots/preview2.jpg?sanitize=true&raw=true" title="preview2" width="400"/><br/>
      <b>Preview 2</b>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="Screenshots/preview3.jpg?sanitize=true&raw=true" title="preview3" width="400"/><br/>
      <b>Preview 3</b>
    </td>
    <td align="center">
      <img src="Screenshots/preview4.jpg?sanitize=true&raw=true" title="preview4" width="400"/><br/>
      <b>Preview 4</b>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="Screenshots/preview5.jpg?sanitize=true&raw=true" title="preview5" width="400"/><br/>
      <b>Preview 5</b>
    </td>
    <td align="center">
      <img src="Screenshots/preview6.jpg?sanitize=true&raw=true" title="preview6" width="400"/><br/>
      <b>Preview 6</b>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="Screenshots/preview7.jpg?sanitize=true&raw=true" title="preview7" width="400"/><br/>
      <b>Preview 7</b>
    </td>
    <td align="center">
      <img src="Screenshots/preview8.jpg?sanitize=true&raw=true" title="preview8" width="400"/><br/>
      <b>Preview 8</b>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="Screenshots/preview9.jpg?sanitize=true&raw=true" title="preview9" width="400"/><br/>
      <b>Preview 9</b>
    </td>
    <td align="center">
      <img src="Screenshots/preview10.jpg?sanitize=true&raw=true" title="preview10" width="400"/><br/>
      <b>Preview 10</b>
    </td>
  </tr>
</table>

### Changelog

## Version 5.1.1.1 by Lululla – 2026-07-20

### Fixed
- **Zoom system** – completely refactored: now `0` always means fit-to-view for any resolution. Trackbar and numeric control are properly synced (positive = zoom in, negative = zoom out).
- **Crash** – fixed `NullReferenceException` in `PanelDesigner_Resize` that caused the app to close unexpectedly.
- **Zoom controls** – now properly respond to user input.

### Added
- **Batch delete** – in `experimental` mode (checkboxes enabled), you can now check multiple nodes (screens, widgets, etc.) and delete them all with a single `Delete` click.
- **Add Screen** – always creates the new screen at the root `<skin>` node, even if you are inside another screen or an include (with an informative message).

### Changed
- **Codebase** – all comments and source code are now in English for better maintainability and collaboration.
---

## Version 5.1.1.0 by Lululla – 2026-07-18

### Fixed

- **License bypass** – enabling/disabling premium features on the fly. :P

---

## Version 5.1.0.9 by Lululla – 2026-07-18

### Added

- **Splash screen** – added `fSplash` form with 800x600 background image (`splash.png` embedded as resource), version label (bottom-right), progress bar, status label, and file label.
- **Startup flow** – modified `Program.cs` to show splash, update progress and file name during initialization, wait 2 seconds after completion, then close splash and launch `fMain`.

### FIXED: 
- **Fix: Alpha button** – inverted logic: now Alpha ON shows colors with transparency, Alpha OFF forces opaque(debug mode).

## 🔐 Premium License
Some features require a premium license:
- **Telnet Commands** – Execute commands on Enigma2 receiver
- **Import/Export Skin** – Copy skin from/to Enigma2 (UNC)
- **Skin Diagnostics** – Advanced analysis (premium only)
- **Skin Converter** – Convert HD/FHD/WQHD/UHD
- **Automatic Updates** – Check and download new versions

Activate via `Tools → License`.  
Contact **Lululla** for activation.

---

## Version 5.1.0.8 by Lululla – 2026-07-17

### FIXED: Font Manager – Duplicate Display & Saving Issues

**Problem:**
- Fonts appeared duplicated in the Font Manager UI (both real fonts and file-name aliases)
- Removing a font from the list did NOT remove it from the database
- `Reload` button reset unsaved changes instead of refreshing the UI
- Modifications to `<fonts>` node in the Code tab were not reflected in Font Manager
- Paths were saved with double slashes (`fonts//Roboto-Regular.ttf`)
- Fonts from `<include>` files were not loaded when main `<fonts/>` node was empty

**Solution:**

**1. Added `IsAutoAlias` property to `sFont`**
- `IsAutoAlias` distinguishes file-name aliases (created by `AddFileAlias()`) from real fonts and user-defined aliases
- Used for filtering in UI and during save operations

**2. Added `Show Aliases` checkbox to Font Manager**
- Default OFF → hides file-name aliases (shows only real fonts)
- ON → shows all fonts + aliases (debug mode)

**3. Fixed `Remove` button**
- Now removes the font from **both** the ListView and the database
- Prevents removed fonts from reappearing after refresh

**4. Fixed `Reload` button**
- Now refreshes the UI from database (does NOT reload from disk)
- Preserves pending changes

**5. Fixed `initFonts()` in `cDataBase`**
- Merges `<fonts>` nodes from main skin AND all included files
- Fixes issue where fonts from includes were not loaded when main `<fonts/>` was empty

**6. Fixed `syncFonts()` in `cDataBase`**
- Uses `OriginalPath` for saving (preserves relative paths)
- Skips `IsAutoAlias` fonts during save (prevents duplicate re-writing)
- Normalizes paths (removes double slashes)

**7. Fixed `RefreshFontList()` in `fFonts`**
- Filters out `IsAutoAlias` fonts when checkbox is OFF
- Shows all fonts when checkbox is ON

**8. Fixed `RemoveDuplicateFonts()` in `fFonts`**
- Now acts on the database, not just the ListView
- Removes duplicate font entries before saving

---

### What Works Now:

1. **Font Manager UI** shows only real fonts (clean, no duplicates)
2. **Checkbox "Show Aliases"** toggles display of auto-aliases for debugging
3. **Remove** permanently deletes font from database (not just UI)
4. **Reload** refreshes UI without losing pending changes
5. **Saving** writes clean, duplicate-free XML with normalized paths
6. **Includes** are properly merged with main `<fonts>` node
7. **Code tab → Designer tab** changes are applied automatically

---

## Summary for Users:

- Open Font Manager → see only your defined fonts (no duplicates)
- Use **Show Aliases** checkbox to see debug info
- Add/Remove/Change fonts → works as expected
- Close window → changes are saved automatically

---

## Version 5.1.0.7 by Lululla – 2026-07-16

### Fixed
- **Fix: Color alpha fix** – RGB colors (#rrggbb) now correctly default to opaque (#ffrrggbb) instead of becoming transparent (#00rrggbb).
- **Fix: Color parser** – added missing alpha handling in sColor constructor for 6-digit hex strings." + Environment.NewLine +
- **Font scaling fix** – font conversion rules are now disabled by default to prevent double-scaling when converting skins (Enigma2 already handles font scaling). Users can enable them manually if needed.
- **Font path normalization** – absolute font paths are now converted to relative paths (fonts/filename.ttf) when saving the skin.
- **Duplicate removal** – duplicate font entries with the same name are skipped during sync to avoid conflicts.

---

## Version 5.1.0.6 by Lululla – 2026-07-14

### Fixed
- **Font path fix** – normalized font paths to remove duplicate "fonts" folder and double slashes.
- **Path normalization** – added check in MapFontPath() and getPath() to clean malformed paths.
- **Skin Converter** – disabled non-physical attributes by default: zPosition, index, scrollbarMode, scrollbarScroll, animationMode, animationPaused, split.
- **User experience** – users can still enable them manually if needed, but they won't be applied unintentionally during conversion.

---

## Version 5.1.0.5 by Lululla – 2026-07-12

### Added
- **Skin naming on creation** – user can now choose the skin name when creating a new skin via `File → New`, instead of using a temporary folder
- **Skin naming on conversion** – user can now choose the destination name when converting a skin via `Tools → Convert Skin...`, instead of automatic naming
- **New document button** – added "New" button in fOpen dialog to create a new skin directly from the open dialog.
- **Root toggle fix** – removed duplicate btnToggleRoot_Click method, kept version with "Show Root"/"Hide Root" labels.
- **Rulers toggle fix** – added missing btnToggleRulers_Click event handler.
- **UHD zoom fix** – extended zoom range from 0.4x–2.0x to 0.1x–5.0x for proper UHD display.
- **Ruler update** – rulers now properly refresh after zoom and resolution changes.
- **Root toggle button** – added btnToggleRoot toolbar button with show/hide functionality for the skin tree panel.

### Fixed
- **Save path** – removed `Path.IsPathRooted` check, always uses `Path.Combine(folder, fileName)` to prevent double path duplication (`D:\temp\Temp\D:\temp\Temp\...`)
- **Converter directory** – added `Directory.CreateDirectory(newSkinFolder)` before copy operations to prevent `DirectoryNotFoundException`
- **New skin persistence** – new skins are now saved permanently in `./skins/{user_choice}/skin.xml` instead of `%TEMP%\OpenSkinDesigner\`
- **Converter source path** – removed automatic fallback to `originalSkinPath` to prevent attempts to read from non-existent directories
- **New screen recursion** – fixed infinite screen creation when "new screen" is clicked on a screen node (screen is now added as sibling, not child)
- **Include handling** – when an include node is selected, new screen is correctly added as a child inside the include file
- **Crosshair fix** – reset transform after designer paint to draw grid and crosshair in correct client coordinates.
- **Grid fix** – grid now aligns with crosshair and scales properly with zoom.
- **Zoom fit calculation** – added CalculateFitZoom() to compute correct "fit to view" zoom for any resolution (HD, FHD, WQHD, UHD)
    Zoom calculation refactor – fixed variable conflicts by using unique names (openRes, fromFileRes, screenRes) across all methods.
- **Scrollbar fix** – zoom now properly fits the screen in the panel, eliminating unnecessary scrollbars at zoom 0 for FHD/WQHD/UHD.
- **Delete screen** – fixed deletion of screens (including empty screens) that caused freezes and recursion; manual node removal from ElementList without rebuilding tree, preventing path exceptions
- **New screen recursion** – blocked creation of screen inside another screen with error message and button disable when on a screen node

---

## Version 5.1.0.4 by Lululla – 2026-07-11

### Added

- **Skin Converter** – New dialog accessible from `Tools → Convert Skin...`
  - Convert skin between HD (1280x720), FHD (1920x1080), WQHD (2560x1440), UHD (3840x2160)
  - **Categories system** – attributes organized in categories (Fonts, Borders, Corner Radius, Gradients, etc.)
  - **Category checkbox** – check/uncheck a category to enable/disable ALL rules inside it
  - **Add/Edit/Remove Category** – create custom categories to organize your own rules
  - **Add/Edit/Remove Rule** – add custom rules to any category (Name, XML Attribute, Scale Mode)
  - **Double-click** – edit any rule by double-clicking it
  - **File list preview** – shows ALL XML files with checkboxes to select which ones to convert
  - **Async conversion** – UI no longer blocks during conversion
  - **Progress display** – shows current step, file name, and progress count
  - **Cancellation support** – click "Cancel" to stop conversion at any time
  - **Image rescaling** – with HighQualityBicubic interpolation
  - **Automatic backup** – original skin preserved, new skin saved in `SkinName_Resolution` folder
  - **Duplicate folder protection** – auto-increments folder name if already exists
  - **Full translations** – all dialogs and messages fully translatable

- **Open other XML from same folder** – New `File → Open other XML from same folder...` command
  - Open any XML skin file located in the same directory as the currently open skin
  - Useful for switching between multiple skins in the same folder (e.g., `MetrixHD/skin_alt.xml`)

- **Grid size setting** – Added to `Settings → Preferences`
  - Grid size is now persistent across sessions (saved in `settings.json`)
  - Press `G` key to cycle through grid sizes: `0, 5, 10, 20, 50` pixels
  - Grid status shown in the status bar (e.g., `Grid: 10 px` or `Grid: Off`)

### Fixed

- **Skin Converter**
  - Infinite folder recursion during skin copy (`_HD/_HD/_HD` nesting) – fixed
  - Include files not being converted – all XML files with convertible attributes are now processed
  - Colors corruption – using `XmlDocument` instead of raw Regex; only specific attributes are modified
  - UI freeze – conversion runs asynchronously with progress updates
  - Default skin opening after conversion – now opens the converted skin correctly
  - `ElementList` null error – proper file path resolution before conversion
  - License check – now only shows warning without closing the application
  - Tools menu items – disabled until a skin is opened

- **File counting during import/export**
  - `CountFiles` function now correctly counts each file only once (no more double counting)
  - Progress bar shows the correct total file count
  - Added exception handling for unauthorized access and missing directories

- **Skin Information**
  - Now shows all XML files in the skin folder, not just referenced includes

- **UI**
  - Crosshair button disabled by default until a skin is opened
  - Convert Skin menu item disabled until a skin is opened
  - Tools menu items (Telnet, Import, Export, Skin Information) disabled until a skin is opened

---

### v5.1.0.3 by Lululla

**Font loading & path resolution improvements**

- **Font loading revamped**  
  Fonts are now mapped automatically by filename, eliminating "Font not found" popups and fallback errors. Aliases are created on the fly so any reference to a font file (e.g. `lcd.ttf`) resolves correctly, even if the skin uses the filename instead of the logical name.

- **Path normalization fixed**  
  `getPath()` now checks the skin folder first, preventing double path concatenation and duplicate directory segments. This ensures all resources (images, fonts, includes) are found reliably, reducing spurious `FileNotFoundException` noise in logs.

- **Cleaner debug logs**  
  All font and path lookups now log detailed search steps, making it easier to diagnose missing resources without intrusive message boxes.

---

## Version 5.1.0.2 by Lululla – 2026-07-06

### Added

- **New Skin:**
  - New `File → New` command with resolution selection dialog to create a new skin from scratch
  - Includes default colors, fonts, windowstyle, and a blank screen
  - Available in menu and toolbar (New button)

- **Label enhancements:**
  - `shadowColor` and `shadowOffset` attributes for text shadow rendering with full HEX color support (`#AARRGGBB`)
  - `ellipsis`, `truncate`, and `lineHeight` attributes for advanced text control
  - `wrap="ellipsis"` support for RT_ELLIPSIS behavior (text truncated with `...`)
  - `fontScale` attribute with `size;N` (font size override) and `width;N` (horizontal compression) support, aligning with OpenATV `skin.py`
  - `setFontScale()` method for dynamic font scaling on labels
  - `pointWidth` parameter for additional horizontal compression of text characters

- **Listbox enhancements:**
  - `separatorLineColor` and `separatorLineSize` attributes for drawing lines between list items
  - `selectionZoom` and `selectionZoomSize` attributes for item scaling and zoom behavior
  - `entryFontScale` attribute with `size;N` (font size override) and `width;N` (horizontal compression) support for Listbox font scaling
  - `rtScroll` flag (value 1024) for multi-content scrolling support with mouse wheel interaction and scrollbar

- **Slider enhancements:**
  - `sliderPixmap` attribute for custom slider thumb images

- **WindowStyle designer:**
  - Fixed border image buttons (TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight) with proper file selection dialogs
  - Added `...` text to border buttons to indicate they are clickable
  - `entryFontScale` support for configList in windowstyle, aligning with OpenATV `skin.py`

- **Include file management:**
  - View and edit include file content directly from the treeview (tab Code now shows include file content)
  - Save changes directly to the include file when using the Sync button
  - Context menu with **Create Include from selected screens** to move selected screens to a separate include file
  - **Expand all includes** context menu option and automatic expansion of include nodes
  - **Create New Include File** in Element menu and toolbar with `addInclude` icon

- **Toolbar:**
  - Added **Add Include** button for quick creation of include files
  - Added **New** button for quick creation of new skins (File → New)
  - Added **Exit** button at the start of the toolbar for quick application exit

- **Font & Color enhancements:**
  - User-selectable **fallback font** via Preferences (Settings → Preferences → Fallback font)
  - System font fallback (Arial) when skin fonts fail to load, ensuring text is always visible
  - Fixed HEX color parser to correctly handle 6-digit `#RRGGBB` colors (now properly sets alpha to 255)
  - Fixed alpha channel inversion bug in `sColor` constructor that caused colors with alpha 255 to become transparent
  - Added fallback for named colors (`yellow`, `red`, `green`, etc.) when not defined in skin colors table

- **Preferences redesign:**
  - Completely redesigned Preferences form with **Visual Studio designer support** (`fPreferences.Designer.cs`)
  - Added **fallback font** combo box populated from the `fonts/` folder
  - Reorganized checkboxes into a **2-column layout** for a more compact form
  - Added **AutoScroll** to ensure all controls are accessible on smaller screens
  - Reduced form height by 30% while maintaining full functionality

- **Menu improvements:**
  - Template menu items are now disabled until a skin is opened (enabled on open, disabled on close)
  - Sort and Units menu items are now disabled until a skin is opened (enabled on open, disabled on close)

- **Premium Features:**
  - **Automatic Updates** – checks for new versions and downloads updates automatically

### Improved

- **Save & Cleanup:**
  - Fixed double `.xml.xml` extension bug
  - Removed automatic saving of duplicate `skin_*.xml` include files
  - Added automatic cleanup of backup files (`skin_*.xml`) on application close to keep skin folders clean
  - Fixed save path double path issue (absolute paths now handled correctly)

- **Font loading:**
  - Fixed double path bug causing `fonts\\D:\\...` errors when loading fonts from absolute paths
  - `MapFontPath` now extracts file names from absolute paths (`/usr/share/fonts/...`) and searches locally in the `fonts/` folder
  - Added support for font file name variations (case, underscores, dashes) for better compatibility with different skin sources

- **Import Screen:**
  - Now imports **ALL screens** from the selected file, not just the first one
  - Handles both single-screen files and files with multiple screens

- **Include handling:**
  - Parser now continues processing even when an included file is not found (skips missing includes instead of stopping)
  - This prevents screen loss when a referenced include file is missing

- **Resolution handling:**
  - Automatically creates `output`/`resolution` nodes when changing skin resolution if they don't exist in the XML

- **Code organization:**
  - Centralized menu/toolbar enable/disable logic into `EnableAllMenusAndToolbars()` and `DisableAllMenusAndToolbars()`
  - Eliminated code duplication across `open()`, `close()`, and `CreateNewSkin()`
  - `MyGlobaleVariables` moved to `OpenSkinDesigner.Structures` namespace for better organization

- **Include resolver:**
  - Now handles nested `<include>` files with support for `filename`, `file`, `src`, `source`, and `href` attributes
  - Resolves absolute paths `/usr/share/enigma2/...` to relative paths

- **Full compatibility with OpenATV `skin.py` features:**
  - `shadowColor`, `shadowOffset`
  - `ellipsis`, `truncate`, `lineHeight`
  - `fontScale` (`size;N` / `width;N`)
  - `wrap='ellipsis'`
  - `separatorLineColor`, `separatorLineSize`
  - `sliderPixmap`
  - `entryFontScale`
  - `RT_SCROLL`

### Fixed

- `NullReferenceException` in `sGraphicScreen` when opening WindowStyle designer
- `DirectoryNotFoundException` when skins folder is missing (added directory creation fallback)
- Color parser now correctly handles 6-digit `#RRGGBB` colors
- Alpha channel inversion bug in `sColor` constructor
- Double `.xml.xml` extension bug in save system
- Duplicate `skin_*.xml` include files no longer created
- `foregroundColor="yellow"` and other named colors now work without explicit definition in skin
- `NullReferenceException` in `cDataBaseResolution.setResolution()` when resolution node was missing
- Save path now correctly handles absolute file paths (no more double path concatenation)
- `ArgumentOutOfRangeException` in Preferences by ensuring comboboxes are populated before setting `SelectedIndex`
- Designer errors in `fPreferences` (missing `using`, `for` loops, uninitialized event handlers)
- `cmbFallbackFont_SelectedIndexChanged` event handler error (removed unused event)

### Translation Files (.lng)

- Translation files use the format `Key:: Value` where:
  - `Key` is the English text (case-sensitive)
  - `Value` is the translated text
  - Separator is `::` (double colon)

### Notes

- **Preferences designer:** The Preferences form now has full Visual Studio designer support (`fPreferences.Designer.cs`). Do not modify the UI code in `fPreferences.cs`.
- **Fallback font:** If you experience font loading issues, go to `Settings → Preferences` and select a fallback font from the list. The combo box is automatically populated from the `fonts/` folder.
- **Exit button:** The toolbar now includes an **Exit** button at the beginning (before "New") for quick application exit.
- **Font paths:** Absolute font paths (`/usr/share/fonts/...`) are now normalized to file names and searched in the local `fonts/` folder. If the font is not found, the fallback font is used.

---

### Version 5.1.0.0 by Lululla – 2026-06-22

**Added:**
- New **Skin Information** module:
  - Detailed skin analysis with two tabs: **Info** and **Diagnostics**
  - Displays skin metadata: Name, Version, Author, Path, Resolution
  - Structural analysis: Screens, Panels, Widgets, Colors, Fonts, Attributes, Includes
  - Resolves `<include>` files to count all elements correctly
  - Preview image support: loads `prev.png` from skin folder
  - Diagnostics panel shows:
    - Found and missing Renderers, Converters, Pixmaps, Images
    - Unused images detection
  - Export all data to a `.txt` file on desktop with version and support links
  - Fully translatable via existing language system

- **Preferences** module completely redesigned:
  - Full manual UI (no PropertyGrid, no designer issues)
  - All settings are now visible and editable
  - Fallback color picker with live preview
  - Premium license now hides/disables "Project" settings (network paths, folders)

- **Premium License System**:
  - Activation via key (HMAC-SHA256 based)
  - Premium features: Telnet, Import/Export from Enigma2, Skin Diagnostics, Network paths
  - License status displayed in Tools → License
  - Click on status label to show license details

- **License status**
  -displayed in `About` window (Premium/Free with color indicator).

- **Automatic backup**
  - of `settings.json` and `license.lic` during update, preserving user preferences and license activation.

- **Complete Help section**
  -(`fHelp`) with all keyboard shortcuts, premium features, and support links – now includes application logo.

**Improved:**
- Skin parser now resolves nested includes (supports `filename`, `file`, `src`, `source`, `href`)
- Better error handling for missing include files
- Update system now safely backs up user data before launching the installer.
- UI layout optimized for skin information display
- `fOpen` now hides network controls when not premium
- `fTelnet` and `fTelnetConfig` are now protected by premium license

**Fixed:**
- `NullReferenceException` when loading skin info
- `lblResolution` missing control
- Empty Resources panel in Skin Information form
- MessageBox translations for export confirmation
- `fPreferences` visibility issues (completely rebuilt)
- Fallback color not persisting between sessions
- Premium menu items not updating after activation
- License menu items now update correctly after activation.
- Language selection and UI translations are more reliable.


### MOD v5.0.0.7 by Lululla

**Network skin management**

- **Auto-copy to local**  
  Opening a network skin automatically copies it to the local `./skins` folder with a progress bar showing file count and current file.

- **Local backup on overwrite**  
  If a local skin with the same name exists, it is backed up with `_backup_` timestamp before being overwritten.

- **Clear work status**  
  Status bar shows whether you are working on a local skin or a network skin.

- **Open confirmation**  
  When opening a skin, a dialog shows the full path and warns about the working location.

- **Borderset parsing fix**  
  Safe handling of missing pixmap files and attributes, preventing NullReferenceException when loading skins with incomplete borderset definitions.

- **Color parsing fix**  
  Added robust hex conversion with fallback to magenta, preventing FormatException on invalid color values.

- **Indexer usage fix**  
  Replaced incorrect indexer syntax with `get()` method calls in color lookups.

**Open dialog enhancements**

- **Refresh button**  
  Reload the skin list without closing the form.

- **Delete button**  
  Remove skins (local and network) with confirmation, full path display, and security check to prevent deletion outside the configured network folder. Handles locked files with automatic retry.

- **Backup visibility**  
  Network skin backups appear in the Open dialog with the `(backup)` label and can be opened directly as normal skins.

- **Currently opened tag**  
  The skin currently opened in the designer is tagged with `(currently opened)` in the Open dialog.

**Import/Export improvements**

- **Progress bars**  
  Both import and export now show file count and current file being copied/uploaded.

- **FTP root path**  
  Configurable in Telnet settings for Export Skin to Enigma2.

**Help & documentation**

- **Full user guide**  
  Complete About from init version 1.0.0 by schischu65 (Nov 23, 2009)
  The Help dialog now includes a comprehensive guide covering all features: Open dialog, network management, import/export, keyboard shortcuts, designer tools, code editor, Telnet/FTP, preferences, templates, and troubleshooting.


### MOD v5.0.0.6 by Lululla

**Rulers positioning & stability**

- **Rulers placed correctly**  
  Horizontal and vertical rulers are now positioned outside the skin preview area – the horizontal ruler sits just below the designer toolbar, and the vertical ruler is to the left of the preview. No more overlapping with the skin or toolbar buttons.

- **Rulers stay put during zoom/scroll**  
  Rulers are now fixed during zoom and scroll operations. They only reposition when the main window or designer panel is resized, ensuring consistent alignment.

- **Rulers button state fixed**  
  The "Rulers" toggle button now correctly reflects whether rulers are visible. Rulers are automatically hidden when a skin is closed.

- **Event handler cleanup**  
  Removed duplicate event subscriptions to prevent double execution and improve performance.

- **General code improvements**  
  Targeted refactoring for better maintainability and stability.

### MOD v5.0.0.5 by Lululla

**Bug fixes & improvements**

- **Rulers positioning**  
  The horizontal ruler is now correctly placed below the designer toolbar, no longer overlapping the "Marker", "Show all" and other toolbar buttons.

- **Rulers translation**  
  The "Rulers" button in the designer toolbar is now fully translatable using `GetTranslation`. Added the `Rulers` key to all language files.

- **Marker label translation**  
  The "Marker" label now uses `AutoSize = true` so that translated text (e.g. Italian "Marcatore") is no longer cut off.

- **Event handler cleanup**  
  Removed duplicate event subscriptions for `Shown`, `ResizeEnd`, `panelDesigner.Resize` and `panelDesignerInner.Scroll`. Only named methods are used, preventing double execution.

- **Template names**  
  Template file names in the "Template" menu are not translated – they remain as physical file names to avoid confusion.

- **General code cleanup**  
  Redundant lambda expressions removed, event handlers consolidated for better maintainability.

- **Fixed NullReferenceException on skin load**  
  The application no longer crashes when opening skins that are missing the `<colors>` or `<fonts>` nodes (e.g., skins that rely on `<include>` references). Fallback colors are automatically used when the skin XML is incomplete.

- **Improved XML parsing robustness**  
  Added null checks for critical XML nodes (`colors`, `fonts`, `output`) in `cDataBase`. The parser now logs warnings and continues with default values instead of throwing exceptions.

- **Better include file handling**  
  Missing `<include>` files are now skipped gracefully, with a warning logged to the console, preventing unexpected crashes when a skin references external files that are not present.

- **Display skin resolution in window title**  
  The main window title now includes the current skin resolution in parentheses (e.g., `Aglare-FHD (1920x1080)`). The resolution is also shown next to the skin name in the toolbar. A fallback resolution of `1280x720` is used when the skin XML does not specify one.
  
- **General stability**  
  The application is now more resilient to malformed or incomplete skin files, ensuring a smoother user experience even with custom or legacy skins.


### v5.0.0.4 by Lululla

### Complete migration to `AppSettings`

**Bug fixes & improvements**
- Replaced `Properties.Settings` with `AppSettings` (JSON stored in `%LocalAppData%\OpenSkinDesigner\settings.json`)
- Fixed settings persistence on Windows 11 (file system virtualization was causing values to reset)
- Settings are now saved in the application folder for debugging
- Fixed settings loading on startup: `ApplySettingsToUi()` is now called **after** all menus are created, preventing `NullReferenceException`
- Fixed `UseCustomLanguage()` crash when menus were not yet initialized
- Added null checks in `StopAutoSaveTimer()` and `StartAutoSaveTimer()`
- Fixed language selection persistence in the menu on restart
- Debug MessageBoxes in `AppSettings` are now translated and only visible in DEBUG mode

### Code cleanup

- Removed `RemoteConfig.cs` (obsolete)
- Cleaned `app.config` – removed `<userSettings>` and `<configSections>` sections
- Removed duplicate `Content` and `None` entries from `.csproj`; folders are now included using `**\*.*`
- Unified Telnet and FTP settings into `AppSettings` (removed `telnet_config.json`)

### Translations
- Language menu now loads correctly on startup

### Persistence
- `settings.json` is now created in the same folder as the executable during debug
- All values (language, paths, checkboxes, fallback color, Telnet/FTP credentials) are now properly saved and restored

### v5.0.0.3 by Lululla
**Minor fixes**: Corrected Preference save on close.

### v5.0.0.2 by Lululla

**New features**

- **Configure button in Open dialog**  
  Set Telnet/FTP credentials directly from the Open window. The UNC path for skins is built automatically and saved.

- **Import/Export skin via UNC**  
  Import and export functions now use the UNC path (file copy). Progress bar, local backup on overwrite, and proper handling of access denied errors.

- **Full translation support**  
  All menu items (Tools, Units, Help, Preferences, Open skin from folder, etc.) are now translatable. Fixed missing translations by converting local menu variables to class fields.

**Fixes**

- Corrected Scintilla margin configuration.
- Fixed NullReferenceException in language loading order.
- Removed redundant code and improved stability.

### v5.0.0.1 by Lululla

**New Features & Improvements**

- **Open skin from any folder**  
  Added a new menu entry `File → Open skin from folder...` 
  that allows opening a skin from any directory on your computer (e.g., desktop, download folder, network path). 
  The folder must contain a valid `skin.xml` file. 
  The feature respects unsaved changes checks and is fully translatable via `GetTranslation`.


### v5.0.0.0 by Lululla  

**.NET 10 Modernization Release**  

- **Full .NET 10 migration**:
  The entire application has been ported from .NET Framework 4.8 to .NET 10, ensuring compatibility with modern Windows versions, improved performance, and better security.  

- **Scintilla5.NET integration**:
  Replaced the legacy ScintillaNET library with Scintilla5.NET, fully compatible with .NET 10. All editor features (syntax highlighting, auto‑completion, code folding, line wrapping) are now working correctly.  

- **Rulers visibility fixed**:
  Horizontal and vertical rulers now appear correctly when a skin is opened and hide when the skin is closed. The 'Rulers' button in the designer toolbar reflects the actual state.  

- **Auto‑update version comparison**:
  The update check now uses proper semantic version comparison (System.Version). Updates are offered only when the online version is strictly greater than the installed one, preventing false update prompts.  

- **Extended translation coverage**:
  Over 95% of the user interface strings are now translatable, including all entries in the keyboard shortcuts help window. Missing translations default to English.  

- **Grid and magnet snap improvements**:
  Designer grid and magnetic snapping now work more reliably, with visual feedback in the status bar (press G to toggle grid, M to toggle magnet).  

- **Network skin tagging**:
  Network skins are now clearly marked in the open dialog with a '(network)' tag. The original path remains unaffected for saving.  

- **General stability and performance**:
  Numerous bug fixes, code cleanup, and internal refactoring to enhance the overall user experience and maintainability.

### v4.2.4.3 by Lululla

**New Features & Improvements**

- **Auto-update version comparison fix**  
  The update check now correctly compares semantic versions using `System.Version`. Previously any version difference (even if the online version was older) would trigger an update request. Now the update is offered only when the online version is strictly greater than the installed one.

- **Rulers visibility fix**  
  Rulers (horizontal and vertical) are now properly shown when the application starts and when a skin is opened. The 'Rulers' button in the designer toolbar reflects the correct state (checked when visible). Rulers disappear automatically when the skin is closed.

- **Translation coverage extended**  
  Language support has been increased to cover approximately 95% of all UI strings, including every entry in the keyboard shortcuts help window. Missing translations fall back to English gracefully.

- **Minor stability improvements**  
  General code cleanup and small bug fixes to enhance the overall user experience.

### v4.2.4.2 by Lululla

**New Features & Improvements**

- **PropertyGrid category collapse**  
  The '0 XML attributes' category is now automatically collapsed by default, keeping the property view tidy and focused on standard attributes.

- **Shift+arrow key movement**  
  Holding Shift while moving a widget with arrow keys now moves by 10 pixels instead of 5, allowing faster repositioning. Ctrl+arrow remains 1 pixel for fine tuning.

- **Magnetic snapping (M key)**  
  When moving a widget with the mouse, its edges snap to other widgets or screen borders within a 6-pixel threshold. Press M to toggle (ON/OFF), with status displayed in the global status bar. Magnetic snap is applied before grid snap when grid is enabled.

- **Keyboard Shortcuts help window**  
  Added a dedicated help window (`FHelp`) listing all keyboard shortcuts and mouse actions, accessible from the `?` menu → `Keyboard Shortcuts`. The window content is fully translatable via `GetTranslation`.

### v4.2.4.1 by Lululla

**New Features & Improvements**

- **Auto‑update**  
  - Added `Check for updates` entry under the `?` (Help) menu.  
  - Compares the current version with a `version.txt` file hosted on GitHub.  
  - If a newer release is available, the browser opens to the release page for manual download.  
  - No external dependencies – works with standard .NET `WebClient`.

- **Stability & refinements**  
  - Fixed missing references and assembly issues for the update mechanism.  
  - Updated changelog and translations for the new feature.

### v4.2.4.0 by Lululla

**New Features & Improvements**

- **Resolution rescaling**  
  - Added a ComboBox with all common resolutions (720p, 1080p, 1440p, 2160p).  
  - Automatically rescales positions, sizes, fonts, and images when changing resolution – no manual work needed.

- **Hybrid Preferences dialog**  
  - New layout: PropertyGrid on the left for main settings (paths, auto‑save, language, colors, editor, designer).  
  - ListView on the right for raw key/value properties (advanced users).  
  - Keeps all your original settings and supports dynamic language switching.

- **cDesigner zoom enhancements**  
  - Zoom range extended from 0.4x–2.0x to 0.35x–10.0x (better detail view).  
  - Added `getAttributes()` and `getAttribute(XmlNode)` methods for future multi‑selection support.

- **sGraphicRectangel improvements**  
  - Full support for selective corner rounding (e.g., `30;topLeft,topRight`).  
  - Unified gradient rendering for backgrounds and selections.

- **Stability**  
  - Fixed missing `using System.Xml;` in `cDesigner.cs`.  
  - No regressions – all existing features (cornerRadius, gradient tolerance, background fallback, etc.) remain intact.

### v4.2.3.9 by Lululla

**New Features (ported from OpenATV version)**

- **Add OpenATV Element menu**:
  - New menu (under "Element") and toolbar button to quickly insert OpenATV‑specific elements: `Panel Reference`, `Inline Panel`, `Stack`, `Rectangle`, `Applet`, `Constant Widget`, `Layout`.
  - Custom icons and full translation support.

- **Missing panel logging**:
  - Logs each missing panel reference only once (with context) to avoid spamming the log file.

- **Double‑click on colors/fonts**:
  - Directly opens the Colors or Fonts dialog instead of switching to the Code tab – much faster editing.

- **Convert wizard**:
  - Double‑click on any `<convert>` node opens a simple dialog to edit its content.
  - Full undo/redo support via the command queue.

- **Editor change tracking suppression**:
  - Prevents false "unsaved changes" flags when switching tree nodes.
  - The flag is now set only when the user actually types in the editor.

- **Raw XML attributes in PropertyGrid**:
  - A new category **"0 XML attributes"** appears in the PropertyGrid for any selected element.
  - Shows all XML attributes that are not handled by standard properties (custom or unknown attributes).
  - For `<convert>` nodes, a `value` property is also available to edit the inner text.

- **Auto‑save before switching tabs**:
  - When leaving the **Code** tab for the **Designer** tab, the editor content is automatically validated.
  - If the XML is valid, changes are applied silently and the tab switches.
  - If invalid, the tab switch is blocked and the error is shown in the status bar (no intrusive message boxes).

### v4.2.3.8 by Lululla

**Bug Fixes & Improvements**

- **Background fallback fixed**:
  - Restored background image loading (`background.jpg`, `background1920.jpg`, etc.) by improving `cDataBase.getPath()` to search in the `skins` folder next to the executable.
  - Background now works correctly for all resolutions (4K, QHD, FHD, and default).

- **Image path resolution enhanced**:
  - `getPath()` now looks for images in multiple locations: project folder, skin folder, `skins` folder (next to the executable), and the executable folder itself.
  - This ensures all pixmaps and background images are found even when opening skins from network paths (UNC) or relative folders.

- **CornerRadius as string**:
  - `cornerRadius` attribute now accepts string values like `30;topLeft,topRight`.
  - The numeric part is extracted for rendering; the full string is preserved in XML for compatibility with downstream tools.

- **BackgroundColor gradient tolerance**:
  - `backgroundColor` attribute now accepts gradient syntax (e.g. `red,green,vertical` or `#00101010,#00303030,vertical`) without throwing "invalid color" errors.
  - Gradients are saved correctly to XML (preview not implemented, but no crashes).

- **Fallback images for widgets**:
  - Improved loading of default images for render types (`picon`, `pig`, `xtraposter`, `xtrabackdrop`, `xtraparental`, `xtrastar`, `xtranextevents`, `msnweatherpixmap`, etc.).
  - Added missing mappings for `posterx`, `weather`, `boximage`, and `genre`.
  - The `skins` folder is now the primary search location for these default images.

- **Stability fixes**:
  - Fixed `NullReferenceException` in `sGraphicWidget.updateObject` and other runtime crashes.
  - Restored original `sGraphicImage` constructor to avoid missing dimensions for background images.

- **Code cleanup**:
  - Removed duplicate constructors in `sGraphicImage` and unified image loading logic.
  - Restored original `drawBackground()` method in `cDesigner.cs` for reliability.
  - Cleaned up unnecessary modifications that broke the preview.

### v4.2.3.7 by Lululla

**New Features**

- **Telnet Commander**:
  - Added standalone Telnet module to connect to Enigma2/DreamOS boxes.
  - Execute common commands (init 4, killall -9 enigma2, systemctl stop/start, screenshot, tail logs, reboot, halt, etc.).
  - View real-time command output in a dedicated monitor (RichTextBox).
  - Custom commands can be added, removed, and saved/loaded from `Telnet/TelnetCommands.xml`.
  - Dedicated toolbar button (`telnet.png`) opens a resizable, user‑friendly window.
  - Supports user/password authentication (default: root / your box password).

- **Translation updates**:
  - Added Italiano, English, Deutsch, Français, Español, Português, Polski, Português, Türkçe, Русский, العربية, Shqip, 中文（简体）, 中文（繁體) translations for all Telnet strings and the new gradient properties.


### v4.2.3.6 by Lululla

**New Features**

- **Template system**:
  - Added new "Template" menu to insert custom widgets/pixmaps/labels/sliders from XML files stored in a configurable `templates` folder. Includes example templates for quick start.

- **Open Screen**:
  - Open standalone screen XML files (without `<skin>` wrapper), edit them, and save back only the screen node – ideal for offline screen editing and version control.
  - Fixed zoom functionality when opening standalone screen files; zoom slider and numeric box are now properly enabled.
  - Open Screen now respects the screen's actual size attribute instead of defaulting to 1920x1080.

- **Import Screen**:
  - Import an external screen XML file into the currently open skin, merging it as a new screen.

- **Label text wrap**:
  - Added "Wrap Text" property for eLabel (and widget render="Label") to enable automatic line wrapping (XML attribute `wrap="1"`).

- **Auto-save**:
  - Added optional auto-save feature (every X minutes) with status bar notification.

- **Network support**:
  - Added ability to open and save skins directly from network paths (UNC). Network folder can be set in Preferences.

- **Font management**:
  - Added full font editor (Add, Remove, Change buttons) in Fonts window. Font name, path, scale, size, and replacement are now editable. Changes are saved to `skin.xml` immediately.

- **Skin project paths**:
  - Added Preferences for Rootfs folder (to resolve system fonts/images) and Enigma2 source folder (for developer reference).

**Improvements**

- **Converter improvements**:
  - Enhanced cConverter with safer value parsing (getIntValue, getSourceTable), better null handling, and support for parent source references.

- **Coordinate system**:
  - Enhanced `parseCoord` to support advanced expressions (`e-10`, `bottom-10`, `center-100`, `top+20`, `right-50%`, etc.). Fixed `FormatException` when using negative values or percentages.

- **Listbox improvements**:
  - Added context‑aware preview entries (menu, bouquet, EPG, movie lists) and smarter font detection (priority attributes like serviceNameFont, EventFontVertical, etc.).

- **Label preview**:
  - Added context‑aware preview text for dynamic sources (clock, events, channels) when no explicit text is set.

- **Code improvements**:
  - Added `cSkinProject.cs` to manage skin, rootfs, and Enigma2 source paths.
  - Enhanced `cDataBase.cs` with `setFonts()`, `syncFonts()`, `renameFontReferences()`.

**Stability & Localization**

- **Stability fixes**:
  - Fixed multiple exceptions when opening single‑screen files (missing mandatory tags like `output`, `colors`, `fonts`, `windowstyle`). Properly handles null references.

- **Localization**:
  - Added translations for all new strings (Template, Open Screen, Import Screen, Wrap Text, Auto-save, Network paths, Rootfs, Enigma2 source, etc.) into all language files.

- **Code cleanup**:
  - Removed duplicate gradient properties, unified gradient handling, general refactoring.


### v4.2.3.5 by Lululla

**New Features**

- **Auto-save**:
  - Added optional auto-save feature (every X minutes) with status bar notification.

You can enable automatic saving of your skin at regular intervals.

*How to use:*
1. Go to **Settings → Preferences**.
2. Check **"Auto-save every"** and set the number of minutes (1–60).
3. Click **OK**.
4. When a skin is open and you make changes, the program will automatically save it every X minutes.
5. A message like `Auto-saved at 14:35` will appear in the status bar.

**Note:** Auto-save only triggers if there are unsaved changes. It uses the normal `save()` function, so it works for both local and network skins.

- **Network support**:
  - Added ability to open and save skins directly from network paths (UNC). Network folder can be set in Preferences.

You can now open and save skins directly from a network share (e.g. your Enigma2 box) without copying files to your local PC.

*How to set up:**
1. Make sure your Enigma2 box has Samba (Windows share) enabled and that the skin folder (e.g. `/usr/share/enigma2/`) is shared.
2. In OpenSkinDesigner, go to **Settings → Preferences**.
3. Under **"Default network path (UNC)"**, enter the path to the **parent folder** that contains your skin subfolders.  
   Example: `\\192.168.1.78\Root\usr\share\enigma2`
4. Click **Browse...** to select the folder visually, then **OK**.

*How to open a network skin:**
- **File → Open**  
  The list will now show **both your local skins (from `./skins/`)** and **any network skins found in the UNC path**.
- Select a skin from the list and click **Open**.
- The skin will load exactly like a local one. You can edit, add widgets, change properties, etc.

*How to save a network skin:**
- Just press **Ctrl+S** or use **File → Save**. The program will overwrite the original `skin.xml` on the network share.

**Stability & Improvements**

- **Bug fixes**:
  - Fixed `ArgumentNullException` in `GetTranslation()` when no language file is loaded.
  - Removed orphaned methods and unused constants.

- **Code cleanup**:
  - Removed duplicate gradient properties, unified gradient handling, and general refactoring.

- **Important notes:**
  - The network path must be accessible and writable by Windows.
  - You must have proper permissions on the share.
  - If you only want to edit a single screen file (without `<skin>` wrapper), use **File → Open Screen...** instead.


### v4.2.3.4 by Lululla

**New Features**

- **Template system**:
  - Added new "Template" menu to insert custom widgets/pixmaps/labels/sliders from XML files stored in a configurable `templates` folder.
  - Includes example templates for quick start (label, pixmap, slider, progress).

- **Open Screen**:
  - Open standalone screen XML files (without `<skin>` wrapper), edit them, and save back only the screen node – ideal for offline screen editing and version control.

- **Import Screen**:
  - Import an external screen XML file into the currently open skin, merging it as a new screen.

- **Label text wrap**:
  - Added "Wrap Text" property for `eLabel` (and widgets with `render="Label"`) to enable automatic line wrapping (XML attribute `wrap="1"`).

**Stability & Improvements**

- **Stability fixes**:
  - Resolved multiple exceptions when opening single‑screen files (missing mandatory tags like `output`, `colors`, `fonts`, `windowstyle`).
  - Properly handles null references in `cDataBase` and `sAttributeScreen` during wrapper generation.

- **Code improvements**:
  - Enhanced XML wrapper generation for single‑screen editing.
  - Unified gradient handling, general refactoring and cleanup.

### v4.2.3.3 by Lululla

**New Features**
- **OpenATV integration**:
  - Added multi-select support.
  - Added grid support.
  - Added magnet/snap functionality.
  - Added OpenATV element menu integration.

- **New element templates**:
  - Added new clock variants.
  - Added PIG (Picture-in-Graphics) templates.
  - Added progress bar templates.
  - Added rounded panel templates.
  - Added various OpenATV component templates.

## Correct flow for using templates
  - Open a skin (or create a new one with **File → New Screen**).
  - Select a screen in the tree on the left.
  - Open **Menu → Template**.
  - Select a template (example: `multi_example`).
  - Widgets will be inserted into the selected screen.

  > ⚠️ Templates can only be inserted inside a **screen**.
  > Selecting a widget or another element will not work.

- **WindowStyle improvements**:
  - Added WindowStyle preview support.
  - Fixed WindowStyle rendering and related issues.

- **Crash handling**:
  - Added a global crash handler for improved stability and debugging.

- **Language & startup fixes**:
  - Updated translations and language resources.
  - Fixed startup crash issues.

### v4.2.3.2 by Lululla

**New Features**
- **Screen reordering**: Added new buttons in the main toolbar to manage screen order inside the skin tree:
  - **Move Up** – Move the selected screen one position up.
  - **Move Down** – Move the selected screen one position down.
  - **Sort Screens** – Automatically sort all screens alphabetically by name (case-insensitive).

- **Code language**: Entire project migrated to English (comments, identifiers, UI messages).

- **Rulers & guidelines**:
  - Added horizontal and vertical rulers with precise skin coordinate tracking.
  - Added red guidelines that correctly follow the mouse cursor at any zoom level.
  - Fixed coordinate conversion issues affecting guideline positioning.

- **Zoom fixes**:
  - Resolved guideline and mouse pointer misalignment when zoom level is not 1:1.

- **UI improvements**:
  - Added ruler toggle button in the designer toolbar.
  - Improved ruler tick marks and number visibility.

- **Code cleanup**:
  - Removed duplicate Paint event subscriptions.
  - Optimized mouse coordinate handling.
  - General refactoring and cleanup.
 
### v4.2.3.1 by Lululla
**New Features**
- **Screen reordering**: New buttons in the main toolbar to manage screen order inside the skin tree:
  - **Move Up** – Move the selected screen one position up.
  - **Move Down** – Move the selected screen one position down.
  - **Sort Screens** – Automatically sort all screens alphabetically by name (case‑insensitive).
  **Code language**: Entire project migrated to English (comments, identifiers, UI messages).

### v4.2.3.0 by Lululla

**New Features**

- **ClockToText** extended with new time formats:
  - `%l` – 12‑hour without leading zero (1‑12)
  - `%I` – 12‑hour with leading zero (01‑12)
  - `%e` – day of month without leading zero (1‑31)
  - `%P` – lowercase AM/PM (`am`/`pm`)
  - `%p` – uppercase AM/PM (`AM`/`PM`)
- **ServiceName** new modes:
  - `ChannelNumber` – e.g., `101`
  - `ChannelNumberAndName` – e.g., `101 - Rai 1`
  - `PiconName` – sanitized name for picon files
  - `ReferenceName` – last part of the service reference
- **Slider widget (`eSlider`)** fully implemented:
  - Horizontal/vertical orientation
  - Properties: `Value`, `Min`, `Max`, `Step`, `Orientation`
  - Supports gradients, pixmap, alpha test, borders
- **Listbox enhancements**:
  - `selectionZoom` – zoom effect on the selected item (in `sGraphicListbox`)
  - `scrollbarBackgroundGradient` and `scrollbarForegroundGradient` for listbox scrollbars
- **Gradient support for any widget** (via base `sAttribute` – `BackgroundGradient`, `ForegroundGradient`)

**Fixes & Improvements**
- Fixed `NullReferenceException` in `sAttributeWidget` when converter node has no `type` attribute.
- Fixed `ArgumentNullException` in `ClockToText.getText` when `Source` is null or `time_sec` key missing.
- Fixed compilation error CS0019 (`bool?` operator) in `sAttributeWidget` constructor.
- Enhanced corner‑radius mask handling in `sGraphicRectangel` – raw values like `"30;topLeft,topRight"` are preserved and rendered correctly.
- Improved `cDataBase.getPath` to handle empty/null paths gracefully.
- Fixed `cDataBase.rescaleLocations` to use the new resolution for `position="center"`.
- Replaced all `Hashtable.Add` calls with indexer to prevent duplicate key exceptions.
- Removed duplicate field declarations in `sAttributeListbox` and added missing properties.
- General code cleanup: removed unused variables, redundant comments, silenced unnecessary message boxes.
- Full compatibility with existing skins (gradients stored in `backgroundColor` or `backgroundGradient`).

**Example of a modern skin using new features:**

```xml
<!-- Clock with 12‑hour format and lowercase am/pm -->
<widget source="global.CurrentTime" render="Label" position="100,100" size="300,50">
  <convert type="ClockToText">Format%l:%M %P</convert>
</widget>

<!-- Service name with channel number -->
<widget source="session.CurrentService" render="Label" position="100,160" size="400,50">
  <convert type="ServiceName">ChannelNumberAndName</convert>
</widget>

<!-- Slider with gradient -->
<widget render="eSlider" position="100,220" size="400,30" orientation="horizontal" min="0" max="100" value="50" step="5" foregroundGradient="blue,cyan,white,horizontal" />

<!-- Listbox with selection zoom and scrollbar gradient -->
<widget render="Listbox" position="100,280" size="300,200" selectionZoom="20" scrollbarForegroundGradient="#ffaa00,#ff8800,#ff5500,vertical" />
```

### v4.2.2.0 by Lululla

This release focuses on stability, robustness and full compatibility with existing skins, fixing several edge‑case crashes and improving error handling.

**Fixes and improvements:**

* Fixed `NullReferenceException` in `sAttributeLabel` constructor when window style or color tables are missing.
* Added robust fallback colors (`LabelForeground`, `LabelBackground`, `Background`) when the skin’s `<windowstyle>` is incomplete or absent.
* Secured the `<convert>` node parsing with try‑catch and null checks – malformed converter entries no longer crash the designer.
* Ensured safe access to `pWindowStyle.pColors` using `ContainsKey` before direct indexing.
* Corrected implicit progress widget detection (`IsImplicitProgressWidget`) for better compatibility with old skins.
* Enhanced corner‑radius mask handling in `sGraphicRectangel` – raw values like `"30;topLeft,topRight"` are preserved and displayed correctly (partial rounding).
* Fixed compilation error CS0019 (`bool?` operator) in `sAttributeWidget` constructor by adding explicit `pRender != null` check.
* Improved `cDataBase.getPath` to handle empty or null paths gracefully (avoids `NotSupportedException`).
* Fixed `cDataBase.rescaleLocations` to use the new resolution for `position="center"` – elements stay centred after resolution change.
* Replaced all `Hashtable.Add` calls with the indexer to prevent duplicate key exceptions.
* Removed duplicate field declarations in `sAttributeListbox` (`pListboxMarked*`, `pscrollbarRadius`) and added missing properties (`sAttributeProgress.Foreground`, `sAttributeListbox.ItemCornerRadiusSelected`).
* Added helper methods `SetOrCreateAttribute` and `RemoveAttributeIfExists` for safer XML attribute handling.
* General code cleanup: removed unused variables, redundant comments and improved naming consistency.
* Full compatibility with skins that store gradients either in `backgroundColor` or `backgroundGradient`.

**Example of a working corner‑radius mask in a screen:**

## Screenshots
<p align="center">
<img src="Screenshots/preview4.jpg?sanitize=true&raw=true" title="preview4" width="400"/>
</p>

```xml
<screen name="Test_All_Features" position="0,0" size="1920,1080" backgroundColor="transparent" flags="wfNoBorder">
  <!-- 1. Label with VERTICAL gradient and masked cornerRadius (top corners only) -->
  <eLabel backgroundColor="red,green,blue,vertical" cornerRadius="30;topLeft,topRight" position="50,50" size="800,150" text="VERTICAL GRADIENT + TOP CORNERS" font="Regular; 28" foregroundColor="white" halign="center" valign="center" zPosition="1" backgroundGradient="red,green,blue,vertical" />

  <!-- 2. Label with HORIZONTAL gradient and full cornerRadius (all corners) -->
  <eLabel backgroundColor="#ff8800,#ffff00,#00ff00,horizontal" cornerRadius="40" position="50,220" size="800,150" text="HORIZONTAL GRADIENT + FULL CORNERS" font="Regular; 28" foregroundColor="white" halign="center" valign="center" zPosition="1" backgroundGradient="#ff8800,#ffff00,#00ff00,horizontal" />

  <!-- 3. Listbox in GRID mode with item gradients, colored scrollbar, selection zoom -->
  <!-- Note: items are generated automatically (pPreviewEntries) -->
  <widget render="Listbox" position="44,416" size="900,480" font="Regular; 22" itemHeight="160" itemWidth="280" itemSpacing="15,15" listOrientation="grid" selectionZoom="20" selection="2" enableWrapAround="true" scrollbarMode="showAlways" scrollbarWidth="18" scrollbarOffset="6" scrollbarRadius="10" scrollbarForegroundGradient="#ffaa00,#ff8800,#ff5500,vertical" scrollbarSliderForegroundColor="gold" scrollbarSliderBackgroundColor="#333333" scrollbarSliderBorderColor="white" scrollbarSliderBorderWidth="2" itemGradient="#222222,#444444,#222222,vertical" itemGradientSelected="#ffaa00,#ffcc00,#ffaa00,horizontal" itemCornerRadius="15" itemCornerRadiusSelected="25" backgroundColor="#1a1a1a" foregroundColor="#eeeeee" backgroundColorSelected="#000000" foregroundColorSelected="#ffcc00">
    <!-- The listbox will automatically display sample entries (List entry 1,2,...) -->
  </widget>

  <!-- 4. Progress with foreground gradient -->
  <widget render="Progress" position="928,904" size="921,50" backgroundColor="grey_tux" foregroundColor="red,orange,green,horizontal" cornerRadius="25" zPosition="1" />

  <!-- 5. Progress with pixmap (if image exists, otherwise gradient is used) -->
  <widget render="Progress" position="931,965" size="919,50" backgroundColor="#444444" foregroundColor="blue,cyan,white,horizontal" pixmap="progress_bg.png" cornerRadius="15" zPosition="1" />

  <!-- 6. Label widget with data source and converter (ClockToText) -->
  <widget source="global.CurrentTime" render="Label" position="1154,109" size="500,60" font="Regular; 36" halign="center" valign="center" transparent="1" foregroundColor="white" backgroundColor="transparent">
    <convert type="ClockToText">Format:%H:%M:%S</convert>
  </widget>

  <!-- 7. Static label example for alignment verification -->
  <widget render="Label" position="1200,220" size="400,150" text="Static Label with gradients" font="Regular; 28" halign="center" valign="center" transparent="1" backgroundColor="red,blue,black,vertical" foregroundColor="white" cornerRadius="30;bottomLeft,bottomRight" zPosition="1" backgroundGradient="red,blue,black,vertical" />

  <!-- 8. Widget using "Label" render and a dummy source (to test preview text) -->
  <widget source="session.Event_Now" render="Label" position="1000,400" size="800,80" font="Regular; 24" halign="center" valign="center" transparent="1" foregroundColor="white" backgroundColor="black,black,black,vertical" backgroundGradient="black,black,black,vertical">
    <convert type="EventName">Name</convert>
  </widget>
</screen>
```

### v4.2.1.0
This MOD continues from the stable 4.2.0.0 feature set.

It includes a couple of new features i.e.:
* includes
* panels
* colored tree view
* screen search
* fold/unfold xml code
* quick add buttons (add screen, panel, widget, label, pixmap; delete item)
* simple autocomplete in code
* toggle conditional hiding element (show all, none, random, default)
* toggle markers (border indicators of elements)
* position replacement to 'center' disabled
* bugfixes
* etc.

Added/updated support includes:
* v4.2.1.0 MOD by Lululla
* - Refactored gradients: unified into single properties (BackgroundColor, ForegroundGradient) for Label, Progress, Listbox
* - Removed duplicate properties (backgroundGradient1/2/3, orientation) and unused fields
* - Added Source, Render, and exposed CornerRadius as a property
* - Fixed 'center' calculation when rescaling resolution
* - Added Text, Valign, Halign, noWrap properties for Label in sAttributeWidge
* - Integrated automatic fallback from foregroundColor to foregroundGradient
* - Unified font setters using helper method
* - Fixed CS0246 error (RenderConverter) with full type reference
* - Prepared support for WQHD and UHD resolutions" 

### v4.2.0.0 - Gradient backgroundColor and cornerRadius mask support
created by [popking159](https://github.com/popking159)
**thanks for [Lululla](https://github.com/Belfagor2005)
Added
* Added support for Enigma2-style backgroundColor gradients on eLabel.
* Added support for 3-part gradient syntax:
* backgroundColor="#00101010,#00303030,vertical"
* backgroundColor="red,green,vertical"
* backgroundColor="#00ff0000,#0000ff00,vertical"
* Added support for preserving extended cornerRadius syntax:
* cornerRadius="30;topLeft,topRight"
* cornerRadius="30;bottomLeft,bottomRight"
* cornerRadius="30;left"
* cornerRadius="30;right"

** This MOD focuses on compatibility with newer Enigma2 skin syntax while keeping the original OpenSkin Designer workflow.
* `eLabel` `backgroundColor` gradients using 3-part syntax: `startColor,endColor,direction`
* HEX gradient values such as `backgroundColor="#00101010,#00303030,vertical"`
* Named-color gradients such as `backgroundColor="red,green,vertical"`
* `cornerRadius` masks such as `cornerRadius="30;topLeft,topRight"`
* Correct saving of raw gradient and corner-radius mask values without reducing them to simple colors/numbers
* Preview rendering that respects partial rounded corners, for example top-left and top-right only

Example:

```xml
<eLabel position="100,100" size="300,80" text="Gradient label" backgroundColor="#00101010,#00303030,vertical" cornerRadius="30;topLeft,topRight" />
```

Changed
* Improved color parsing so comma-separated gradient values are no longer treated as invalid single colors.
* Updated eLabel background handling so backgroundColor can be used for both normal colors and gradients.
* Updated cornerRadius handling to save the original raw value instead of reducing it to a plain numeric radius.
* Improved preview rendering so corner-radius edge masks are respected visually.

Fixed
* Fixed saving of backgroundColor="#00101010,#00303030,vertical".
* Fixed saving of backgroundColor="red,green,vertical".
* Fixed saving of backgroundColor="#00ff0000,#0000ff00,vertical".
* Fixed saving of cornerRadius="30;topLeft,topRight".
* Fixed preview issue where cornerRadius="30;topLeft,topRight" was displayed as rounded on all four corners.

### v3.3.0.0
created by [Humaxx](https://github.com/Humaxx)
* Focus remains in the selected property grid value

### v3.2.6.6 by kitte888"
* Added some new attributes for eLabels like backgroundGradient, cornerRadius
* Added some new attributes for render listBox like itemCornerRadius

### v3.2.6.5
created by [Humaxx](https://github.com/Humaxx)
* Drawing without color, now using fallback color

### v3.2.6.4
created by [Humaxx](https://github.com/Humaxx)
* Fixed unhandeld Exception (ignoring 'templates')

### v3.2.6.3
created by [Humaxx](https://github.com/Humaxx)
* Fixed typos
* Added dutch translation --> thanks to 'lk1zhm'
* Added new 'Converter.xml and 'simpleConverter.xml'
* Fixed some unhandled Exception when no converter was found

### v3.2.6.2
created by [Humaxx](https://github.com/Humaxx)
* Fixed the display of the error message

### v3.2.6.1
created by [Humaxx](https://github.com/Humaxx)
* Added an option to hide attribut-list in code-editor
* Updated language-files
* After opening the skin, the main node is displayed in the code editor
* Bugfix: Notification about unsafed changes, hasn't work in every case

### v3.2.6.0
created by [Humaxx](https://github.com/Humaxx)
* Undo application termination if a '.svg' graphic is used in the 'borderset's
* If '.svg' graphic is used, the application searches for a corresponding '.png' graphic'

### v3.2.5.9
created by [Humaxx](https://github.com/Humaxx)
* Fixed borderset - bug
* application will be terminated if a '.svg' graphic is used in the 'borderset's

### v3.2.5.8
created by [Humaxx](https://github.com/Humaxx)
* Fixed unhandled Exception when borderset path has not been specified

### v3.2.5.7
created by [Humaxx](https://github.com/Humaxx)
* Support for resolution 3200 x 1800
* Fixed unhandled Exception when borderset has no filename

### v3.2.5.6
created by [Humaxx](https://github.com/Humaxx)
Support for QHD (WQHD) and 4K UHD (Ultra HD)

### v3.2.5.5
created by [Humaxx](https://github.com/Humaxx)
* Add an option to not replace color beginning with '#'

### v3.2.5.4
created by [Humaxx](https://github.com/Humaxx)
* Bugfix: Selected Treeviewnode was deleted when pressing any key in Designer-Mode

### v3.2.5.3
created by [Humaxx](https://github.com/Humaxx)
* Bugfix: fixed unhandled exception if using delete - key without selected item
* Bugfix: using delete-key no longer deletes a selected item in propertygrid

### v3.2.5.2
created by [Humaxx](https://github.com/Humaxx)
* Added an option for linewrapping in code-editor
* Typos
* Added missing translations

### v3.2.5.1
created by [Humaxx](https://github.com/Humaxx)
* Bugfix: fixed unhandled exception if file (include) was not found
* Bugfix: fixed unhandled exception if * is used for integer value
* Added an example in converterSimple.xml for converter-preview-text

### v3.2.5.0
created by [Humaxx](https://github.com/Humaxx)
* Added 'experimental delete-mode'
* Bugfix: Don't delete root-node
* Bugfix: 'Color-Dialog': changed 'Change'-button to 'Rename'-button
* Bugfix: 'Color-Dialog': changing a color now triggers unsafed-changes-notification
* Closing 'Color-Dialog' instead of hiding
* Changes in 'Color-Dialog' now take immediatly effect without the need to save and reload
* Nomore saveing and reloading needed if a color is defined two times.

### v3.2.4.9
created by [Humaxx](https://github.com/Humaxx)
* Using 'delete'-key to delete select element

### v3.2.4.8
created by [Humaxx](https://github.com/Humaxx)
* Add options to show notifications about unsafed changes
* Added missing translations
* Bugfix: Now also a notification is shown, if colors are changed
* Added 'ExtEvent' to converter.xml

### v3.2.4.7
created by [Humaxx](https://github.com/Humaxx)
* Add albanian language (thanks to 'kqiqi1')
* Fixed polish language
* Added missing translations
* Bugfix: now displaying an error message if a font is not valid

### v3.2.4.6
created by [Humaxx](https://github.com/Humaxx)
* Fixed unhandled exception when using right-click in designer
* Add turkish language (thanks to 'audi06)
* Bugfix: restoring language only searches for first language file in languages-directory
* Translate existing element-items after changing language

### v3.2.4.5
created by [Humaxx](https://github.com/Humaxx)
* Displaying the name of the loaded skin.

### v3.2.4.4
created by [Humaxx](https://github.com/Humaxx)
* Added missing translation

### v3.2.4.3
created by [Humaxx](https://github.com/Humaxx)
* Multilanguage support
* Added missing translation
* Settings are now saved

### v3.2.4.2
created by [Humaxx](https://github.com/Humaxx)
* Upgraded search-function
* Added missing translation
* Fixed text from 'Open-Button' in 'Open-Dialog'

### v3.2.4.1 (05.06.2020)
created by [Humaxx](https://github.com/Humaxx)
* Add search for searching text in code editor

### v3.2.4.0 (04.06.2020)
created by [Humaxx](https://github.com/Humaxx)
* Fixed typos
* Fixed unhandled exception in 'Color Dialog'
* Allow only valid characters in Textboxes in 'Color Dialog'
* Support for language file (CustomLanguage.lng) in 'xml'-diretory

### v3.2.3.5 (14.04.2020)
created by [Humaxx](https://github.com/Humaxx)
* Fixed an unhandled exception if image is corrupt
* Only take 'jpg'; 'jpeg' and 'png' for random picture selection

### v3.2.3.4 (01.04.2020)
created by [Humaxx](https://github.com/Humaxx)
* Added render 'ChamaeleonRunningText'
* If pixmap have a path without specified filename, take random image
* Bugfix: pixmap path
* Added all renders containing 'runningtext'
* Handling all renders containing 'list' as listbox
* Notifying about unsafed changes

### v3.2.3.3 (27.03.2020)
created by [Humaxx](https://github.com/Humaxx)
* Fixed path not found exception
* Updated converter.xml
* Added speedyAXBlueRunningText
* Removed doubled attributs
* Added some entries to attribut-list like 'foregroundColors' 'options' 'pixmaps' and more
* Added a option to enable showing full attribut-list
* Autocomplete attribut list - max preview set to 15 instead of 5

### v3.2.3.2 (26.03.2020)
created by [Humaxx](https://github.com/Humaxx)
* Fixed unhandled exception if no Font is declared or only alias - then using 'lcd.ttf'
* Fixed unhandled exceptions if a color is missing or declared with 'foregroundColors'
* Ask to show messageboxes again or not
* Bugfix: show picon also when a path is set
* Added option to set 'Fallback-Color', which is used for previewing some text

### v3.2.3.1 (23.03.2020)
created by [Humaxx](https://github.com/Humaxx)
* Added more sources rendered as listbox
* Fixed unhandled exception if source = null

### v3.2.3.0 (23.03.2020)
created by [Humaxx](https://github.com/Humaxx)
* Undefined colors are added alternatively ('#' is not replaced by 'un')'
* Added a option how to add undefined colors (with '#' or with 'un')
* Fixed unhandled exception if a borderset-file isn't existing
* Fixed unhandled exception in 'Windowstyle-preview' if no borderstyle is declared in skin.xml
* Bug fix in 'Windowstyle-preview': Now displaying correct borderset and filename
* Fixed a bug that probably exists since 3.1.0.3. Font preview is now again working
* Editor: now showing up to 99999 line numbers instead of max 999
* Editor: background color changed for better contrast
* Text-preview: using lcd.ttf if declared font is not found
* Added VTi-Fonts
* Converter bug fixes: 'TimeshiftService' added to prevent a exception in 'Timeshiftstate'
* Corrected xhdpicon.png for building in visual studio

### v3.2.2.0 (08.04.2019 - 21.04.2019)
created by [Scrounger](https://github.com/Scrounger)
* cConverterSimplePresets added
* Alias font bug fixes -> gobal loading / usage added
* Fonts sorting added
* Label: font bug fix property grid -> change font or fontsize
* ListBox font added to property grid
* Show font style and size for listboxes
* Font bug fix -> catch exception if font is not defined or exist
* ListBox: Show entries added
* Label metrixreloadedvrunningtext added
* ListBox: count of entries to show bug fixed
* sAttributePixmap: element with attribute 'path' -> bug fix if skinPath is part of attribute path
* converterSimple.xml: MetrixReloaded converters added

### v3.2.0.0 (08.04.2019)
created by [Scrounger](https://github.com/Scrounger)
* Converter: support for 'FullDescription' added
* Resize picon on element size change
* Use attribute scale for ePixmap & widget which have 'pixmap' attribute.
* Converter MovieInfo added
* Show images for widgets with any render and 'path' attribute
* Show EventImage if render attribute contains 'eventimage'
* Show XHDPicon if render attribute contains 'xhdpicon'
* Show images with 'pixmaps' attribute

### MOD v3.1.0.0 by Jason Hood

- **License**  
  Add the GPLv3 license file.

- **Translation**  
  Replace 'Suchen' with 'Search'.

- **UI improvements**  
  Restore the cursor on leaving the preview.

- **Tree view**  
  Tweak tree labels.

- **Font support**  
  Support for 'alias'.

- **Path handling**  
  Add skin path if file doesn't exist.

- **Menu**  
  Disable 'Save As'.

- **Search**  
  Allow Escape to reset the search.

- **Include & Panel**  
  Support 'include' and 'panel' layout.

- **Resolution**  
  Set resolution exactly, starting zoomed.

- **Properties**  
  Recognise undefined background color in properties.

- **Bug fixes**  
  Fix typo in event duration converter.
  Use bright magenta (#ff00ff) for undefined colors.
  Recognise relative elements.
  Add 'ShortFullDate' converter.
  Fix setting colors.
  Fix conditional labels.

### v2.0.5.0 
* New: Undo - Redo functionality for Designer (Not for the Editor!) 
* New: Allow manual reloading of Converters (Settings->Reload converter.xml) 
* Better: In Designer a right click will always select the parent screen 
* Better: Color-Window reworked 
* Fix: Now possible to change the border of an element 
* Fix: Now possible to change the font of an element 
* Fix: XML Editor should work now!

### v2.0.3.5
* New: Widget Sources are now saved in an external xml (xml/converter.xml) 
* New: Widget Label text can now be configured in an external xml (xml/previewText.xml) 
* New: First Draft of an Preview-Fullscreen mode, F10 
* New: Alpha mode can by deactivated (Button Alpha in Toolbar) 
* Fix: Label noWrap works now correctly 
* Fix: Some general bugfixes

### v2.0.3.0
* Fix: Border-styles are again correctly displayed 
* New: Full-Screen mode: Enter and Leave by pressing F11 
* New: Background-Image support: background.jpg in skins folder 
* New: Full support of alpha blending 
* Fix: Some general fixes

### v2.0.2.6
* Fix: Better font error messages

### v2.0.2.5
* Fix: Center is now also parsed correctly in PropertyGrid 
* New: Mouse-Support: Elements can be oved by pressing LEFT KEY 
* New: Keyboard-Support: Elements can be moved by useing the Cursor Key, Margin is 5pixel, for 1pixel margin press CTRL

### v2.0.1.9
* New: Enhanced XML Editor, with line numbers + Syntax-highlighting

### v2.0.1.5
* Fix: "center" is now diplayed properly in PropertyGrid

### v2.0.1.0
* Fix: Fonts were searched at the wrong place 
* Fix: "300, 300" as position value is now also parsed correctly 
* New: Support for center, center in Windows

### schischu65 Nov 23, 2009
* init
* Initial directory structure.

