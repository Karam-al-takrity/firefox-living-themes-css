# Firefox Living Themes (CSS)

Five animated themes for the Firefox interface, in pure `userChrome.css` and `userContent.css`, with original SVG art. Switch between them live, with no restart, using a setting in `about:config`.

There's no JavaScript, nothing goes in Firefox's program folder, and nothing loads from the internet.

Tested on **Firefox 159 on Windows 11**. Other versions and systems may need small fixes, and issues and pull requests are welcome.

## The themes

- **Nocturne** (the default): pastel glass tabs, a centred address bar, a magnifying bookmarks dock, a rocket loading bar and 20 colour palettes.
- **Ame:** neon on dark glass, with rain running down the toolbar.
- **Relics:** dark red and lantern orange, with a red thread under the active tab.
- **Manga: Ghoul:** slanted panel tabs, a speech-bubble address bar and Japanese sound effects on buttons. Inspired by Tokyo Ghoul.
- **Meridian:** brass and midnight blue, with engraved tab plates and a ruler line under the toolbars.

Every theme also restyles the new tab page, menus, tooltips and private windows.

## Install

1. **Let Firefox load custom styles.** Type `about:config` in the address bar and press Enter. If a warning appears, click **Accept the Risk and Continue**. Search for `toolkit.legacyUserProfileCustomizations.stylesheets` and set it to **true** with the ⇄ button.
2. **Find your profile folder.** Type `about:support` in the address bar. Next to **Profile Folder**, click **Open Folder**.
3. **Download this repo.** On this page, click **Code → Download ZIP** and unzip it.
4. **Copy the files.** Close Firefox completely. If your profile folder already has a `chrome` folder, rename it first (for example to `chrome-old`) to keep a backup. Then copy the `chrome` folder from the download into your profile folder.
5. **Start Firefox.** You should see Nocturne.

## Switching themes

Each theme has an on/off setting: `ame.active`, `relics.active`, `manga.active` and `meridian.active`. Keep **one** of them on, or all of them off for Nocturne. The change is instant.

1. Open `about:config`.
2. Search for the **full name** of the theme you're leaving, for example `meridian.active`, and set it to false with ⇄.
3. Search for the theme you want, for example `manga.active`, and set it to true.

**The first time**, the settings don't exist yet. Firefox offers to create one when you search its name: choose **Boolean** and click **+**.

**Shortcut:** an address like `about:config?filter=manga.active` opens that setting directly. It needs the exact name, so a partial one like `.active` shows nothing. Make a bookmarks folder called **Themes** with one bookmark per theme, and switching takes one click.

## Stopping the animations

Each theme has a freeze setting: `nocturne.freeze`, `ame.freeze`, `relics.freeze`, `manga.freeze` and `meridian.freeze`. Set one to **true** to stop that theme's animations. Themes also respect your system's reduced motion setting.

## Bookmark icons

Bookmarks-bar folders named `AI`, `Social`, `Piracy`, `Tetris`, `TFT`, `Chess`, `Linux` or `Other`, and a bookmark named `Freeze`, get custom icons. Edit the names in each theme's CSS to match your own folders.

## Uninstall

Close Firefox, delete the `chrome` folder from your profile folder (or rename your backup back to `chrome`), and set `toolkit.legacyUserProfileCustomizations.stylesheets` to false.

## Contributing

New themes, fixes for other Firefox versions, and macOS or Linux testing are all welcome. Please keep everything pure CSS, and keep every custom property and keyframe name prefixed with its theme's name. Screenshots of the themes in real Firefox are especially welcome.

## License

Code and art are under the [MIT License](LICENSE).

This is an unofficial fan project, not affiliated with or endorsed by Mozilla or the creators of the works it nods to. Tokyo Ghoul, The Mentalist and the other referenced titles belong to their respective owners. The artwork here is original and contains no material copied from those works.
